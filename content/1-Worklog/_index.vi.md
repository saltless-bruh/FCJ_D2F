---
title: "Nhật Ký Làm Việc"
date: 2025-10-11
weight: 1
chapter: false
---

pre: "{{< b >}}1.{{< /b >}}"

------

**Session Manager** là một chức năng nằm trong dịch vụ System Manager của AWS, Session Manager cung cấp khả năng quản lý các máy chủ một cách an toàn mà **không cần mở port SSH, không cần Bastion Host hoặc quản lý SSH key**.

Phần này chứa các hoạt động làm việc hàng ngày của tôi trong thời gian thực tập từ 12/08/2025 đến 12/11/2025. Mỗi mục bao gồm:Session Manager cũng giúp dễ dàng tuân thủ các chính sách của công ty yêu cầu quyền truy cập có kiểm soát, đảm bảo việc bảo mật nghiêm ngặt và ghi log truy việc truy cập trong khi vẫn cung cấp cho người dùng cuối quyền truy cập đa nền tảng.

- NgàyVới việc sử dụng Session Manager, bạn sẽ có được những ưu điểm sau:

- Các công việc đã hoàn thành

- Kỹ năng đã học được- Không cần phải mở cổng 22 cho giao thức SSH.

- Thách thức gặp phải- Có thể cấu hình để kết nối không cần đi ra ngoài internet.

- Giải pháp đã thực hiện- Không cần quản lý private key của server để kết nối SSH.

- Ghi chú và quan sát- Quản lý tập trung được user bằng việc sử dụng AWS IAM.

- Truy cập tới server một cách dễ dàng và đơn giản bằng một cú click chuột.

## Các Mục Hàng Ngày- Thời gian truy cập nhanh chóng hơn các phương thức truyền thống như SSH

- Hỗ trợ nhiều hệ điều hành khác nhau như Linux, Windows, MacOS.

[Nhấn vào đây để xem chi tiết nhật ký làm việc]- Log lại được các phiên kết nối và các câu lệnh đã thực thi trong lúc kết nối tới server.

Lưu ý: Vui lòng cập nhật phần này thường xuyên với các hoạt động và trải nghiệm học tập hàng ngày của bạn.Với những ưu điểm trên, bạn có thể sử dụng Session Manager thay vì sử dụng kỹ thuật Bastion host giúp chúng ta tiết kiệm được thời gian và chi phí khi quản lý server Bastion.
