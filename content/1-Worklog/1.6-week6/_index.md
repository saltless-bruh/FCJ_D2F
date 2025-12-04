---
title: "Week 6 Worklog"
date: 2025-10-13
weight: 6
chapter: false
pre: " <b> 1.6 </b> "
---

#### WEEK 6 WORKLOG

⚠️ **Note**: This worklog documents actual work completed during Week 6 of the internship program.

### Week 6 Objectives

- Implement certificate lifecycle automation with Lambda
- Integrate CloudHSM for secure key management
- Set up CRL and OCSP endpoints for certificate validation

### Tasks Performed This Week

| No. | Task Description | Start Date | End Date | Reference |
|-----|------------------|------------|----------|-----------|
| 1 | Develop Lambda functions for certificate automation - Implement certificate issuance workflow - Build automatic renewal logic - Create revocation handler | 13/10/2025 | 15/10/2025 | [Lambda Functions](https://github.com/) |
| 2 | Implement EventBridge rules for lifecycle automation - Schedule certificate expiry checks (7/30 days before) - Trigger renewal workflows - Send expiry notifications | 16/10/2025 | 17/10/2025 | [EventBridge](https://aws.amazon.com/eventbridge/) |
| 3 | Complete AWS security services lab - CloudHSM for key storage - KMS for encryption keys - Secrets Manager for credentials | 18/10/2025 | 18/10/2025 | [AWS Security Labs](https://cloudjourney.awsstudygroup.com/) |
| 4 | Set up certificate validation endpoints - Configure CRL distribution point - Implement OCSP responder - Test certificate revocation checking | 19/10/2025 | 19/10/2025 | Certificate Validation |

### Week 6 Achievements

- **Certificate automation implemented** with Lambda for issuance, renewal, and revocation

- **EventBridge scheduling configured** for proactive certificate lifecycle management

- **CloudHSM integrated** for secure private key storage

- **Certificate validation endpoints operational** with CRL and OCSP for real-time revocation checking
