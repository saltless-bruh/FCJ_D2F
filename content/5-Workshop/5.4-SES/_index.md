---
title: "Using SES"
weight: 4
chapter: false
pre: " <b> 5.4. </b> "
---

#### Overview

In this section, you will learn how to use **Amazon Simple Email Service (SES)** to send emails from your application or backend environment. SES is a fully managed email platform that supports transactional messages, notifications, and marketing campaigns. You will verify your email identity or domain, configure basic settings, and understand how SES processes and delivers messages.

---

## Why using Amazon SES

Amazon SES is commonly used in cloud-based applications due to its reliability, cost efficiency, and ease of integration.

- **High deliverability:** SES uses trusted Amazon mail servers and supports SPF, DKIM, and DMARC to reduce spam filtering.
- **Flexible integration:** Send emails via SES API, AWS SDK, SMTP interface, or Lambda.
- **Scalable and cost-effective:** Suitable for workloads from small to large scale, costing only $0.10 per 1,000 emails.
- **Built-in monitoring:** Track bounces, complaints, and deliveries using SNS and CloudWatch.
- **Secure and controlled:** Manage permissions with IAM policies and restrict allowed sending identities.

---

## SES Architecture

Amazon SES architecture is built around three core components that define how emails are authenticated, transmitted, and monitored.

### 1. Verified Identities

Before sending messages, SES requires verification of your sending domain or email address.  
This prevents unauthorized use and ensures SES can send emails on your behalf.

Verification usually requires DNS records:

- **SPF (TXT)** — verifies the sender
- **DKIM (CNAME)** — provides cryptographic signing
- **DMARC (TXT, optional)** — adds domain-level protection

---

### 2. Email Sending Workflow

Once verification is complete, your application can send messages using the SES API, AWS SDKs, or SMTP.

High-level workflow:
SES automatically handles email routing, retries, throttling, and formatting.

### 3. How to do it

Press **Get Started**

Fill in your **Email**
Press **Next**

## Step-by-Step Implementation Guide

### Part 1: Access Amazon SES Console

1. Sign in to **AWS Management Console**
2. Navigate to **Amazon SES** service
3. Select your preferred region (e.g., **ap-southeast-1**)
4. Click **Get Started** button

---

### Part 2: Create Email Identity

**Step 1:** Choose Identity Type

- Navigate to **Verified identities** in left sidebar
- Click **Create identity**
  ![Create Identity](/5-Workshop/5.4-SES-img/SES-B1.png)
- Choose between:
  - **Email address** - Quick setup, good for testing
  - **Domain** - Production use, more flexible

**Step 2:** For Email Address Verification

1. Select **Email address** option
2. Enter your email address (e.g., `your-email@gmail.com`)
3. Click **Create identity**
   ![Create Identity](/5-Workshop/5.4-SES-img/SES-B2.png)
   **Step 3:** Verify Your Email

4. Check your inbox for verification email from AWS
5. Subject: "Amazon Web Services – Email Address Verification Request"
6. Click the verification link in email
7. Return to SES console
8. Refresh the page - Status should show **Verified**
   ![Create Identity](/5-Workshop/5.4-SES-img/SES-B3.png)

---

### Part 3: Verify Domain (Optional - Recommended for Production)

**Step 1:** Create Domain Identity

1. Click **Create identity**
2. Select **Domain** option
3. Enter your domain name (e.g., `iotsecuredmonitor.click`)
4. Check **Use a custom MAIL FROM domain** (optional)
   ![Domain Verification](/5-Workshop/5.4-SES-img/SES-P3B1.png)
5. Click **Create identity**
   ![Domain Verification](/5-Workshop/5.4-SES-img/SES-P3B1.1.png)
   **Step 2:** Get DNS Records

6. After creating, click **Get DNS records** button
7. You will see 3 types of records:

**DKIM Records (3 CNAME records):**

**SPF Record (TXT record):**

**DMARC Record (TXT record - optional):**

![Domain Verification](/5-Workshop/5.4-SES-img/SES-P3B2.png)

### Part 4: Send Test Email

**Step 1:** Navigate to Test Email

1. Go to Verified identities
2. Select your verified email or domain
3. Click Send test email button
   ![Send Test Email](/5-Workshop/5.4-SES-img/SES-P4B1.png)

**Step 2:** Configure Test Email

1. Email format scenario:

- Formatted - Simple HTML/text email
- Raw - Full MIME message
- Custom - Custom headers
- Templated - Use email template

2. From address: Your verified email

3. To address: Recipient email

- Note: In Sandbox mode, recipient must also be verified

4. Subject: Enter email subject

5. Body:

- Text: Plain text version
- HTML: HTML formatted version

![Send Test Email](/5-Workshop/5.4-SES-img/SES-P4B2.png)

**Step 3:** Send Email

1. Click Send test email
2. Check recipient inbox
3. Verify email delivery

### Part 5: Configure Email Monitoring

Email Monitoring

**Step 1:** Create Configuration Set

1. Go to Configuration sets
2. Click Create set
   ![Email Monitoring](/5-Workshop/5.4-SES-img/SES-P5B1.png)
3. Enter name: production-emails
4. Click Create
   ![Email Monitoring](/5-Workshop/5.4-SES-img/SES-P5B1.1.png)
   ![Email Monitoring](/5-Workshop/5.4-SES-img/SES-P5B1.2.png)

**Step 2:** Add Event Destination

1. Select your configuration set
2. Click Add destination
   ![Email Monitoring](/5-Workshop/5.4-SES-img/SES-P5B2.png)
3. Choose destination type:
   ![Email Monitoring](/5-Workshop/5.4-SES-img/SES-P5B2.1.png)
   ![Email Monitoring](/5-Workshop/5.4-SES-img/SES-P5B2.2.png)
   ![Email Monitoring](/5-Workshop/5.4-SES-img/SES-P5B2.3.png)

**Step 3:** Enable Reputation Metrics

1. In configuration set settings
2. Enable Reputation metrics
   ![Email Monitoring](/5-Workshop/5.4-SES-img/SES-P5B3.png)
   ![Email Monitoring](/5-Workshop/5.4-SES-img/SES-P5B3.1.png)
