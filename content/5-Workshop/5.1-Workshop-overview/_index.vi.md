---
title : "Giới thiệu"
weight : 1
chapter : false
pre : " <b> 5.1. </b> "
---

#### Tổng quan workshop

Mục tiêu: xây webapp kết nối dữ liệu cảm biến ESP32 và gửi cảnh báo khi có sự cố.

Stack & dịch vụ
- Frontend: React (JS/TS) host trên Amplify, code GitHub, domain Route 53 (`www.iotsecuredmonitor.click`).
- Auth: Amazon Cognito user pool.
- API: Amazon API Gateway + Lambda.
- Ingest IoT: AWS IoT Core + IoT Rule → Lambda; lưu DynamoDB và S3.
- Cảnh báo: Amazon SES (email).

Luồng dữ liệu (theo sơ đồ)
1) Cảm biến ESP32 gửi qua Internet Gateway vào **IoT Core**.  
2) **IoT Rule** chuyển tiếp thông điệp.  
3) **Lambda** xử lý, ghi **DynamoDB/S3**, và gọi **SES** gửi cảnh báo.  
4) Người dùng truy cập web trên **Amplify** qua **Route 53**; **Cognito** xác thực đăng nhập.  
5) UI gọi **API Gateway** (Lambda backend) để lấy dữ liệu/trạng thái.

Kết quả & ghi chú
- Site hoạt động: `https://www.iotsecuredmonitor.click`.  
- Hoàn thiện pipeline IoT → cloud → web; khó khăn ban đầu do lần đầu dùng nhiều dịch vụ AWS và giới hạn chi phí, nhưng đã triển khai thành công và có cảnh báo hoạt động.
