---
title: "Đề xuất Dự Án Hệ Thống Giám Sát & Cảnh Báo An Toàn IoT"
date: 2025-09-30
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

## 1. Tổng Quan Dự Án

### Tên Dự Án

#### Hệ Thống Giám Sát & Cảnh Báo An Toàn IoT Cho Smart Home Trên Nền Tảng AWS

### Mô Tả Dự Án

Phát triển hệ thống giám sát và cảnh báo an toàn IoT toàn diện cho ngôi nhà thông minh, kết hợp tích hợp sensor phần cứng, giao thức bảo mật tiên tiến, kiến trúc backend serverless và dashboard trực quan real-time. Hệ thống cung cấp khả năng giám sát end-to-end các thông số môi trường (nhiệt độ, độ ẩm, phát hiện khí gas, chuyển động) với các biện pháp bảo mật mạnh mẽ và phân tích dữ liệu trên cloud.

### Thông Tin Đội Ngũ

- **Quy Mô Đội**: 5 thành viên (sinh viên năm 3 đại học)
- **Cấu Trúc Đội**:
  - 2 Kỹ Sư IC Design (Chuyên gia Hardware/Firmware)
  - 2 Kỹ Sư Phần Mềm (Chuyên gia Backend/Frontend)  
  - 1 Chuyên Gia Bảo Mật (Expert Cybersecurity & PKI)

### Thời Gian Thực Hiện

**3 tháng** (Tháng 9/2025 - Tháng 11/2025)

### Tổng Ngân Sách

**$100 USD** phân bổ cho hai thành phần chính:

- Phát triển WebApp: $10
- IoT Hardware & Firmware: $40

### Quy Mô Ứng Dụng

**Smart Home** - Một ngôi nhà tiêu biểu với 3 sensor nodes phủ sóng các khu vực quan trọng.

---

## 2. Mục Tiêu Dự Án

### Mục Tiêu Chính

1. **Phát triển hệ sinh thái IoT** cho giám sát smart home
2. **Triển khai hệ thống giám sát real-time** cho các thông số môi trường và an toàn
3. **Tạo backend serverless có khả năng mở rộng** sử dụng các dịch vụ AWS được quản lý
4. **Xây dựng giao diện dashboard trực quan** cho giám sát và quản lý thiết bị

### Chỉ Số Thành Công Chính

- **Kết Nối Thiết Bị**: 99.9% uptime cho kết nối thiết bị IoT
- **Hiệu Suất Real-time**: <100ms độ trễ cho cảnh báo quan trọng
- **Trải Nghiệm Người Dùng**: Dashboard responsive có thể truy cập trên web và mobile
- **Hiệu Quả Chi Phí**: Giữ trong ngân sách $100 trong khi đạt được production-ready prototype

---

## 3. Kiến Trúc Kỹ Thuật

### 3.1 Lớp Phần Cứng (Thiết Bị IoT)

- **Vi Điều Khiển**: ESP32 với khả năng WiFi tích hợp
- **Cảm Biến**: Nhiệt độ/độ ẩm (DHT11), Phát hiện khí gas (MQ series), Cảm biến lửa MKE-S04 IR
- **Giao Tiếp**: MQTT over TLS 1.3 cho truyền dữ liệu an toàn

### 3.2 Tích Hợp Dịch Vụ AWS Cloud

| Dịch Vụ | Mục Đích | Chi Phí Ước Tính Hàng Tháng |
|---------|---------|---------------------------|
| **AWS IoT Core** | Gateway thiết bị và messaging | $3-8 (cho smart home) |
| **AWS IoT Rules** | Định tuyến và lọc thông điệp | Miễn phí |
| **AWS Lambda** | Logic business serverless | $10.25 |
| **Amazon DynamoDB** | Database NoSQL cho dữ liệu sensor | $0.36 |
| **Amazon S3** | Lưu trữ và sao lưu dữ liệu | $1-2 |
| **Amazon SES** | Dịch vụ gửi email thông báo | $1-2 |
| **API Gateway** | Endpoints RESTful API | $6.25 |
| **Amazon Cognito** | Xác thực và phân quyền người dùng | $1-2 |
| **AWS Amplify** | Hosting frontend và CI/CD | $1-2 |
| **Amazon Route 53** | Quản lý DNS và domain | $1-2 |

