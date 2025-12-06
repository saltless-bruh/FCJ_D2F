---
title: "Nhật Ký Tuần 2"
date: 2025-09-15
weight: 2
chapter: false
pre: " <b> 1.2 </b> "
---

#### NHẬT KÝ TUẦN 2

{{% notice note %}}
Nhật ký này ghi lại công việc thực tế đã hoàn thành trong Tuần 2 của chương trình thực tập.
{{% /notice %}}

### Mục tiêu Tuần 2

- Tham dự Vietnam Cloud Day 2025 để học về dịch vụ AWS mới nhất và xu hướng cloud
- Nghiên cứu best practices về quản lý chứng chỉ PKI/TLS
- Tinh chỉnh kiến trúc dự án theo hướng security-first

### Các nhiệm vụ thực hiện trong tuần này

| STT | Mô tả Nhiệm vụ                                                                                                                                                                           | Ngày Bắt đầu | Ngày Kết thúc | Tham khảo                                                                                   |
| --- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------------- | ------------------------------------------------------------------------------------------- |
| 1   | Tham dự Vietnam Cloud Day 2025 - Tìm hiểu dịch vụ bảo mật AWS mới - Networking với chuyên gia AWS - Khám phá use case bảo mật IoT                                                        | 18/09/2025   | 18/09/2025    | [Vietnam Cloud Day](https://vietnamcloudday.vn/)                                            |
| 2   | Nghiên cứu hạ tầng PKI trên AWS - Tìm hiểu ACM Private CA - Đánh giá quản lý chứng chỉ AWS - Khám phá CloudHSM cho lưu trữ key                                                           | 16/09/2025   | 17/09/2025    | [ACM Private CA](https://aws.amazon.com/certificate-manager/private-certificate-authority/) |
| 3   | Tinh chỉnh sơ đồ kiến trúc hệ thống - Định nghĩa phân cấp chứng chỉ (Root/Intermediate/Device CA) - Thiết kế quy trình tự động Lambda - Lên kế hoạch schema DynamoDB cho device registry | 19/09/2025   | 20/09/2025    | Thiết kế Kiến trúc                                                                          |
| 4   | Tài liệu hóa đặc tả kỹ thuật ban đầu - Định nghĩa yêu cầu API - Tạo sơ đồ data flow - Thiết lập roadmap dự án                                                                            | 21/09/2025   | 21/09/2025    | Tài liệu Dự án                                                                              |

### Thành tựu Tuần 2

- **Tham dự Vietnam Cloud Day 2025** và thu được insights về best practices bảo mật AWS IoT

- **Kiến trúc PKI được thiết kế** với phân cấp CA 3 tầng (Root → Intermediate → Device)

- **Đặc tả kỹ thuật được tài liệu hóa** cho quản lý vòng đời chứng chỉ

- **Sơ đồ kiến trúc hoàn thành** thể hiện tự động hóa Lambda, DynamoDB registry và orchestration EventBridge
