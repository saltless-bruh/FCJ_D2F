---
title: "Triển khai với Amplify"
weight: 8
chapter: false
pre: " <b> 5.7. </b> "
---

#### Tổng quan
Kết nối repo và deploy frontend bằng AWS Amplify.

### Các bước

1) Mở **Amplify Console** → **New app** → **Host web app**  
   ![Amplify](/5-Workshop/5.7-Amplify-img/amplify1.jpg)

2) **Kết nối repository & branch** (ví dụ GitHub)  
   ![Amplify](/5-Workshop/5.7-Amplify-img/amplify2.jpg)

3) **Authorize** và chọn **branch** cần deploy  
   ![Amplify](/5-Workshop/5.7-Amplify-img/amplify3.jpg)

4) Xem lại **build settings** (amplify.yml) → giữ mặc định hoặc chỉnh khi cần  
   ![Amplify](/5-Workshop/5.7-Amplify-img/amplify4.jpg)

5) Nhấn **Save and deploy** để chạy pipeline  
   ![Amplify](/5-Workshop/5.7-Amplify-img/amplify5.jpg)

6) Chờ build + deploy hoàn tất → trạng thái **Deployed**  
   ![Amplify](/5-Workshop/5.7-Amplify-img/amplify6.jpg)

7) Mở **live URL** để kiểm tra ứng dụng  
   ![Amplify](/5-Workshop/5.7-Amplify-img/amplify7.jpg)

