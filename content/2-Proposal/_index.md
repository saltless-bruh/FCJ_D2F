---
title: "Proposal"
date: 2025-09-30
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

## 1. Project Overview

### Project Title

#### IoT Security Monitoring & Alert System for Smart Home on AWS Cloud Platform

### Project Description

Development of a comprehensive IoT security monitoring and alert system for smart homes, combining hardware sensor integration, advanced security protocols, serverless backend architecture, and real-time dashboard visualization. The system provides end-to-end monitoring capabilities for environmental parameters (temperature, humidity, gas detection, motion) with robust security measures and cloud-based analytics.

### Team Information

- **Team Size**: 5 members (3rd-year university students)
- **Team Composition**:
  - 2 IC Design Engineers (Hardware/Firmware specialists)
  - 2 Software Engineers (Backend/Frontend specialists)  
  - 1 Security Specialist (Cybersecurity & PKI expert)

### Project Duration

**3 months** (September 2025 - November 2025)

### Total Budget

**$100 USD** allocated across two main components:

- WebApp Development: $10
- IoT Hardware & Firmware: $40  

### Project Scale

**Smart Home** - A typical home with 3 sensor nodes covering critical areas.

---

## 2. Project Objectives

### Primary Goals

1. **Develop IoT device ecosystem** for smart home monitoring
2. **Implement real-time monitoring system** for environmental and security parameters
3. **Create scalable serverless backend** using AWS managed services
4. **Build intuitive dashboard interface** for monitoring and device management

### Key Success Metrics

- **Device Connectivity**: 99.9% uptime for IoT device connections
- **Real-time Performance**: <100ms latency for critical alerts
- **User Experience**: Responsive dashboard accessible on web and mobile
- **Cost Efficiency**: Stay within $100 budget while achieving production-ready prototype

---

## 3. Technical Architecture

### 3.1 Hardware Layer (IoT Devices)

- **Microcontroller**: ESP32 with integrated WiFi capability
- **Sensors**: Temperature/humidity (DHT11), Gas detection (MQ series), MKE-S04 IR fire sensor
- **Communication**: MQTT over TLS 1.3 for secure data transmission

### 3.2 AWS Cloud Services Integration

| Service | Purpose | Estimated Monthly Cost |
|---------|---------|----------------------|
| **AWS IoT Core** | Device gateway and messaging | $3-8 (for smart home) |
| **AWS IoT Rules** | Message routing and filtering | Free |
| **AWS Lambda** | Serverless business logic | $10.25 |
| **Amazon DynamoDB** | NoSQL database for sensor data | $0.36 |
| **Amazon S3** | Data storage and backup | $1-2 |
| **Amazon SES** | Email notification services | $1-2 |
| **API Gateway** | RESTful API endpoints | $6.25 |
| **Amazon Cognito** | User authentication and authorization | $1-2 |
| **AWS Amplify** | Frontend hosting and CI/CD | $1-2 |
| **Amazon Route 53** | DNS and domain management | $1-2 |

### 3.3 System Architecture Diagram

![System Architecture](/FCJ_D2F/images/Diagrams.png)

---

## 4. Budget Analysis

### 4.1 WebApp Development ($10)

- **Frontend Framework**: React.js/Vue.js development tools - free
- **Testing & Deployment**: AWS S3/CloudFront hosting - $10
- **Development Libraries**: Chart.js, Material-UI, WebSocket libraries - free
- **Documentation & Training**: Technical writing resources - free

### 4.2 IoT Hardware & Firmware ($40)

- **Development Boards**: 3x ESP32 development kits for smart home - $15
- **Sensors & Components**: Temperature, humidity, gas, motion sensors - $10
- **Power Supplies & Enclosures**: Housing and power management - $10
- **Connectivity Components**: WiFi modules and antenna - $5

---

## 5. Implementation Timeline

### Phase 1: Foundation (Month 1)

#### Week 1-2: Architecture & Planning

- System architecture design and documentation
- AWS account setup and service configuration
- Development environment preparation
- Team training on AWS services and security protocols

#### Week 3-4: Core Development

- Hardware schematic design and component sourcing
- Basic firmware development for sensor integration
- Backend API design and initial Lambda functions
- Database schema design

### Phase 2: Integration (Month 2)

