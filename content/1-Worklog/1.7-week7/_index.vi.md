---
title: "Nhật Ký Tuần 7"
date: 2025-10-20
weight: 7
chapter: false
pre: " <b> 1.7 </b> "
---

#### NHẬT KÝ TUẦN 7

{{% notice note %}}
Nhật ký này ghi lại công việc thực tế đã hoàn thành trong Tuần 7 của chương trình thực tập.
{{% /notice %}}

### Mục tiêu Tuần 7

- Triển khai phát hiện mối đe dọa với AWS IoT Device Defender
- Xây dựng cơ chế thực thi chính sách
- Phát triển pipeline xử lý sự kiện với Kinesis

### Các nhiệm vụ thực hiện trong tuần này

| STT | Mô tả Nhiệm vụ                                                                                                                                            | Ngày Bắt đầu | Ngày Kết thúc | Tham khảo                                                          |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------------- | ------------------------------------------------------------------ |
| 1   | Cấu hình AWS IoT Device Defender - Thiết lập security profiles - Định nghĩa behavior baselines - Cấu hình audit checks                                    | 20/10/2025   | 21/10/2025    | [IoT Device Defender](https://aws.amazon.com/iot-device-defender/) |
| 2   | Triển khai thực thi chính sách bảo mật - Tạo IoT policies cho device groups - Triển khai certificate-based authentication - Thiết lập authorization rules | 22/10/2025   | 23/10/2025    | Security Policies                                                  |
| 3   | Hoàn thành CloudWatch và monitoring lab - Thiết lập dashboards cho security metrics - Cấu hình alarms cho anomalies - Triển khai log aggregation          | 24/10/2025   | 25/10/2025    | [CloudWatch](https://aws.amazon.com/cloudwatch/)                   |
| 4   | Xây dựng event processing pipeline với Kinesis - Cấu hình Kinesis Data Streams - Triển khai Lambda consumers - Thiết lập data transformation              | 25/10/2025   | 26/10/2025    | [Kinesis](https://aws.amazon.com/kinesis/)                         |

### Thành tựu Tuần 7

- **IoT Device Defender được cấu hình** với security profiles và behavior baselines

- **Thực thi chính sách được triển khai** với certificate-based authentication và authorization

- **CloudWatch monitoring được thiết lập** với security dashboards và anomaly alarms

- **Event processing pipeline hoạt động** sử dụng Kinesis cho phát hiện mối đe dọa thời gian thực
