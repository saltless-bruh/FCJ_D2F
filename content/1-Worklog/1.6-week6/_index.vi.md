---
title: "Nhật Ký Tuần 6"
date: 2025-10-13
weight: 6
chapter: false
pre: " <b> 1.6 </b> "
---

#### NHẬT KÝ TUẦN 6

{{% notice note %}}
Nhật ký này ghi lại công việc thực tế đã hoàn thành trong Tuần 6 của chương trình thực tập.
{{% /notice %}}

### Mục tiêu Tuần 6

- Triển khai tự động hóa vòng đời chứng chỉ với Lambda
- Tích hợp CloudHSM cho quản lý key bảo mật
- Thiết lập CRL và OCSP endpoints cho xác thực chứng chỉ

### Các nhiệm vụ thực hiện trong tuần này

| STT | Mô tả Nhiệm vụ                                                                                                                                                      | Ngày Bắt đầu | Ngày Kết thúc | Tham khảo                                                    |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------------- | ------------------------------------------------------------ |
| 1   | Phát triển Lambda functions cho tự động hóa chứng chỉ - Triển khai quy trình phát hành chứng chỉ - Xây dựng logic gia hạn tự động - Tạo revocation handler          | 13/10/2025   | 15/10/2025    | [Lambda Functions](https://github.com/)                      |
| 2   | Triển khai EventBridge rules cho tự động hóa vòng đời - Lập lịch kiểm tra chứng chỉ hết hạn (7/30 ngày trước) - Kích hoạt quy trình gia hạn - Gửi thông báo hết hạn | 16/10/2025   | 17/10/2025    | [EventBridge](https://aws.amazon.com/eventbridge/)           |
| 3   | Hoàn thành AWS security services lab - CloudHSM cho lưu trữ key - KMS cho encryption keys - Secrets Manager cho credentials                                         | 18/10/2025   | 18/10/2025    | [AWS Security Labs](https://cloudjourney.awsstudygroup.com/) |
| 4   | Thiết lập certificate validation endpoints - Cấu hình CRL distribution point - Triển khai OCSP responder - Kiểm tra certificate revocation checking                 | 19/10/2025   | 19/10/2025    | Certificate Validation                                       |

### Thành tựu Tuần 6

- **Tự động hóa chứng chỉ được triển khai** với Lambda cho phát hành, gia hạn và thu hồi

- **EventBridge scheduling được cấu hình** cho quản lý vòng đời chứng chỉ chủ động

- **CloudHSM được tích hợp** cho lưu trữ private key bảo mật

- **Certificate validation endpoints hoạt động** với CRL và OCSP cho kiểm tra thu hồi thời gian thực