#### Week 5-6: Hardware-Software Integration

- Component assembly
- Device-to-cloud communication implementation
- Real-time data pipeline development
- User authentication setup

#### Week 7-8: Frontend Development

- Dashboard UI/UX design
- Frontend dashboard development
- Mobile responsive implementation

### Phase 3: Testing & Deployment (Month 3)

#### Week 9-10: System Integration Testing

- End-to-end system testing and validation
- Performance optimization and load testing
- User acceptance testing and feedback incorporation
- Bug fixes and refinements

#### Week 11-12: Production Preparation

- Documentation completion and technical manual creation
- Production deployment and monitoring setup
- Final system validation
- Project presentation and demonstration preparation

---

## 6. Deliverables

### 6.1 Hardware Deliverables

- ***IoT Sensor Boards**: 3 fully functional prototypes with integrated sensors for smart home*
- **Hardware Documentation**: Schematics and assembly instructions
- **Manufacturing Guide**: Production-ready documentation for scale-up

### 6.2 Software Deliverables

- **Backend API**: RESTful services with comprehensive documentation
- **Frontend Dashboard**: Responsive web application with real-time monitoring
- **Mobile Interface**: Progressive Web App (PWA) for mobile device access
- **Database Schema**: Optimized data models for time-series sensor data

---

## 7. Risk Assessment & Mitigation

### 7.1 Technical Risks

| Risk | Impact | Probability | Mitigation Strategy |
|------|--------|-------------|-------------------|
| Hardware component delays | High | Medium | Order components early, maintain backup suppliers |
| AWS service cost overrun | Medium | Low | Implement cost monitoring, use free tier effectively |
| Security vulnerability discovery | High | Low | Regular security testing, follow AWS best practices |
| Integration complexity | Medium | Medium | Incremental integration, comprehensive testing |

### 7.2 Project Management Risks

| Risk | Impact | Probability | Mitigation Strategy |
|------|--------|-------------|-------------------|
| Team member unavailability | Medium | Low | Cross-training, documentation, backup assignments |
| Timeline delays | Medium | Medium | Buffer time allocation, milestone tracking |
| Budget constraints | High | Low | Weekly budget tracking, cost optimization |

---

## 8. Expected Outcomes & Impact

### 8.1 Technical Achievements

- **Functional IoT System**: Production-ready prototype demonstrating all key features
- **Real-time Performance**: Sub-second response times for critical alerts and notifications
- **Scalable Architecture**: Cloud-native design ready for expansion

### 8.2 Learning Outcomes

- **Cloud Architecture**: Hands-on experience with AWS services and serverless computing
- **IoT Development**: Understanding of IoT device integration and firmware development
- **Full-Stack Development**: Complete software development lifecycle experience
- **Project Management**: Practical experience in agile development and team collaboration

### 8.3 Future Applications

- **Smart Home Management**: Environmental monitoring for smart homes
- **Commercial IoT**: Equipment monitoring and predictive maintenance systems
- **Healthcare Monitoring**: Patient environment and medical device tracking
- **Environmental Monitoring**: Air quality and climate monitoring networks

---

## 9. Conclusion

This IoT Security Monitoring & Alert System project represents a comprehensive approach to modern IoT development, *combining cutting-edge hardware design,* robust security protocols, and scalable cloud architecture. With a budget of $100 and a timeline of 3 months, our team of 5 dedicated students will deliver a production-ready prototype that demonstrates best practices in IoT security, cloud computing, and full-stack development.

The project not only serves as an excellent learning experience but also creates a foundation for real-world applications in smart homes, industrial monitoring, and environmental protection. By leveraging AWS managed services and focusing on security-first design principles, we aim to create a system that meets both current needs and future scalability requirements.

**Project Contact Information:**

- **Project Manager**: Tran Quang Huy  
- **Security Lead**: Tran Quang Huy
- **Email**: <huytqse182122@fpt.edu.vn>
- **Project Repository**: <https://github.com/saltless-bruh/D2F_FCJ>

---

*This proposal is submitted for consideration and approval. We look forward to the opportunity to demonstrate our technical capabilities and deliver exceptional results within the proposed timeline and budget.*

## Project Documents

{{%attachments title="Related Documents" style="blue" /%}}
