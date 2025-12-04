---
title: "Translated Blogs"
date: 2025-10-12
weight: 3
chapter: false
pre: "<b>3. </b>"
---

## Overview

During Week 5 of my AWS First Cloud Journey internship (October 6-9, 2025), I translated three AWS technical blogs from English to Vietnamese. This initiative aims to make valuable AWS technical content accessible to Vietnamese developers and contribute to the growing Vietnamese cloud computing community. All translations were submitted via Google Form to the FCJ content team.

These translations focus on maintaining technical accuracy while ensuring natural Vietnamese phrasing, helping bridge the language gap for Vietnamese developers learning AWS technologies.

---

## Blog 1: Correlating Telemetry Data with Amazon OpenSearch Service and Amazon Managed Grafana

### Original Content Summary

This blog explores how to troubleshoot large, distributed enterprise applications by correlating different observability signals (logs, traces, and metrics) using Amazon OpenSearch Service and Amazon Managed Grafana. It demonstrates building a comprehensive observability solution that reduces Mean Time to Resolution (MTTR) by enabling effective root cause analysis across microservices architectures.

### Translation Highlights

- **Technical Terms Retained**: OpenTelemetry Collector, serverless, pipeline, microservices, fault isolation, trace, metric, log
- **AWS Services Preserved**: Amazon OpenSearch Service, Amazon Managed Grafana, Amazon Managed Service for Prometheus, Amazon EKS, Amazon OpenSearch Ingestion
- **Localization Decisions**: Translated conceptual explanations into natural Vietnamese while preserving technical accuracy. Terms like "observability signals" became "tín hiệu khả năng quan sát" to maintain clarity
- **Code and Configuration**: All YAML configurations, JSON policies, and command-line examples kept in original format with Vietnamese explanatory text

### Key Topics Covered

- Setting up OpenTelemetry for unified telemetry collection
- Implementing Amazon OpenSearch Ingestion pipelines for scalable data processing
- Configuring separate storage for logs and traces in OpenSearch domains
- Integrating Amazon Managed Grafana for data visualization
- Creating IAM policies and roles for secure pipeline operations
- Building correlation workflows across different data stores
- Best practices for enterprise-scale observability architecture

### Target Audience

- DevOps engineers implementing observability solutions
- Cloud architects designing distributed systems monitoring
- SRE teams working on improving MTTR
- Vietnamese developers adopting AWS observability services

### Translation Approach

- Direct translation for procedural steps while maintaining command syntax
- Adaptation of architectural concepts to Vietnamese technical vocabulary
- Preserved all AWS Console navigation paths in English with Vietnamese descriptions
- Maintained code blocks and configuration files unchanged for easy implementation

### Link to Translated Content