### 3.3 Sơ Đồ Kiến Trúc Hệ Thống

![Kiến Trúc Hệ Thống](/FCJ_D2F/images/Diagrams.png)

---

## 4. Phân Tích Ngân Sách

### 4.1 Phát Triển WebApp ($10)

- **Framework Frontend**: Công cụ phát triển React.js/Vue.js - free
- **Testing & Deployment**: AWS S3/CloudFront hosting - $10
- **Thư Viện Phát Triển**: Chart.js, Material-UI, WebSocket libraries - free
- **Tài Liệu & Đào Tạo**: Tài nguyên technical writing - free

### 4.2 IoT Hardware & Firmware ($40)

- **Board Phát Triển**: 3x ESP32 development kits cho smart home - $15
- **Cảm Biến & Linh Kiện**: Sensor nhiệt độ, độ ẩm, khí gas, chuyển động - $10
- **Nguồn Điện & Vỏ Bảo Vệ**: Housing và quản lý nguồn - $10
- **Linh Kiện Kết Nối**: WiFi modules và antenna - $5

---

## 5. Kế Hoạch Thực Hiện

### Giai Đoạn 1: Nền Tảng (Tháng 1)

#### Tuần 1-2: Kiến Trúc & Lập Kế Hoạch

- Thiết kế kiến trúc hệ thống và tài liệu hóa
- Setup tài khoản AWS và cấu hình dịch vụ
- Chuẩn bị môi trường phát triển
- Đào tạo đội ngũ về AWS services và giao thức bảo mật

#### Tuần 3-4: Phát Triển Cốt Lõi

- Thiết kế sơ đồ hardware và sourcing linh kiện
- Phát triển firmware cơ bản cho tích hợp sensor
- Thiết kế backend API và các Lambda function ban đầu
- Thiết kế database schema

### Giai Đoạn 2: Tích Hợp (Tháng 2)

#### Tuần 5-6: Tích Hợp Hardware-Software

- Lắp ráp linh kiện
- Triển khai communication từ thiết bị lên cloud
- Phát triển pipeline dữ liệu real-time
- Setup xác thực người dùng

#### Tuần 7-8: Phát Triển Frontend

- Thiết kế UI/UX dashboard
- Phát triển dashboard frontend
- Triển khai responsive cho mobile

### Giai Đoạn 3: Testing & Deployment (Tháng 3)

#### Tuần 9-10: Testing Tích Hợp Hệ Thống

- Testing và validation hệ thống end-to-end
- Tối ưu hiệu suất và load testing
- User acceptance testing và tích hợp feedback
- Sửa lỗi và cải tiến

#### Tuần 11-12: Chuẩn Bị Sản Xuất

- Hoàn thiện tài liệu
- Production deployment và setup monitoring
- Validation hệ thống cuối cùng
- Chuẩn bị presentation và demonstration dự án

---

## 6. Sản Phẩm Bàn Giao

### 6.1 Sản Phẩm Hardware

- ***IoT Sensor Boards**: 12 prototype hoàn chính với sensor tích hợp cho smart home*
- **Tài Liệu Hardware**: Schematics và hướng dẫn lắp ráp
- **Hướng Dẫn Manufacturing**: Tài liệu sẵn sàng sản xuất để scale-up

### 6.2 Sản Phẩm Software

- **Backend API**: RESTful services với tài liệu toàn diện
- **Frontend Dashboard**: Ứng dụng web responsive với giám sát real-time
- **Mobile Interface**: Progressive Web App (PWA) cho truy cập mobile device
- **Database Schema**: Data models tối ưu cho dữ liệu time-series sensor

---

## 7. Đánh Giá Rủi Ro & Giảm Thiểu

### 7.1 Rủi Ro Kỹ Thuật

