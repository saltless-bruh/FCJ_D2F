---
title: "Workshop"
weight: 5
chapter: false
pre: " <b> 5. </b> "
---
# IoT Security Workshop

#### Tổng quan
- Xây dựng webapp kết nối dữ liệu cảm biến ESP32, có cảnh báo sự cố.
- Stack: React (JS/TS) trên Amplify + Route 53, Cognito cho đăng nhập, API Gateway + Lambda backend.
- Ingest IoT: AWS IoT Core + Rule → Lambda, lưu DynamoDB/S3; SES gửi email cảnh báo.
- Site chạy: `https://www.iotsecuredmonitor.click`.

#### Nội dung
1. [Tổng quan workshop](5.1-Workshop-overview/)
2. [Chuẩn bị](5.2-Prerequiste/)
3. [Kết nối IoT Core với DynamoDB](5.3-S3-Iot%20core/)
4. [Sử dụng SES](5.4-SES/)
5. [Sử dụng Route 53](5.5-Route53/)
6. [Sử dụng S3](5.6-S3/)
7. [Triển khai với Amplify](5.7-Amplify/)
8. [Cấu hình Cognito](5.8-Cognito/)
9. [Tạo API với API Gateway](5.9-API%20Gateway/)
10. [Xây dựng Lambda Function](5.10-Lambda/)
