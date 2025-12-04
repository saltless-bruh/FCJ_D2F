# TRANSLATED BLOGS CONTENT GENERATION PROMPT

## Role and Context

You are an expert technical writer and bilingual content specialist (English/Vietnamese) working on documentation for the AWS First Cloud Journey (FCJ) internship program. Your task is to create comprehensive documentation of translated blog contributions in both English and Vietnamese, following FCJ's standard documentation format.

## Project Context

**Intern:** Senior Software Developer at AWS FCJ  
**Period:** September 8, 2025 - December 4, 2025  
**Task:** Translated 3 AWS technical blogs from English to Vietnamese during Week 5 (October 6-12, 2025)  
**Submission:** Via Google Form to FCJ content tea
**Format:** Follow this format <https://workshop-sample.fcjuni.com/3-blogstranslated/>

## Source Materials

You must fetch and incorporate content from these three Google Docs containing the translated blogs:

1. <https://docs.google.com/document/d/1hnV0juMqHs53-WLwe6cQpJSUdNTdIaE8y3VO6PMqPX4/edit?usp=sharing>
2. <https://docs.google.com/document/d/1ID0cw1LUwhZiFC03ndyjJQdcxwlh7VxjsS0wr6Oo3pk/edit?usp=sharing>
3. <https://docs.google.com/document/d/1bODyGeqjYXIxA9rkMRZvqJZtq4J9PEKTWRfBdUb2ekA/edit?usp=sharing>

**Note:** If the Google Docs are not accessible, request the user to provide the blog content or make the documents publicly accessible.

## Output Requirements

### File Structure

Generate two complete markdown files:

1. `3-Translated-Blogs/_index.md` (English version)
2. `3-Translated-Blogs/_index.vi.md` (Vietnamese version)

### Format Specifications

Follow Hugo static site generator structure with proper front matter and hierarchical organization similar to FCJ workshop documentation standards:[3]

```markdown
---
title: "Translated Blogs"
date: YYYY-MM-DD
weight: 3
chapter: false
---

## Overview
[Brief introduction to blog translation contributions]

## Blog 1: [Title in English]
### Original Content Summary
[2-3 sentence summary of the original blog topic]

### Translation Highlights
[Key technical terms translated, challenges faced, localization decisions]

### Target Audience
[Who benefits from this translation]

### Link to Translation
[Link to Google Doc or published version]

## Blog 2: [Title in English]
[Repeat structure]

## Blog 3: [Title in English]
[Repeat structure]

## Translation Methodology
[Approach taken for technical accuracy and cultural localization]

## Impact and Contribution
[How these translations benefit the Vietnamese AWS community]
```

## Content Structure Guidelines

### English Version (_index.md)

**Front Matter:**

```yaml
---
title: "Translated Blogs"
date: 2025-10-12
weight: 3
chapter: false
pre: "<b>3. </b>"
---
```

**Overview Section:**

- Brief introduction (3-4 sentences) explaining the blog translation initiative
- Mention this was part of Week 5 activities (October 6-12, 2025)
- State the purpose: making AWS technical content accessible to Vietnamese developers
- Note submission via Google Form to FCJ

**Per Blog Structure:**
Each of the 3 blogs should have:

