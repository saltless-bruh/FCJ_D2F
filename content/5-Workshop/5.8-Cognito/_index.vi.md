---
title: "Cấu hình Cognito"
weight: 9
chapter: false
pre: " <b> 5.8. </b> "
---

#### Tổng quan
Tạo Cognito User Pool và app client để xác thực.

### Các bước

1) Vào **Cognito** → **Create user pool**  
   ![Cognito](/5-Workshop/5.8-Cognito-img/cognito1.jpg)

2) Cấu hình **sign-in options, password policy**, và **MFA** nếu cần  
   ![Cognito](/5-Workshop/5.8-Cognito-img/cognito2.jpg)

3) Tạo **App client** (không dùng secret cho ứng dụng frontend), lưu lại ID  
   ![Cognito](/5-Workshop/5.8-Cognito-img/cognito3.jpg)

4) Thiết lập **Domain** (Cognito-hosted UI), khai báo callback URLs, lưu cấu hình  
   ![Cognito](/5-Workshop/5.8-Cognito-img/cognito4.jpg)

