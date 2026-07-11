# Tsavo Ranger Report: Redesigning EduSavvy AI Using the 4D Framework

## Introduction

Artificial Intelligence has the potential to transform education by providing personalized learning experiences, reducing teacher workload, and improving student outcomes. However, AI systems can also produce inaccurate, culturally inappropriate, or misleading responses when they lack sufficient context or rely on unverified information. The EduSavvy scenarios demonstrate common AI failures, including hallucinated data, poor localization, and culturally insensitive examples.

This report applies the **4D Framework (Delegation, Description, Discernment, and Diligence)** to redesign three AI interactions. Each redesign includes improved prompts, technical implementation details, Retrieval-Augmented Generation (RAG) requirements, negative prompting, and deployment safeguards. The report concludes by explaining why an **AI agency model**, where AI collaborates with teachers rather than replacing them, leads to better educational outcomes.

---

# Interaction 1: Science Tutoring (Turkana Scenario)

## Original Problem

The AI explained plant water absorption using snowmelt and glaciers, examples that are completely inappropriate for Turkana's arid environment.

---

## 4D Framework

### Delegation

* AI explains scientific concepts.
* Teacher reviews the response before students receive it.
* Curriculum experts define approved knowledge sources.

### Description

Prompt specifies:

* Kenyan secondary school learner.
* Turkana context.
* Arid and semi-arid ecosystems.
* CBC-aligned explanation.
* Simple language.

### Discernment

Before producing an answer, the AI checks:

* Is the ecosystem appropriate?
* Are the plant examples found in Kenya?
* Does the explanation match the learner's level?

### Diligence

The system retrieves information only from:

* Kenya Institute of Curriculum Development (KICD)
* CBC Science curriculum
* Approved biology learning resources

Teacher validation remains mandatory for generated lesson content.

---

## Redesigned Prompt

> **Act as a Kenyan secondary school science tutor. Explain how plants obtain water using examples from Turkana and other arid regions of Kenya. Use local plants such as acacia trees and describe how roots absorb water from the soil after rainfall. Align your explanation with the Kenya CBC curriculum and use simple language suitable for Form Two learners.**

---

## Technical Specifications

**Model Temperature:** **0.3**

Reason:

* Prioritizes factual consistency.
* Reduces unnecessary creativity.

**RAG Sources**

* Kenya Institute of Curriculum Development (KICD)
* CBC Science Curriculum
* Approved Kenyan Biology textbooks

---

## Negative Prompt

> Do not use snow, glaciers, ice, snowmelt, temperate climates, or examples from Europe or North America.

---

# Interaction 2: Mathematics Help (Mombasa Scenario)

## Original Problem

The AI generated mathematics questions involving pork purchases, making the exercise culturally insensitive for many Muslim learners in Mombasa.

---

## 4D Framework

### Delegation

* AI generates practice questions.
* Teacher approves the final worksheet.

### Description

Prompt requires:

* Kenyan everyday examples.
* Culturally appropriate contexts.
* CBC Mathematics alignment.
* Age-appropriate difficulty.

### Discernment

The AI evaluates whether examples:

* Respect religious diversity.
* Reflect Kenyan daily life.
* Avoid unnecessary cultural bias.

### Diligence

The AI retrieves examples from:

* CBC Mathematics curriculum
* Approved Kenyan classroom resources

The system also applies a cultural sensitivity filter before displaying questions.

---

## Redesigned Prompt

> **Generate ten mathematics word problems for Grade Six learners using everyday Kenyan contexts such as M-Pesa transactions, bus fares, fruit markets, school supplies, and farming activities. Ensure every question is culturally respectful and suitable for learners from all regions of Kenya.**

---

## Technical Specifications

**Model Temperature:** **0.4**

Reason:

* Allows moderate creativity while maintaining factual accuracy.

**RAG Sources**

* Kenya Institute of Curriculum Development Mathematics Curriculum
* CBC Teacher Guides
* Approved Kenyan Mathematics textbooks

---

## Negative Prompt

> Do not use examples involving pork, alcohol, gambling, weapons, or culturally or religiously sensitive situations. Do not use foreign currencies or non-Kenyan grading systems.

---

# Interaction 3: Parent Progress Reports (Hallucinated Rankings)

## Original Problem

The AI falsely reported that a learner ranked in the "bottom 10% nationally" despite having no verified national comparison data.

---

## 4D Framework

### Delegation

* AI drafts the report.
* Teacher reviews and approves before parents receive it.
* School administrators approve performance summaries.

### Description

Prompt specifies:

* Use only verified school assessment data.
* Avoid unsupported comparisons.
* Present constructive feedback.

### Discernment

Before generating a report, the AI asks:

* Is the data verified?
* Does a national benchmark exist?
* Is the comparison supported?

If not, the comparison is removed automatically.

### Diligence

Reports retrieve information only from:

* Verified EduSavvy database
* School assessment records
* CBC assessment framework

No external rankings are permitted unless officially provided.

---

## Redesigned Prompt

> **Generate a parent progress report using only verified school assessment records. Summarize learner strengths, areas requiring improvement, attendance, and recommendations. Do not compare the learner with national performance unless verified benchmark data has been provided. Include a transparency note indicating that the report is based solely on available school records.**

---

## Technical Specifications

**Model Temperature:** **0.2**

Reason:

* Parent reports require maximum accuracy and consistency.

---

## RAG Sources

* EduSavvy Student Database
* School Assessment Records
* KICD Assessment Framework

---

## Verification Pipeline

1. Retrieve verified learner data.
2. Validate grading scale.
3. Check whether benchmark datasets exist.
4. Remove unsupported comparisons.
5. Flag reports containing high-risk claims for teacher approval.

---

## Negative Prompt

> Do not generate national rankings, county rankings, percentiles, or comparisons unless verified benchmark data has been supplied. Do not invent statistics or performance trends.

---

# Reflection: From Automation to Agency

Traditional educational AI focuses primarily on **automation**. It generates lessons, quizzes, and reports independently, often without understanding the learner's cultural context or verifying the accuracy of its information. While this approach increases efficiency, it also increases the risk of hallucinations, culturally inappropriate examples, and inaccurate feedback.

An **agency model** transforms AI from an autonomous decision-maker into an intelligent collaborator that works alongside teachers. In this model, AI performs repetitive tasks such as drafting quizzes, explaining concepts, and preparing parent reports, while educators provide professional judgment, contextual understanding, and final approval.

The redesigned EduSavvy system demonstrates this shift by combining AI with teacher oversight, curriculum alignment, retrieval of verified information through RAG, and safety mechanisms such as negative prompting and verification pipelines. These safeguards ensure that content remains factually accurate, culturally appropriate, and aligned with Kenya's Competency-Based Curriculum.

Moving toward an agency model improves student learning because it delivers personalized instruction without sacrificing educational quality. Students receive locally relevant examples that reflect their own environment, teachers spend less time preparing materials, and parents receive trustworthy reports based on verified evidence rather than fabricated comparisons. The result is an AI system that is not only more efficient but also more reliable, inclusive, and supportive of meaningful learning.
