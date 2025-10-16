---
title: Hội Thảo
date: 2025-10-11
weight: 5
chapter: false
pre: " <b> 5. </b>"
---
Phần này ghi lại các hội thảo mà tôi đã tạo và trình bày trong thời gian thực tập.

Với Session Manager chúng ta có thể xem được lịch sử các kết nối tới các instance thông qua **Session history**. Tuy nhiên chúng ta chưa xem được chi tiết các câu lệnh được sử dụng.

## Hội Thảo: AWS Systems Manager Session Manager

![S3](/images/4.s3/001-s3.png)

### Tổng Quan

Trong phần này chúng ta sẽ tiến hành tạo S3 bucket và thực hiện cấu hình lưu trữ các session logs để xem được chi tiết các câu lệnh được sử dụng trong session.

Một hội thảo toàn diện về việc sử dụng AWS Systems Manager Session Manager để quản lý instance một cách an toàn mà không cần máy chủ bastion hoặc khóa SSH.

![port-fwd](/images/arc-log.png)

### Đối Tượng Tham Gia

### Nội dung

- Kỹ sư Điện toán Đám mây AWS

- Quản trị viên Hệ thống  - [Cập nhật IAM Role](./4.1-updateiamrole/)

- Kỹ sư DevOps  - [Tạo **S3 Bucket**](./4.2-creates3bucket/)

  - [Tạo S3 Gateway endpoint](./4.3-creategwes3)

### Điều Kiện Tiên Quyết  - [Cấu hình **Session logs**](./4.4-configsessionlogs/)

- Hiểu biết cơ bản về dịch vụ AWS
- Tài khoản AWS với quyền hạn thích hợp
- Quen thuộc với instances EC2

### Chủ Đề Được Đề Cập

1. Tổng quan về Session Manager
2. Thiết lập Session Manager
3. Quản lý Instances EC2
4. Ghi nhật ký và Giám sát
5. Thực hành tốt nhất về Bảo mật

### Thực Hành

1. Tạo và Cấu hình Instances EC2
2. Thiết lập Vai trò và Quyền hạn IAM
3. Triển khai Ghi nhật ký Phiên
4. Làm việc với Instances Private
5. Xử lý Các Vấn đề Thường gặp

### Tài Nguyên Cung Cấp

- Hướng dẫn từng bước
- Sơ đồ kiến trúc
- Mẫu chính sách IAM
- Mẫu cấu hình
- Hướng dẫn xử lý sự cố

### Tác Động Của Hội Thảo

- Đào tạo hơn 20 người tham gia
- Nâng cao hiểu biết về quản lý instance an toàn
- Giảm phụ thuộc vào máy chủ bastion
- Tăng cường thực hành bảo mật
