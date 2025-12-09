---
title: "Using Route 53"
weight: 5
chapter: false
pre: " <b> 5.5. </b> "
---

#### Overview

In this section, you will learn how to use **Amazon Route 53** to manage DNS for your IoT temperature and humidity monitoring project. Route 53 will help you configure a custom domain for your web application, set up DNS records for email service (SES), and create subdomains for different components of your IoT system.

---

## What is Amazon Route 53?

**Amazon Route 53** is a highly available and scalable Domain Name System (DNS) web service designed to route end users to your application by translating domain names into IP addresses.

### Key Features:

- **Domain Registration** - Register new domain names directly through AWS
- **DNS Management** - Create and manage DNS records (A, CNAME, TXT, MX, etc.)
- **Health Checks** - Monitor endpoint health and route traffic accordingly
- **Traffic Routing** - Intelligent routing based on latency, geography, or weighted policies
- **Integration with AWS** - Seamlessly works with EC2, S3, CloudFront, Load Balancers, etc.

---

## Why Use Route 53 for IoT Project?

For your IoT temperature and humidity monitoring system, Route 53 provides:

✅ **Custom Domain** - Professional URL like `iotmonitor.click` instead of CloudFront/S3 URLs  
✅ **API Endpoint** - Clean API subdomain `api.iotmonitor.click` for API Gateway  
✅ **MQTT Endpoint** - Custom endpoint for IoT devices connection  
✅ **SSL/TLS Certificates** - Required DNS validation for HTTPS  
✅ **High Availability** - 100% uptime SLA, redundant DNS servers worldwide  
✅ **Serverless Integration** - Works seamlessly with S3, CloudFront, API Gateway, Lambda

---

## Step-by-Step Implementation Guide

### Part 1: Access Amazon Route 53 Console

1. Sign in to **AWS Management Console**
2. In the search bar, type **Route 53**
3. Click on **Route 53** service
4. You'll see the Route 53 dashboard

## ![Access Amazon Route 53](/5-Workshop/5.5-R53-img/R53-P1B1.png)

---

### Part 2: Create Hosted Zone

For this workshop, we assume you already own a domain from a registrar (GoDaddy, Namecheap, Cloudflare, etc.). We'll create a hosted zone in Route 53 to manage DNS records.

**Note:** Domain registration through Route 53 is not covered in AWS Free Tier. You can use an existing domain or purchase one from external registrars starting at $1-3/year.

## ![Create Hosted Zone](/5-Workshop/5.5-R53-img/R53-P2B1.png)

**Step 1:** Create Hosted Zone

1. Click **Hosted zones** in left sidebar
2. Click **Create hosted zone** button

## ![Create Hosted Zone](/5-Workshop/5.5-R53-img/R53-P2B2.png)

**Step 2:** Configure Hosted Zone

1. **Domain name:** Enter your domain (e.g., `iotmonitor.click`)
2. **Description:** Optional description (e.g., "IoT Monitoring System DNS")
3. **Type:**
   - ✅ **Public hosted zone** (for internet-accessible domains)
   - ⚪ Private hosted zone (for VPC-internal DNS)
4. **Tags:** Optional (e.g., `Project: IoT-Monitor`)
5. Click **Create hosted zone**

## ![Create Hosted Zone](/5-Workshop/5.5-R53-img/R53-P2B3.png)

**Step 3:** Note Name Servers
After creation, you'll see 4 NS (Name Server) records:

```
ns-123.awsdns-12.com
ns-456.awsdns-34.net
ns-789.awsdns-56.org
ns-012.awsdns-78.co.uk
```

**Step 4:** Update Name Servers at Domain Registrar
Go to your domain registrar (GoDaddy, Namecheap, etc.) and:

1. Login to your account
2. Find **DNS Management** or **Name Servers**
3. Change to **Custom Name Servers**
4. Add all 4 Route 53 name servers
5. Save changes

**Wait 24-48 hours for DNS propagation**

**Verify name servers changed:**

```bash
nslookup -type=NS iotmonitor.click
```

---

### Part 3: Create DNS Records for IoT Application

---

#### 3.1: Create A Record for Main Website (CloudFront Distribution)

**Step 1:** Create Record

1. Select your hosted zone
2. Click **Create record**

**Step 2:** Configure A Record (Alias) for CloudFront

```
Record name: [leave empty for root domain]
Record type: A - IPv4 address
Alias: Yes
Alias target: CloudFront distribution
  - Select "Alias to CloudFront distribution"
  - Choose your CloudFront distribution from dropdown
  - Example: d123abc456def.cloudfront.net
Routing policy: Simple routing
```

![Create Record](/5-Workshop/5.5-R53-img/R53-P3B1.png)

---

#### 3.2: Create A Record for API Subdomain (API Gateway)

**Step 1:** Create Record

1. Click **Create record**

**Step 2:** Configure A Record (Alias) for API Gateway

```
Record name: api
Record type: A - IPv4 address
Alias: Yes
Alias target: API Gateway API
  - Select "Alias to API Gateway API"
  - Region: us-east-1 (or your region)
  - Select your API Gateway endpoint from dropdown
  - Example: abc123xyz.execute-api.us-east-1.amazonaws.com
Routing policy: Simple routing
```

![Create Record](/5-Workshop/5.5-R53-img/R53-P3B1.png)

---

## Additional Resources

- **AWS Route 53 Documentation:** https://docs.aws.amazon.com/route53/
- **DNS Record Types:** https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/ResourceRecordTypes.html
- **SES Domain Verification:** https://docs.aws.amazon.com/ses/latest/dg/verify-domain-procedure.html
- **Route 53 Pricing:** https://aws.amazon.com/route53/pricing/
- **DNS Propagation Checker:** https://dnschecker.org
- **DMARC Guide:** https://dmarc.org/overview/

---

## Conclusion

Congratulations! You have successfully configured Amazon Route 53 for your IoT temperature and humidity monitoring project.
