---
title: "Workshop"
weight: 5
chapter: false
pre: " <b> 5. </b> "
---
# IoT Security Workshop

#### Overview
- Build a webapp connected to ESP32 sensor data with incident alerts.
- Stack: React (JS/TS) on Amplify + Route 53, Cognito auth, API Gateway + Lambda backend.
- IoT ingest: AWS IoT Core + Rule → Lambda, storing to DynamoDB/S3; SES for email alerts.
- Live site: `https://www.iotsecuredmonitor.click`.

#### Content
1. [Workshop overview](5.1-Workshop-overview/)
2. [Prerequiste](5.2-Prerequiste/)
3. [Connect IoT Core with DynamoDB](5.3-S3-Iot%20core/)
4. [Using SES](5.4-SES/)
5. [Using Route 53](5.5-Route53/)
6. [Using S3](5.6-S3/)
7. [Deploy with Amplify](5.7-Amplify/)
8. [Configure Cognito](5.8-Cognito/)
9. [Create API with API Gateway](5.9-API%20Gateway/)
10. [Build Lambda Function](5.10-Lambda/)
