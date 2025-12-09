---
title: "Sử dụng SES"
weight: 4
chapter: false
pre: " <b> 5.4. </b> "
---

#### Tổng quan

Trong phần này, bạn sẽ học cách sử dụng **Amazon Simple Email Service (SES)** để gửi email từ ứng dụng hoặc môi trường backend của bạn. SES là một nền tảng email được quản lý hoàn toàn hỗ trợ các tin nhắn giao dịch, thông báo và chiến dịch marketing. Bạn sẽ xác minh danh tính email hoặc domain của mình, cấu hình các cài đặt cơ bản, và hiểu cách SES xử lý và gửi tin nhắn.

---

## Tại sao sử dụng Amazon SES

Amazon SES được sử dụng phổ biến trong các ứng dụng cloud nhờ tính đáng tin cậy, hiệu quả về chi phí và dễ dàng tích hợp.

- **Khả năng gửi cao:** SES sử dụng các máy chủ mail đáng tin cậy của Amazon và hỗ trợ SPF, DKIM, và DMARC để giảm lọc spam.
- **Tích hợp linh hoạt:** Gửi email qua SES API, AWS SDK, giao diện SMTP, hoặc Lambda.
- **Có thể mở rộng và tiết kiệm chi phí:** Phù hợp cho khối lượng công việc từ nhỏ đến lớn, chỉ tốn $0.10 cho 1,000 email.
- **Giám sát tích hợp:** Theo dõi bounces, complaints, và deliveries bằng SNS và CloudWatch.
- **An toàn và được kiểm soát:** Quản lý quyền với IAM policies và hạn chế danh tính gửi được phép.

---

## Kiến trúc SES

Kiến trúc Amazon SES được xây dựng xung quanh ba thành phần cốt lõi xác định cách email được xác thực, truyền tải và giám sát.

### 1. Verified Identities (Danh tính đã xác minh)

Trước khi gửi tin nhắn, SES yêu cầu xác minh domain hoặc địa chỉ email gửi của bạn.  
Điều này ngăn chặn việc sử dụng trái phép và đảm bảo SES có thể gửi email thay mặt bạn.

Xác minh thường yêu cầu các bản ghi DNS:

- **SPF (TXT)** — xác minh người gửi
- **DKIM (CNAME)** — cung cấp chữ ký mật mã
- **DMARC (TXT, tùy chọn)** — thêm bảo vệ cấp domain

---

### 2. Quy trình gửi Email

Sau khi hoàn tất xác minh, ứng dụng của bạn có thể gửi tin nhắn bằng SES API, AWS SDKs, hoặc SMTP.

Quy trình tổng quan:
SES tự động xử lý định tuyến email, thử lại, điều chỉnh và định dạng.

### 3. Cách thực hiện

Nhấn **Get Started**
Điền **Email** của bạn
Nhấn **Next**

## Hướng dẫn Triển khai từng bước

### Phần 1: Truy cập Amazon SES Console

1. Đăng nhập vào **AWS Management Console**
2. Điều hướng đến dịch vụ **Amazon SES**
3. Chọn region ưa thích của bạn (ví dụ: **ap-southeast-1**)
4. Nhấn nút **Get Started**

---

### Phần 2: Tạo Email Identity

**Bước 1:** Chọn loại Identity

- Điều hướng đến **Verified identities** trong thanh bên trái
- Nhấn **Create identity**
  ![Create Identity](/images/5-Workshop/5.4-SES-img/SES-B1.png)
- Chọn giữa:
  - **Email address** - Thiết lập nhanh, tốt cho testing
  - **Domain** - Sử dụng production, linh hoạt hơn

**Bước 2:** Xác minh địa chỉ Email

1. Chọn tùy chọn **Email address**
2. Nhập địa chỉ email của bạn (ví dụ: `your-email@gmail.com`)
3. Nhấn **Create identity**
   ![Create Identity](/images/5-Workshop/5.4-SES-img/SES-B2.png)

**Bước 3:** Xác minh Email của bạn