[View Full Translation - Blog 1](https://docs.google.com/document/d/1hnV0juMqHs53-WLwe6cQpJSUdNTdIaE8y3VO6PMqPX4/edit?usp=sharing)

---

## Blog 2: Implementing Advanced Data Protection for Amazon EKS with NetApp Trident Add-on and Amazon FSx for NetApp ONTAP

### Original Content Summary

This technical guide demonstrates how to deploy advanced data protection capabilities for Amazon EKS using the NetApp Trident add-on from AWS Marketplace and Amazon FSx for NetApp ONTAP. It covers cross-cluster PersistentVolumeClaim (PVC) replication for disaster recovery, instant snapshots for data protection, and in-place snapshot restoration using Kubernetes custom resources.

### Translation Highlights

- **Technical Terms Retained**: add-on, Container Storage Interface (CSI), PersistentVolumeClaim (PVC), snapshot, bind mount, volume mount, Storage Virtual Machines (SVM), SnapMirror
- **AWS Services Preserved**: Amazon EKS, Amazon FSx for NetApp ONTAP, AWS Marketplace, AWS Secrets Manager, AWS IAM
- **Localization Decisions**: Translated disaster recovery concepts while keeping DR abbreviation. "Failover" translated as "chuyển đổi dự phòng" for clarity in Vietnamese context
- **GitOps Integration**: Emphasized how Trident custom resources enable GitOps workflows, a key concept for modern Kubernetes deployments

### Key Topics Covered

- Installing and configuring NetApp Trident as an EKS add-on
- Setting up cross-cluster replication between primary and DR EKS clusters
- Configuring FSx for ONTAP file systems and Storage Virtual Machines
- Creating IAM policies and roles for Trident CSI driver operations
- Implementing TridentMirrorRelationship (TMR) for data replication
- Testing failover scenarios for disaster recovery validation
- Best practices for multi-cluster Kubernetes storage management

### Target Audience

- Kubernetes administrators managing stateful applications
- Platform engineers implementing disaster recovery solutions
- DevOps teams adopting GitOps workflows
- Vietnamese cloud engineers working with container storage

### Translation Approach

- Step-by-step procedural translation with preserved command syntax
- Visual references (figures) translated in context
- Technical prerequisites clearly outlined in Vietnamese
- Code samples and YAML manifests maintained with Vietnamese annotations

### Link to Translated Content

[View Full Translation - Blog 2](https://docs.google.com/document/d/1ID0cw1LUwhZiFC03ndyjJQdcxwlh7VxjsS0wr6Oo3pk/edit?usp=sharing)

---

## Blog 3: Fine-tuning Large Language Models with Reinforcement Learning from Human or AI Feedback

### Original Content Summary

This advanced machine learning blog explores techniques for aligning Large Language Models (LLMs) with human preferences through Reinforcement Learning from Human Feedback (RLHF), Reinforcement Learning from AI Feedback (RLAIF), and Direct Policy Optimization (DPO). It provides a comprehensive comparison of these methods and implements a practical RLAIF use case to reduce toxicity in LLM responses.

### Translation Highlights

- **Technical Terms Retained**: Large Language Models (LLMs), Natural Language Processing (NLP), reinforcement learning, reward model, policy optimization, hallucination, Constitutional AI, superalignment
- **AWS Services Preserved**: Amazon SageMaker, Amazon Bedrock, Amazon SageMaker Ground Truth
- **Localization Decisions**: Complex ML concepts like "Pareto frontier" explained with Vietnamese context. "Alignment" translated as "căn chỉnh" or "tương thích" depending on context
- **Academic References**: Maintained all citation formats and paper references in original form

### Key Topics Covered

- Comparison of RLHF, RLAIF, and DPO for LLM fine-tuning
- Reward model categories for human preferences (helpfulness, honesty, harmlessness)
- Implementing RLAIF pipelines without explicit human annotation
- Using Proximal Policy Optimization (PPO) for policy gradient training
- Evaluating toxicity reduction in LLM responses
- Scaling alignment efforts beyond direct human supervision
- Practical implementation with Hugging Face TRL library on Amazon SageMaker

### Target Audience

- Machine learning engineers working with foundation models
- AI researchers exploring alignment techniques
- Data scientists fine-tuning LLMs for production use
- Vietnamese ML practitioners adopting responsible AI practices

### Translation Approach

- Preserved mathematical formulations and algorithm descriptions
- Translated conceptual frameworks with careful attention to AI ethics terminology
- Maintained Python code samples with Vietnamese commentary
- Explained trade-offs between methods in clear Vietnamese language

### Link to Translated Content

[View Full Translation - Blog 3](https://docs.google.com/document/d/1bODyGeqjYXIxA9rkMRZvqJZtq4J9PEKTWRfBdUb2ekA/edit?usp=sharing)

---

## Translation Methodology

### Approach

**Direct Translation**: Applied for procedural steps, command syntax, and configuration examples where technical accuracy is paramount. All AWS CLI commands, YAML configurations, and code samples remained in original format.

**Adaptation**: Used for conceptual explanations and architectural discussions where cultural context and Vietnamese technical vocabulary improve understanding. For example, "observability" became "khả năng quan sát" rather than a direct loan word.

**Transcreation**: Applied sparingly for introductory sections and user-facing descriptions to ensure natural Vietnamese flow while preserving technical intent.

### Quality Standards

- **Technical Accuracy**: All AWS service names, API calls, and technical specifications verified against official AWS documentation
- **Natural Language Flow**: Vietnamese sentences structured for readability while avoiding awkward word-for-word translations
- **Terminology Consistency**: Maintained consistent translation of recurring technical terms across all three blogs
- **Code Preservation**: All code blocks, commands, and configuration files kept in original English/syntax for immediate usability

### Tools and Resources

- AWS official documentation (both English and available Vietnamese resources)
- Vietnamese technical writing style guides
- Collaboration with FCJ team for terminology verification
- Reference to existing Vietnamese AWS community content

### Challenges Overcome

**1. AWS-Specific Jargon**: Balanced between keeping AWS service names in English (for searchability and official documentation alignment) versus translating conceptual terms. Solution: Keep all AWS service names and most technical abbreviations in English while translating explanatory text.

**2. Cloud Architecture Concepts**: Translated complex distributed systems concepts (like "fault isolation," "cascading failures") into Vietnamese while maintaining precision. Solution: Used descriptive Vietnamese phrases that explain the concept clearly.

**3. Code Example Clarity**: Ensured Vietnamese readers could follow English code comments and variable names. Solution: Added Vietnamese explanatory paragraphs before and after code blocks.

**4. Technical Depth Balance**: Maintained intermediate-to-advanced technical level appropriate for the target audience without oversimplifying. Solution: Assumed reader familiarity with basic cloud concepts and focused translation effort on unique AWS service features.

---

## Impact and Contribution

### Community Benefit

These translations directly support the Vietnamese AWS developer community by:

- **Lowering Language Barriers**: Enabling non-English proficient developers to access advanced AWS technical content
- **Accelerating Learning**: Reducing cognitive load by providing native-language explanations of complex concepts
- **Building Local Expertise**: Contributing to Vietnam's growing cloud computing talent pool
- **FCJ Mission Alignment**: Supporting First Cloud Journey's goal of making cloud education accessible to Vietnamese learners

### Learning Outcomes

Through this translation project, I developed:

- **Deep AWS Service Understanding**: Translating technical content required thorough comprehension of observability architectures, Kubernetes storage systems, and ML fine-tuning techniques
- **Technical Writing Skills**: Learned to balance technical precision with readability in Vietnamese
- **Bilingual Technical Communication**: Enhanced ability to explain complex technical concepts in both English and Vietnamese
- **Cultural Localization**: Understanding how to adapt English technical documentation for Vietnamese technical culture

### Metrics

- **Total Word Count**: Approximately 15,000+ words translated across three blogs
- **Translation Time**: ~20-25 hours total (including research, translation, and quality review)
- **Technical Terms Standardized**: 100+ AWS service names and technical terms consistently applied
- **Target Audience Reach**: Vietnamese AWS developers at intermediate to advanced skill levels

### Future Impact

These translations join a growing body of Vietnamese AWS technical content, helping establish terminology standards and best practices for future Vietnamese cloud documentation. They serve as reference materials for:

- Vietnamese universities teaching cloud computing courses
- Enterprise teams in Vietnam adopting AWS services
- Independent developers learning advanced AWS architectures
- FCJ program participants in future cohorts
