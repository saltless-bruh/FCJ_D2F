---
title: "Sử dụng S3"
weight: 7
chapter: false
pre: " <b> 5.7. </b> "
---

#### Amazon S3 (Simple Storage Service)

**Amazon S3** là dịch vụ lưu trữ đối tượng cung cấp khả năng mở rộng hàng đầu, tính sẵn sàng cao, bảo mật và hiệu suất tốt. Bạn có thể sử dụng Amazon S3 để lưu trữ và truy xuất bất kỳ lượng dữ liệu nào, bất cứ lúc nào, từ bất kỳ đâu.

#### Nội dung học

Trong phần này, bạn sẽ học cách:

- Tạo S3 bucket
- Tải lên và quản lý objects
- Cấu hình quyền truy cập bucket
- Bật versioning và lifecycle policies
- Thiết lập static website hosting
- Triển khai các phương pháp bảo mật tốt nhất

#### Các khái niệm chính

**S3 Bucket**: Là container để lưu trữ objects trong Amazon S3. Mỗi bucket có tên duy nhất trên toàn cầu.

**Objects**: Các file được lưu trữ trong S3, bao gồm dữ liệu và metadata. Mỗi object được xác định bởi một key duy nhất trong bucket.

**Storage Classes**: Các lựa chọn khác nhau để lưu trữ dữ liệu dựa trên mô hình truy cập:

- S3 Standard: Truy cập thường xuyên
- S3 Intelligent-Tiering: Tối ưu chi phí tự động
- S3 Standard-IA: Truy cập không thường xuyên
- S3 Glacier: Lưu trữ dài hạn

#### Tạo S3 Bucket

1. **Truy cập S3 Console**

   - Mở AWS Management Console
   - Tìm kiếm "S3" và nhấp vào dịch vụ S3
     ![Tạo S3 Bucket](/5-Workshop/5.6-S3-img/S3-P1B1.png)

2. **Tạo Bucket mới**

   - Nhấp **Create bucket**
     ![Tạo S3 Bucket](/5-Workshop/5.6-S3-img/S3-P1B2.png)
   - Nhập tên bucket duy nhất (phải là duy nhất trên toàn cầu)
   - Chọn AWS Region
   - Cấu hình các thiết lập bổ sung:
     - Object Ownership
     - Block Public Access settings (giữ nguyên mặc định)
     - Bucket Versioning
     - Encryption
       ![Tạo S3 Bucket](/5-Workshop/5.6-S3-img/S3-P1B3.png)

3. **Nhấp Create Bucket**
   ![Tạo S3 Bucket](/5-Workshop/5.6-S3-img/S3-P1B4.png)

#### Tải Objects lên S3

1. **Chọn Bucket của bạn**

   - Nhấp vào tên bucket từ danh sách
     ![Tải Objects lên S3](/5-Workshop/5.6-S3-img/S3-P2B1.png)

2. **Tải File lên**

   - Nhấp **Upload**
     ![Tải Objects lên S3](/5-Workshop/5.6-S3-img/S3-P2B2.png)
   - Nhấp **Add files** hoặc kéo thả files
   - Cấu hình permissions và properties
   - Nhấp **Upload**
     ![Tải Objects lên S3](/5-Workshop/5.6-S3-img/S3-P2B3.png)

3. **Xem Chi tiết Object**
   - Nhấp vào tên object để xem properties
   - Sao chép object URL để truy cập
     ![Tải Objects lên S3](/5-Workshop/5.6-S3-img/S3-P2B4.png)

#### Cấu hình Quyền truy cập Bucket

##### Sử dụng Bucket Policies

Bucket policies là ngôn ngữ chính sách truy cập dựa trên JSON để quản lý quyền.

Ví dụ policy cho phép public read access:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::ten-bucket-cua-ban/*"
    }
  ]
}
```

##### Sử dụng Access Control Lists (ACLs)

- Thiết lập permissions ở cấp bucket hoặc object
- Cấp quyền truy cập cho các AWS accounts cụ thể

#### Bật Versioning

Versioning giữ nhiều phiên bản của một object trong cùng một bucket.

1. Vào **Properties** của bucket
2. Tìm **Bucket Versioning**
3. Nhấp **Edit**
4. Chọn **Enable**
5. Nhấp **Save changes**
   ![Bật Versioning](/5-Workshop/5.6-S3-img/S3-P4B1.png)
   ![Bật Versioning](/5-Workshop/5.6-S3-img/S3-P4B1.1.png)

Lợi ích:

- Khôi phục từ các lỗi xóa nhầm
- Truy xuất các phiên bản trước đó
- Duy trì lịch sử backup

#### Thiết lập Lifecycle Policies

Tự động chuyển đổi objects giữa các storage classes hoặc xóa chúng.

1. Vào tab **Management**
2. Nhấp **Create lifecycle rule**
3. Cấu hình:
   - Tên rule
   - Phạm vi rule (toàn bộ bucket hoặc lọc theo prefix/tags)
   - Các hành động lifecycle:
     - Chuyển đổi sang storage classes khác
     - Hết hạn objects sau số ngày chỉ định
     - Xóa multipart uploads chưa hoàn thành

#### Static Website Hosting

Host một website tĩnh sử dụng S3:

1. Vào tab **Properties**
2. Tìm **Static website hosting**
3. Nhấp **Edit**
4. Chọn **Enable**
5. Cấu hình:
   - Index document (vd: index.html)
   - Error document (vd: error.html)
6. Nhấp **Save changes**

Website endpoint của bạn sẽ là: `http://ten-bucket.s3-website-region.amazonaws.com`

#### Bước tiếp theo

Sau khi hoàn thành phần này, bạn sẽ có thể:

- Tạo và cấu hình S3 buckets
- Tải lên và quản lý objects hiệu quả
- Triển khai các phương pháp bảo mật tốt nhất
- Tối ưu chi phí sử dụng lifecycle policies
- Sử dụng S3 cho các ứng dụng thực tế khác nhau
