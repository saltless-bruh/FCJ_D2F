---
title : "Connect IoT Core With DynamoDB"
weight : 3
chapter : false
pre : " <b> 5.3. </b> "
---

#### Using IoT Rule

In this section, you will create **Table** 

![overview](/images/5-Workshop/5.3-S3-vpc/DBIOT1.jpeg)

+ Choose **Create Rule**

![overview](/images/5-Workshop/5.3-S3-vpc/DBIOT2.jpeg)
+ Name the **Rule**
+ Choose **Next**


![overview](/images/5-Workshop/5.3-S3-vpc/DBIOT3.jpeg)
+ Write the SQL Query **SELECT * FROM 'esp32/pub'**

![overview](/images/5-Workshop/5.3-S3-vpc/DBIOT4.jpeg)
+ Choose **DynamoDB in Action 1**
+ Create **DynamoDB Table**

![overview](/images/5-Workshop/5.3-S3-vpc/DBIOT5.jpeg)
+ Choose **Create Table**
![overview](/images/5-Workshop/5.3-S3-vpc/DBIOT6.jpeg)

![overview](/images/5-Workshop/5.3-S3-vpc/DBIOT7.jpeg)
+ Choose **Keys like table details**

![overview](/images/5-Workshop/5.3-S3-vpc/DBIOT8.jpeg)
+ Choose **Create New Rule**

![overview](/images/5-Workshop/5.3-S3-vpc/DBIOT9.jpeg)
+ **Naming** Then **Create**


![overview](/images/5-Workshop/5.3-S3-vpc/DBIOT10.jpeg)
+ Choose **Next**
![overview](/images/5-Workshop/5.3-S3-vpc/DBIOT11.jpeg)
+ Choose **Explore Item**
![overview](/images/5-Workshop/5.3-S3-vpc/DBIOT12.jpeg)


#### Using DynamoDB
#### Content

- [Create gateway endpoint](3.1-create-gwe/)
- [Test gateway endpoint](3.2-test-gwe/)