1. **Blog Title** (## header)
   - Use the actual English title from the source document
   - Add subtitle if relevant

2. **Original Content Summary** (### header)
   - 2-3 sentences summarizing the blog's main topic
   - Include the primary AWS services or concepts covered
   - Example: "This blog explores AWS Lambda deployment strategies using containerized applications, covering best practices for Docker image optimization and cold start reduction."

3. **Translation Highlights** (### header)
   - Technical terminology decisions
   - Localization choices for Vietnamese audience
   - Challenges encountered (e.g., translating AWS service names, technical jargon)
   - Example: "Retained 'Lambda function' and 'cold start' in English as they are standard industry terms. Translated conceptual explanations into natural Vietnamese while preserving technical accuracy."

4. **Key Topics Covered** (### header)
   - Bullet list of main topics/sections in the blog
   - AWS services discussed
   - Technical concepts explained
   - Best practices highlighted

5. **Target Audience** (### header)
   - Who benefits from this translation
   - Skill level (beginner, intermediate, advanced)
   - Use cases or scenarios

6. **Translation Approach** (### header)
   - Methodology used (direct translation, adaptation, transcreation)
   - Tools utilized (if any)
   - Quality assurance steps

7. **Link to Translated Content** (### header)
   - Provide the Google Doc link
   - Note: "[View Full Translation](Google Doc URL)"

### Vietnamese Version (_index.vi.md)

**Front Matter:**

```yaml
---
title: "[translate:Các Blog Đã Dịch]"
date: 2025-10-12
weight: 3
chapter: false
pre: "<b>3. </b>"
---
```

**Structure:**

- Mirror the English version structure exactly
- Use natural Vietnamese phrasing
- Preserve AWS service names in English (e.g., Lambda, S3, EC2, DynamoDB)
- Keep technical terms in English when they are industry standard (e.g., serverless, container, deployment, CI/CD)
- Translate conceptual explanations naturally into Vietnamese

**Translation Guidelines for Vietnamese:**

- Headers: Translate to Vietnamese (e.g., Tổng Quan, Phương Pháp Dịch Thuật)
- AWS Services: Keep in English (AWS Lambda, Amazon S3, AWS IoT Core)
- Technical Terms: Use English for established terms (serverless, microservices, CI/CD, API Gateway)
- Explanations: Natural Vietnamese with appropriate technical vocabulary
- Bullet points: Translate fully to Vietnamese while preserving technical accuracy

## Content Requirements for Each Blog

### Information to Extract from Source Documents

1. **Original blog title** (English)
2. **Main topic/theme** (AWS service or concept)
3. **Technical depth** (introductory, intermediate, advanced)
4. **Key AWS services mentioned**
5. **Primary audience** (developers, architects, DevOps engineers, etc.)
6. **Core concepts explained**
7. **Practical examples or use cases**
8. **Best practices highlighted**

### Translation Documentation Elements

1. **Technical terminology decisions**
   - Which terms were kept in English
   - Which terms were translated to Vietnamese
   - Rationale for each decision

2. **Localization adaptations**
   - Cultural context adjustments
   - Examples adapted for Vietnamese market
   - Regional cloud considerations (if applicable)

3. **Quality assurance**
   - Review process
   - Technical accuracy verification
   - Native speaker review (if applicable)

4. **Challenges and solutions**
   - Complex technical concepts
   - Ambiguous source material
   - Vietnamese terminology gaps

## Translation Methodology Section

Include a comprehensive section covering:

### Approach

- **Direct Translation:** When technical accuracy requires literal translation
- **Adaptation:** When cultural context demands modification
- **Transcreation:** When preserving intent over literal meaning

### Quality Standards

- Technical accuracy verification against AWS documentation
- Natural Vietnamese language flow
- Consistency in terminology throughout
- Peer review by other Vietnamese developers (if applicable)

### Tools and Resources

- Translation memory tools used (if any)
- AWS terminology databases referenced
- Vietnamese technical writing style guides
- Collaboration with FCJ team members

### Challenges Overcome

- Handling AWS-specific jargon
- Translating cloud architecture concepts
- Maintaining code example clarity
- Balancing technical precision with readability

## Impact and Contribution Section

### Community Benefit

- How these translations help Vietnamese developers
- Accessibility improvements for non-English speakers
- Contribution to FCJ's mission of cloud education
- Building Vietnamese AWS technical content library

### Learning Outcomes

- Translation skills developed
- Deeper AWS service understanding
- Technical writing improvement
- Bilingual content creation expertise

### Metrics (if available)

- Word count per blog
- Translation time invested
- Technical terms translated
- Community feedback received

## Writing Style Guidelines

### Tone

- **Professional but accessible:** Technical content that's approachable
- **Educational:** Emphasize learning and knowledge sharing
- **Contributor mindset:** Highlight community contribution aspect
- **Bilingual excellence:** Showcase quality of both languages

### Language Specifications

**English Version:**

- Clear, concise technical writing
- Active voice preferred
- Short paragraphs (3-4 sentences max)
- Use bullet points for lists
- Professional technical documentation style

**Vietnamese Version:**

- Natural Vietnamese phrasing (avoid word-for-word translation)
- Appropriate use of formal technical Vietnamese
- Retain English terms where industry-standard
- Use Vietnamese punctuation conventions
- Maintain professional tone while being accessible

### Formatting Standards

- Use `##` for main sections (e.g., Blog 1, Blog 2)
- Use `###` for subsections (e.g., Translation Highlights, Key Topics)
- Use `-` for bullet points (no indentation)
- Use `**bold**` for emphasis on key terms
- Use backticks for code terms: `Lambda`, `S3`, `API Gateway`
- Use blockquotes `>` for important notes or callouts

## Technical Accuracy Requirements

### AWS Service Names

- Always use official AWS service names in English
- Example: AWS Lambda (not Lambda, not AWS Lambda)
- Example: Amazon S3 (not S3)
- Example: AWS IoT Core (not AWS Lõi IoT)

### Technical Terms

Preserve in English:

- Architecture patterns (serverless, microservices, event-driven)
- Technical operations (deployment, scaling, monitoring)
- Development concepts (CI/CD, containerization, orchestration)
- Industry acronyms (API, SDK, CLI, REST, JSON, YAML)

Translate to Vietnamese:

- General concepts (security → bảo mật, performance → hiệu suất)
- Action descriptions (configure → cấu hình, implement → triển khai)
- Explanatory text and instructions

### Code and Commands

- Keep all code snippets in original format
- Keep command-line examples in English
- Translate code comments if present in source
- Translate explanations around code blocks

## Quality Checklist

Before finalizing, verify:

- [ ] Both English and Vietnamese versions are complete
- [ ] All 3 blogs are documented with full details
- [ ] Front matter is correct in both files
- [ ] AWS service names are consistently in English
- [ ] Technical terms follow the preservation guidelines
- [ ] Vietnamese translation reads naturally (not robotic)
- [ ] All links to Google Docs are included and functional
- [ ] Sections are parallel between English and Vietnamese versions
- [ ] Translation methodology is clearly explained
- [ ] Impact and contribution sections are meaningful
- [ ] Formatting is consistent throughout
- [ ] No markdown syntax errors
- [ ] Headers follow hierarchical structure (##, ###)
- [ ] Bullet points are properly formatted

## Expected Output Deliverables

### File 1: `3-Translated-Blogs/_index.md`

- Complete English documentation
- 600-1000 words total
- Professional technical writing style
- Clear structure with all required sections
- Links to all 3 translated blogs

### File 2: `3-Translated-Blogs/_index.vi.md`

- Complete Vietnamese documentation
- Parallel structure to English version
- Natural Vietnamese phrasing
- Appropriate technical term handling
- Links to all 3 translated blogs

## Additional Instructions

1. **If Source Documents Are Inaccessible:**
   - Clearly indicate which documents couldn't be accessed
   - Request user to provide blog titles and summaries
   - Offer to generate template structure that user can fill in
   - Suggest making Google Docs publicly viewable

2. **Blog Title Extraction:**
   - Extract actual blog titles from source documents
   - Use original English titles in both versions
   - Vietnamese version can include Vietnamese translation in parentheses

3. **Technical Content Handling:**
   - Prioritize technical accuracy over creative translation
   - Verify AWS terminology against official documentation
   - Maintain consistency across all 3 blog documentation

4. **Community Context:**
   - Emphasize contribution to Vietnamese AWS developer community
   - Highlight FCJ's mission of making cloud knowledge accessible
   - Connect to broader goal of technical content localization

5. **Professional Presentation:**
   - Format must be ready for immediate use in Hugo static site
   - No placeholders or incomplete sections
   - Professional documentation quality suitable for publication

## Success Criteria

The generated documentation should:

- ✅ Accurately represent the 3 translated blogs with full details
- ✅ Provide clear insight into translation methodology and challenges
- ✅ Be bilingual with high-quality English and Vietnamese content
- ✅ Follow FCJ documentation standards and Hugo format
- ✅ Include all required sections with appropriate depth
- ✅ Demonstrate professional technical writing skills
- ✅ Be publication-ready without further editing needed
- ✅ Properly handle technical terminology in both languages
- ✅ Include working links to source translations
- ✅ Contribute meaningful context about community impact

***

This prompt follows advanced prompt engineering practices including:

- **Clear role and context** definition
- **Specific output structure** with templates
- **Detailed content requirements** per section
- **Bilingual handling guidelines** with technical term preservation rules
- **Quality standards** and verification checklist
- **Fallback instructions** for inaccessible sources
- **Success criteria** for output validation
- **Professional formatting** standards
- **Cultural localization** considerations for Vietnamese audience

The prompt is designed to generate production-ready documentation that accurately represents your blog translation contributions to the FCJ program.[2][4][3]

[1](https://www.reddit.com/r/TranslationStudies/comments/pd7dfb/format_for_translating_a_webpage/)
[2](https://translayte.com/blog/how-to-translate-blog-posts-professionally)
[3](https://blogs.fcdo.gov.uk/wp-content/uploads/FCO-Blogs-Languages-1.1.pdf)
[4](https://www.verbolabs.com/ultimate-guide-to-the-perfect-format-of-blog-writing/)
[5](https://www.tandfonline.com/doi/full/10.1080/23322969.2023.2170526)
[6](https://www.semanticscholar.org/paper/c4d6d4646802b91c4a35ad4ca145754e65dd5eec)
[7](https://www.tandfonline.com/doi/full/10.1080/13556509.2018.1543566)
[8](https://www.semanticscholar.org/paper/04d9f6a6590d7e9b58dcf4b90246707cfc174f6f)
[9](https://www.semanticscholar.org/paper/1a805825b98e93edcc152fa54d99ae27450d7c12)
[10](https://www.semanticscholar.org/paper/ec8ea58dac258a4e7198675e0632520cec0f8b0c)
[11](https://www.semanticscholar.org/paper/aff5f95a1b25b628d350e6f9a17712e70cc238bd)
[12](https://www.semanticscholar.org/paper/e53c82bd76b30df417b716703def7797b12f9284)
[13](https://www.cdri.org.kh/publication/negotiating-family-and-personal-aspirations-four-young-cambodian-women-reflecting-on-choosing-a-major)
[14](http://choicereviews.org/review/10.5860/CHOICE.35-2812)
[15](https://www.aclweb.org/anthology/W16-2603.pdf)
[16](https://www.mdpi.com/2304-6775/10/1/9/pdf)
[17](https://journals.uni-lj.si/elope/article/download/11829/12909)
[18](https://www.degruyter.com/document/doi/10.1515/applirev-2022-0016/pdf)
[19](https://www.mdpi.com/2079-9292/12/5/1140/pdf?version=1677660375)
[20](https://pmc.ncbi.nlm.nih.gov/articles/PMC10877626/)
[21](https://downloads.hindawi.com/journals/misy/2022/3737199.pdf)
[22](https://www.tandfonline.com/doi/pdf/10.1080/21670811.2018.1468722?needAccess=true)
[23](http://fibreculturejournal.org/wp-content/pdfs/FCJ-190RobertWGehl.pdf)
[24](https://fcjsisters.wordpress.com)
[25](https://aws.amazon.com/blogs/machine-learning/create-a-serverless-pipeline-to-translate-large-documents-with-amazon-translate/)
[26](https://aws.amazon.com/blogs/machine-learning/translating-documents-with-amazon-translate-aws-lambda-and-the-new-batch-translate-api/)
[27](http://fc2blogmanualen.blog.fc2.com/blog-entry-1.html)
[28](https://www.ficode.com/blog/a-step-by-step-guide-to-aws-cloud-migration)
