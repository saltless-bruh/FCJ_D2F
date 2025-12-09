---
title: "Xây dựng Lambda Function"
weight: 11
chapter: false
pre: " <b> 5.10. </b> "
---

#### Tổng quan
Tạo và kiểm thử hàm AWS Lambda cho logic backend.

### Các bước

1) Trong **Lambda Console** → **Create function** → **Author from scratch**  
   ![Lambda](/5-Workshop/5.10-Lambda-img/lambda1.jpg)

2) Đặt tên, chọn **Runtime** (Node.js/Python...), giữ quyền mặc định hoặc chọn execution role  
   ![Lambda](/5-Workshop/5.10-Lambda-img/lambda2.jpg)

3) Thêm/chỉnh **handler code** trong editor  
   ![Lambda](/5-Workshop/5.10-Lambda-img/lambda3.jpg)

4) Nhấn **Deploy** để publish mã mới nhất  
   ![Lambda](/5-Workshop/5.10-Lambda-img/lambda4.jpg)

5) Tạo **Test event** và chạy **Test** để kiểm tra kết quả  
   ![Lambda](/5-Workshop/5.10-Lambda-img/lambda5.jpg)