4. Kiểm tra hộp thư đến của bạn để tìm email xác minh từ AWS
5. Chủ đề: "Amazon Web Services – Email Address Verification Request"
6. Nhấn vào link xác minh trong email
7. Quay lại SES console
8. Làm mới trang - Trạng thái sẽ hiển thị **Verified**
   ![Create Identity](/images/5-Workshop/5.4-SES-img/SES-B3.png)

---

### Phần 3: Xác minh Domain (Tùy chọn - Khuyến nghị cho Production)

**Bước 1:** Tạo Domain Identity

1. Nhấn **Create identity**
2. Chọn tùy chọn **Domain**
3. Nhập tên domain của bạn (ví dụ: `iotsecuredmonitor.click`)
4. Chọn **Use a custom MAIL FROM domain** (tùy chọn)
   ![Domain Verification](/images/5-Workshop/5.4-SES-img/SES-P3B1.png)
5. Nhấn **Create identity**
   ![Domain Verification](/images/5-Workshop/5.4-SES-img/SES-P3B1.1.png)

**Bước 2:** Lấy bản ghi DNS

6. Sau khi tạo, nhấn nút **Get DNS records**
7. Bạn sẽ thấy 3 loại bản ghi:

**Bản ghi DKIM (3 bản ghi CNAME):**

**Bản ghi SPF (bản ghi TXT):**

**Bản ghi DMARC (bản ghi TXT - tùy chọn):**

![Domain Verification](/images/5-Workshop/5.4-SES-img/SES-P3B2.png)

### Phần 4: Gửi Email thử nghiệm

**Bước 1:** Điều hướng đến Test Email

1. Đi đến Verified identities
2. Chọn email hoặc domain đã xác minh của bạn
3. Nhấn nút Send test email
   ![Send Test Email](/images/5-Workshop/5.4-SES-img/SES-P4B1.png)

**Bước 2:** Cấu hình Email thử nghiệm

1. Kịch bản định dạng email:

- Formatted - Email HTML/text đơn giản
- Raw - Tin nhắn MIME đầy đủ
- Custom - Headers tùy chỉnh
- Templated - Sử dụng email template

2. From address: Email đã xác minh của bạn

3. To address: Email người nhận

- Lưu ý: Ở chế độ Sandbox, người nhận cũng phải được xác minh

4. Subject: Nhập chủ đề email

5. Body:

- Text: Phiên bản văn bản thuần
- HTML: Phiên bản định dạng HTML

![Send Test Email](/images/5-Workshop/5.4-SES-img/SES-P4B2.png)

**Bước 3:** Gửi Email

1. Nhấn Send test email
2. Kiểm tra hộp thư đến của người nhận
3. Xác minh việc gửi email

### Phần 5: Cấu hình Giám sát Email

Giám sát Email

**Bước 1:** Tạo Configuration Set

1. Đi đến Configuration sets
2. Nhấn Create set
   ![Email Monitoring](/images/5-Workshop/5.4-SES-img/SES-P5B1.png)
3. Nhập tên: production-emails
4. Nhấn Create
   ![Email Monitoring](/images/5-Workshop/5.4-SES-img/SES-P5B1.1.png)
   ![Email Monitoring](/images/5-Workshop/5.4-SES-img/SES-P5B1.2.png)

**Bước 2:** Thêm Event Destination

1. Chọn configuration set của bạn
2. Nhấn Add destination
   ![Email Monitoring](/images/5-Workshop/5.4-SES-img/SES-P5B2.png)
3. Chọn loại destination:
   ![Email Monitoring](/images/5-Workshop/5.4-SES-img/SES-P5B2.1.png)
   ![Email Monitoring](/images/5-Workshop/5.4-SES-img/SES-P5B2.2.png)
   ![Email Monitoring](/images/5-Workshop/5.4-SES-img/SES-P5B2.3.png)

**Bước 3:** Bật Reputation Metrics

1. Trong cài đặt configuration set
2. Bật Reputation metrics
   ![Email Monitoring](/images/5-Workshop/5.4-SES-img/SES-P5B3.png)
   ![Email Monitoring](/images/5-Workshop/5.4-SES-img/SES-P5B3.1.png)