| Rủi Ro                    | Tác Động   | Xác Suất   | Chiến Lược Giảm Thiểu                                   |
| ------------------------- | ---------- | ---------- | ------------------------------------------------------- |
| Delay linh kiện hardware  | Cao        | Trung bình | Order sớm, duy trì backup suppliers                     |
| Vượt chi phí AWS service  | Trung bình | Thấp       | Monitoring chi phí, sử dụng free tier hiệu quả          |
| Phát hiện lỗ hổng bảo mật | Cao        | Thấp       | Testing bảo mật thường xuyên, follow AWS best practices |
| Độ phức tạp integration   | Trung bình | Trung bình | Integration từng bước, comprehensive testing            |

### 7.2 Rủi Ro Quản Lý Dự Án

| Rủi Ro                       | Tác Động   | Xác Suất   | Chiến Lược Giảm Thiểu                             |
| ---------------------------- | ---------- | ---------- | ------------------------------------------------- |
| Thành viên team không có sẵn | Trung bình | Thấp       | Cross-training, documentation, backup assignments |
| Delay timeline               | Trung bình | Trung bình | Buffer time allocation, milestone tracking        |
| Ràng buộc ngân sách          | Cao        | Thấp       | Weekly budget tracking, cost optimization         |

---

## 8. Kết Quả Mong Đợi & Tác Động

### 8.1 Thành Tựu Kỹ Thuật

- **Hệ Thống IoT Hoạt Động**: production-ready prototype thể hiện tất cả tính năng chính
- **Hiệu Suất Real-time**: Thời gian phản hồi dưới giây cho cảnh báo và thông báo quan trọng
- **Kiến Trúc Có Khả Năng Mở Rộng**: Thiết kế cloud-native sẵn sàng mở rộng

### 8.2 Kết Quả Học Tập

- **Kiến Trúc Cloud**: Trải nghiệm thực tế với AWS services và serverless computing
- **Phát Triển IoT**: Hiểu biết về tích hợp thiết bị IoT và phát triển firmware
- **Full-Stack Development**: Trải nghiệm complete software development lifecycle
- **Quản Lý Dự Án**: Kinh nghiệm thực tế trong agile development và team collaboration

### 8.3 Ứng Dụng Tương Lai

- **Quản Lý Smart Home**: Giám sát môi trường cho nhà ở thông minh
- **IoT Thương Mại**: Hệ thống giám sát thiết bị và predictive maintenance
- **Healthcare Monitoring**: Tracking môi trường bệnh nhân và thiết bị y tế
- **Giám Sát Môi Trường**: Mạng giám sát chất lượng không khí và khí hậu

---

## 9. Kết Luận

Dự án Hệ Thống Giám Sát & Cảnh Báo An Toàn IoT này thể hiện cách tiếp cận toàn diện đến phát triển IoT hiện đại, *kết hợp thiết kế hardware tiên tiến,* giao thức bảo mật mạnh mẽ, và kiến trúc cloud có khả năng mở rộng. Với ngân sách $100 và timeline 3 tháng, đội ngũ 5 sinh viên tận tụy sẽ giao một production-ready prototype thể hiện best practices trong IoT security, cloud computing, và full-stack development.

Dự án không chỉ phục vụ như một trải nghiệm học tập xuất sắc mà còn tạo ra nền tảng cho các ứng dụng thực tế trong smart home, giám sát công nghiệp, và bảo vệ môi trường. Bằng cách tận dụng AWS managed services và tập trung vào nguyên tắc thiết kế security-first, chúng tôi hướng đến tạo ra một hệ thống đáp ứng cả nhu cầu hiện tại và yêu cầu scalability tương lai.

**Thông Tin Liên Hệ Dự Án:**

- **Project Manager**: Trần Quang Huy  
- **Security Lead**: Trần Quang Huy
- **Email**: <huytqse182122@fpt.edu.vn>
- **Project Repository**: <https://github.com/saltless-bruh/D2F_FCJ>

---

*Đề xuất này được gửi để xem xét và phê duyệt. Chúng tôi mong được cơ hội thể hiện khả năng kỹ thuật và giao kết quả xuất sắc trong timeline và ngân sách đề xuất.*

## Tài Liệu Dự Án

{{%attachments title="Tài Liệu Liên Quan" style="blue" /%}}
