---
title : "Introduction"
weight : 1 
chapter : false
pre : " <b> 5.1. </b> "
---

#### Workshop overview

Goal: build a webapp that connects to ESP32 sensor data and sends alerts on incidents.

Stack & services
- Frontend: React (JS/TS) hosted on Amplify, source on GitHub, custom domain via Route 53 (`www.iotsecuredmonitor.click`).
- Auth: Amazon Cognito user pool.
- API: Amazon API Gateway fronting Lambda.
- IoT ingest: AWS IoT Core + IoT Rule → Lambda; data stored in DynamoDB and S3.
- Alerts: Amazon SES email notifications.

Data flow (per architecture)
1) ESP32 sensors publish via Internet Gateway to **IoT Core**.  
2) **IoT Rule** forwards messages.  
3) **Lambda** processes payloads, writes to **DynamoDB/S3**, and triggers **SES** for alerts.  
4) Users access the webapp on **Amplify** via **Route 53**; **Cognito** handles sign-in.  
5) The web UI calls **API Gateway** (backed by Lambda) to read data and status.

Result & notes
- Live site: `https://www.iotsecuredmonitor.click`.  
- Delivered end-to-end IoT → cloud → web experience; initial challenges were learning AWS services under budget constraints but achieved a working pipeline and alerts.
