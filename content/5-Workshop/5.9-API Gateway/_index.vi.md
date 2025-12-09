---
title: "Tạo API với API Gateway"
weight: 10
chapter: false
pre: " <b> 5.9. </b> "
---

#### Tổng quan

Tạo HTTP API, gắn backend và deploy.

### Các bước

1) Mở **API Gateway** → **Create API** → chọn **HTTP API**  
   ![API](/images/5-Workshop/5.9-API%20Gateway-img/API1.jpg)

2) Đặt tên API, thêm **route + method** (ví dụ GET /items)  
   ![API](/images/5-Workshop/5.9-API%20Gateway-img/API2.jpg)

3) Chọn **Integration** (Lambda/HTTP endpoint), chọn đích  
   ![API](/images/5-Workshop/5.9-API%20Gateway-img/API3.jpg)

4) Xác nhận map route ↔ integration  
   ![API](/images/5-Workshop/5.9-API%20Gateway-img/API4.jpg)

5) Tạo **Stage** (vd: prod) và **Deploy**  
   ![API](/images/5-Workshop/5.9-API%20Gateway-img/API5.jpg)

6) Lấy **Invoke URL** và test endpoint  
   ![API](/images/5-Workshop/5.9-API%20Gateway-img/API6.jpg)

7) (Tùy chọn) Bật **CORS**, auth, throttling nếu cần  
   ![API](/images/5-Workshop/5.9-API%20Gateway-img/API7.jpg)

8) Test bằng client (browser/cURL/Postman)  
<<<<<<< HEAD
   ![API](/images/5-Workshop/5.9-API%20Gateway-img/API8.jpg)
=======
   ![API](/5-Workshop/5.9-API%20Gateway-img/API8.jpg)
>>>>>>> 0ac3103672ff8af68eb80253b652e32a5ea0f43a
