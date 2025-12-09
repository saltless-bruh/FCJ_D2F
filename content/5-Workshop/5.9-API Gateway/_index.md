---
title: "Create API with API Gateway"
weight: 10
chapter: false
pre: " <b> 5.9. </b> "
---

#### Overview
Create an HTTP API, integrate backend, and deploy.

### Steps

1) Open **API Gateway** → **Create API** → choose **HTTP API**  
   ![API](/5-Workshop/5.9-API%20Gateway-img/API1.jpg)

2) Name the API, add a **route** and **method** (e.g., GET /items)  
   ![API](/5-Workshop/5.9-API%20Gateway-img/API2.jpg)

3) Choose **Integration** (e.g., Lambda/HTTP endpoint), select target  
   ![API](/5-Workshop/5.9-API%20Gateway-img/API3.jpg)

4) Confirm route + integration mapping  
   ![API](/5-Workshop/5.9-API%20Gateway-img/API4.jpg)

5) Create **Stage** (e.g., prod) and **Deploy**  
   ![API](/5-Workshop/5.9-API%20Gateway-img/API5.jpg)

6) View **Invoke URL** and test the endpoint  
   ![API](/5-Workshop/5.9-API%20Gateway-img/API6.jpg)

7) (Optional) Add **CORS**, auth, or throttling as needed  
   ![API](/5-Workshop/5.9-API%20Gateway-img/API7.jpg)

8) Test with a client (browser/cURL/Postman)  
   ![API](/5-Workshop/5.9-API%20Gateway-img/API8.jpg)

