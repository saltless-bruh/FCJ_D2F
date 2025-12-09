---
title : "Kết nối IoT Core với DynamoDB"
weight : 3
chapter : false
pre : " <b> 5.3. </b> "
---

#### Sử dụng IoT Rule

Trong phần này, bạn sẽ tạo **Table**

![overview](/images/5-Workshop/5.3-S3-vpc/DBIOT1.jpeg)

+ Chọn **Create Rule**

![overview](/images/5-Workshop/5.3-S3-vpc/DBIOT2.jpeg)

+ Đặt tên cho **Rule**
+ Chọn **Next**

![overview](/images/5-Workshop/5.3-S3-vpc/DBIOT3.jpeg)

+ Viết câu truy vấn SQL **SELECT * FROM 'esp32/pub'**

![overview](/images/5-Workshop/5.3-S3-vpc/DBIOT4.jpeg)

+ Chọn **DynamoDB trong Action 1**
+ Tạo **DynamoDB Table**

![overview](/images/5-Workshop/5.3-S3-vpc/DBIOT5.jpeg)

+ Chọn **Create Table**
![overview](/images/5-Workshop/5.3-S3-vpc/DBIOT6.jpeg)

![overview](/images/5-Workshop/5.3-S3-vpc/DBIOT7.jpeg)

+ Chọn **Keys như chi tiết bảng**

![overview](/images/5-Workshop/5.3-S3-vpc/DBIOT8.jpeg)

+ Chọn **Create New Rule**

![overview](/images/5-Workshop/5.3-S3-vpc/DBIOT9.jpeg)

+ **Đặt tên** sau đó **Create**

![overview](/images/5-Workshop/5.3-S3-vpc/DBIOT10.jpeg)

+ Chọn **Next**
![overview](/images/5-Workshop/5.3-S3-vpc/DBIOT11.jpeg)
+ Chọn **Explore Item**
![overview](/images/5-Workshop/5.3-S3-vpc/DBIOT12.jpeg)
