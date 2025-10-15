---

title : "Tự Đánh Giá"

date: 2025-10-11
date: 2025-09-30

weight : 6

chapter : false

pre : " <b> 6. </b> "

---

Phần này chứa đánh giá của tôi về các kỹ năng đã phát triển và các lĩnh vực cần cải thiện trong thời gian thực tập.{{% notice info %}}

**Port Forwarding** là mốt cách thức hữu ích để chuyển hướng lưu lượng mạng từ 1 địa chỉ IP - Port này sang 1 địa chỉ IP - Port khác. Với **Port Forwarding** chúng ta có thể truy cập một EC2 instance nằm trong private subnet từ máy trạm của chúng ta.

## Phát Triển Kỹ Năng Kỹ Thuật{{% /notice %}}

### Các Dịch Vụ AWS Đã Thành ThạoChúng ta sẽ cấu hình **Port Forwarding** cho kết nối RDP giữa máy của mình với **Private Windows Instance** nằm trong private subnet mà chúng ta đã tạo cho bài thực hành này

- Cấu hình EC2 và VPC![port-fwd](/images/arc-04.png)

- Systems Manager và Session Manager

- Vai trò và Chính sách IAM

- S3 và Giải pháp Lưu trữ

- Ghi nhật ký CloudWatch#### Tạo IAM User có quyền kết nối SSM

### Lập Trình và Công Cụ1. Truy cập vào [giao diện quản trị dịch vụ IAM](https://console.aws.amazon.com/iamv2/home)

- Click **Users** , sau đó click **Add users**.

- Thành thạo AWS CLI

- Lập trình Shell Script![FWD](/images/5.fwd/001-fwd.png)

- Cơ sở hạ tầng dưới dạng Code (IaC)

- Kiểm soát phiên bản Git2. Tại trang **Add user**.

- Tài liệu kỹ thuật  + Tại mục **User name**, điền **Portfwd**.

  - Click chọn **Access key - Programmatic access**.

## Phát Triển Chuyên Môn  + Click **Next: Permissions**

### Điểm Mạnh Đã Phát Triển![FWD](/images/5.fwd/002-fwd.png)

- Quản lý dự án3. Click **Attach existing policies directly**.

- Tài liệu kỹ thuật  + Tại ô tìm kiếm , điền **ssm**.

- Giải quyết vấn đề  + Click chọn **AmazonSSMFullAccess**.

- Hợp tác nhóm  + Click **Next: Tags**, click **Next: Reviews**.

- Quản lý thời gian  + Click **Create user**.

### Lĩnh Vực Cần Cải Thiện4. Lưu lại thông tin **Access key ID** và **Secret access key** để thực hiện cấu hình AWS CLI

- Kiến trúc AWS Nâng cao#### Cài đặt và cấu hình AWS CLI và Session Manager Plugin

- Chiến lược Tối ưu hóa Chi phí  

- Kiểm tra Hiệu suấtĐể thực hiện phần thực hành này, đảm bảo máy trạm của bạn đã cài [AWS CLI]() và [Session Manager Plugin](https://docs.aws.amazon.com/systems-manager/latest/userguide/session-manager-working-with-install-plugin.html)

- Script Tự động hóa

- Nói trước công chúngBạn có thể tham khảo thêm bài thực hành về cài đặt và cấu hình AWS CLI [tại đây](https://000011.awsstudygroup.com/).

## Thành Tựu Chính{{%notice tip%}}

Với Windows thì khi giải nén thư mục cài đặt **Session Manager Plugin** bạn hãy chạy file **install.bat** với quyền Administrator để thực hiện cài đặt.

1. Tạo tài liệu hội thảo toàn diện{{%/notice%}}

2. Triển khai giải pháp quản lý instance an toàn

3. Đóng góp vào tài liệu của nhóm#### Thực hiện Portforwarding

4. Tham gia các sự kiện cộng đồng

1. Chạy command dưới đây trong **Command Prompt** trên máy của bạn để cấu hình **Port Forwarding**.

## Kết Quả Học Tập

```bash

- Hiểu sâu về dịch vụ AWS  aws ssm start-session --target (your ID windows instance) --document-name AWS-StartPortForwardingSession --parameters portNumber="3389",localPortNumber="9999" --region (your region) 

- Thực hành tốt nhất trong bảo mật đám mây```

- Kỹ năng viết tài liệu kỹ thuật{{%notice tip%}}

- Chiến lược giải quyết vấn đề hiệu quả

Thông tin **Instance ID** của **Windows Private Instance** có thể tìm được khi bạn xem chi tiết máy chủ EC2 Windows Private Instance.

## Mục Tiêu Phát Triển Tương Lai

{{%/notice%}}

1. Chứng chỉ AWS Professional

2. Thiết kế Kiến trúc Nâng cao  + Câu lệnh ví dụ

3. Đóng góp cho Mã nguồn Mở

4. Phát triển Kỹ năng Lãnh đạo```
C:\Windows\system32>aws ssm start-session --target i-06343d7377486760c --document-name AWS-StartPortForwardingSession --parameters portNumber="3389",localPortNumber="9999" --region ap-southeast-1
```

{{%notice warning%}}

Nếu câu lệnh của bạn báo lỗi như dưới đây : \
SessionManagerPlugin is not found. Please refer to SessionManager Documentation here: <http://docs.aws.amazon.com/console/systems-manager/session-manager-plugin-not-found\>
Chứng tỏ bạn chưa cài Session Manager Plugin thành công. Bạn có thể cần khởi chạy lại **Command Prompt** sau khi cài **Session Manager Plugin**.

{{%/notice%}}

2. Kết nối tới **Private Windows Instance** bạn đã tạo bằng công cụ **Remote Desktop** trên máy trạm của bạn.

- Tại mục Computer: điền **localhost:9999**.

![FWD](/images/5.fwd/003-fwd.png)

3. Quay trở lại giao diện quản trị của dịch vụ System Manager - Session Manager.

- Click tab **Session history**.
- Chúng ta sẽ thấy các session logs với tên Document là **AWS-StartPortForwardingSession**.

![FWD](/images/5.fwd/004-fwd.png)

Chúc mừng bạn đã hoàn tất bài thực hành hướng dẫn cách sử dụng Session Manager để kết nối cũng như lưu trữ các session logs trong S3 bucket. Hãy nhớ thực hiện bước dọn dẹp tài nguyên để tránh sinh chi phí ngoài ý muốn nhé.
