---
title: "Sử dụng Route 53"
weight: 5
chapter: false
pre: " <b> 5.5. </b> "
---

#### Tổng quan

Trong phần này, bạn sẽ học cách sử dụng **Amazon Route 53** để quản lý DNS cho dự án giám sát nhiệt độ và độ ẩm IoT của bạn. Route 53 sẽ giúp bạn cấu hình domain tùy chỉnh cho ứng dụng web, thiết lập bản ghi DNS cho dịch vụ email (SES), và tạo subdomain cho các thành phần khác nhau của hệ thống IoT.

---

## Amazon Route 53 là gì?

**Amazon Route 53** là dịch vụ web Domain Name System (DNS) có tính sẵn sàng cao và có khả năng mở rộng được thiết kế để định tuyến người dùng cuối đến ứng dụng của bạn bằng cách chuyển đổi tên miền thành địa chỉ IP.

### Các tính năng chính:

- **Domain Registration** - Đăng ký tên miền mới trực tiếp qua AWS
- **DNS Management** - Tạo và quản lý bản ghi DNS (A, CNAME, TXT, MX, v.v.)
- **Health Checks** - Giám sát sức khỏe endpoint và định tuyến lưu lượng tương ứng
- **Traffic Routing** - Định tuyến thông minh dựa trên độ trễ, địa lý, hoặc chính sách có trọng số
- **Integration with AWS** - Hoạt động liền mạch với EC2, S3, CloudFront, Load Balancers, v.v.

---

## Tại sao sử dụng Route 53 cho dự án IoT?

Đối với hệ thống giám sát nhiệt độ và độ ẩm IoT của bạn, Route 53 cung cấp:

✅ **Custom Domain** - URL chuyên nghiệp như `iotmonitor.click` thay vì URL CloudFront/S3  
✅ **API Endpoint** - Subdomain API sạch `api.iotmonitor.click` cho API Gateway  
✅ **MQTT Endpoint** - Endpoint tùy chỉnh cho kết nối thiết bị IoT  
✅ **SSL/TLS Certificates** - Yêu cầu xác thực DNS cho HTTPS  
✅ **High Availability** - SLA uptime 100%, máy chủ DNS dự phòng trên toàn thế giới  
✅ **Serverless Integration** - Hoạt động liền mạch với S3, CloudFront, API Gateway, Lambda

---

## Hướng dẫn Triển khai từng bước

### Phần 1: Truy cập Amazon Route 53 Console

1. Đăng nhập vào **AWS Management Console**
2. Trong thanh tìm kiếm, nhập **Route 53**
3. Nhấn vào dịch vụ **Route 53**
4. Bạn sẽ thấy dashboard Route 53

## ![Access Amazon Route 53](/images/5-Workshop/5.5-R53-img/R53-P1B1.png)

---

### Phần 2: Tạo Hosted Zone

Đối với workshop này, chúng tôi giả sử bạn đã sở hữu một domain từ nhà đăng ký (GoDaddy, Namecheap, Cloudflare, v.v.). Chúng ta sẽ tạo hosted zone trong Route 53 để quản lý bản ghi DNS.

**Lưu ý:** Đăng ký domain qua Route 53 không được bao gồm trong AWS Free Tier. Bạn có thể sử dụng domain hiện có hoặc mua từ nhà đăng ký bên ngoài bắt đầu từ $1-3/năm.

## ![Create Hosted Zone](/images/5-Workshop/5.5-R53-img/R53-P2B1.png)

**Bước 1:** Tạo Hosted Zone

1. Nhấn **Hosted zones** trong thanh bên trái
2. Nhấn nút **Create hosted zone**

## ![Create Hosted Zone](/images/5-Workshop/5.5-R53-img/R53-P2B2.png)

**Bước 2:** Cấu hình Hosted Zone

1. **Domain name:** Nhập domain của bạn (ví dụ: `iotmonitor.click`)
2. **Description:** Mô tả tùy chọn (ví dụ: "IoT Monitoring System DNS")
3. **Type:**
   - ✅ **Public hosted zone** (cho domain có thể truy cập từ internet)
   - ⚪ Private hosted zone (cho DNS nội bộ VPC)
4. **Tags:** Tùy chọn (ví dụ: `Project: IoT-Monitor`)
5. Nhấn **Create hosted zone**

## ![Create Hosted Zone](/images/5-Workshop/5.5-R53-img/R53-P2B3.png)

**Bước 3:** Ghi chú Name Servers
Sau khi tạo, bạn sẽ thấy 4 bản ghi NS (Name Server):

```
ns-123.awsdns-12.com
ns-456.awsdns-34.net
ns-789.awsdns-56.org
ns-012.awsdns-78.co.uk
```

**Bước 4:** Cập nhật Name Servers tại Domain Registrar
Đi đến nhà đăng ký domain của bạn (GoDaddy, Namecheap, v.v.) và:

1. Đăng nhập vào tài khoản của bạn
2. Tìm **DNS Management** hoặc **Name Servers**
3. Thay đổi thành **Custom Name Servers**
4. Thêm tất cả 4 name servers của Route 53
5. Lưu thay đổi

**Đợi 24-48 giờ để DNS lan truyền**

**Xác minh name servers đã thay đổi:**

```bash
nslookup -type=NS iotmonitor.click
```

---

### Phần 3: Tạo bản ghi DNS cho ứng dụng IoT

---

#### 3.1: Tạo bản ghi A cho Website chính (CloudFront Distribution)

**Bước 1:** Tạo Record

1. Chọn hosted zone của bạn
2. Nhấn **Create record**

**Bước 2:** Cấu hình bản ghi A (Alias) cho CloudFront

```
Record name: [để trống cho root domain]
Record type: A - IPv4 address
Alias: Yes
Alias target: CloudFront distribution
  - Chọn "Alias to CloudFront distribution"
  - Chọn CloudFront distribution của bạn từ dropdown
  - Ví dụ: d123abc456def.cloudfront.net
Routing policy: Simple routing
```

![Create Record](/images/5-Workshop/5.5-R53-img/R53-P3B1.png)

---

#### 3.2: Tạo bản ghi A cho API Subdomain (API Gateway)

**Bước 1:** Tạo Record

1. Nhấn **Create record**

**Bước 2:** Cấu hình bản ghi A (Alias) cho API Gateway

```
Record name: api
Record type: A - IPv4 address
Alias: Yes
Alias target: API Gateway API
  - Chọn "Alias to API Gateway API"
  - Region: us-east-1 (hoặc region của bạn)
  - Chọn API Gateway endpoint của bạn từ dropdown
  - Ví dụ: abc123xyz.execute-api.us-east-1.amazonaws.com
Routing policy: Simple routing
```

![Create Record](/images/5-Workshop/5.5-R53-img/R53-P3B1.png)

---

## Tài nguyên bổ sung

- **AWS Route 53 Documentation:** https://docs.aws.amazon.com/route53/
- **DNS Record Types:** https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/ResourceRecordTypes.html
- **SES Domain Verification:** https://docs.aws.amazon.com/ses/latest/dg/verify-domain-procedure.html
- **Route 53 Pricing:** https://aws.amazon.com/route53/pricing/
- **DNS Propagation Checker:** https://dnschecker.org
- **DMARC Guide:** https://dmarc.org/overview/

---

## Kết luận

Chúc mừng! Bạn đã cấu hình thành công Amazon Route 53 cho dự án giám sát nhiệt độ và độ ẩm IoT của mình.
