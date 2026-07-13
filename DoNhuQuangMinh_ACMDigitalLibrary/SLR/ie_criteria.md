# Inclusion and Exclusion Criteria

## Inclusion Criteria

| ID | Criterion |
|----|-----------|
| IC1 | The study is written in English. |
| IC2 | The study was published in or after 2018. |
| IC3 | The study is peer-reviewed (conference paper, journal article, or workshop paper). |
| IC4 | The study is related to at least one of the following topics: automated software testing, acceptance testing, Behavior-Driven Development (BDD), Gherkin scenario generation, requirements engineering, user stories, requirements-to-test transformation, or the application of Large Language Models (LLMs) in Software Engineering. |
| IC5 | The study provides empirical evidence, experimental results, case studies, evaluations, or quantitative/qualitative assessment of the proposed approach. |

---

## Exclusion Criteria

| ID | Criterion |
|----|-----------|
| EC1 | Duplicate record already identified from another search string or source. |
| EC2 | Full text is unavailable or inaccessible for review. |
| EC3 | The publication is a poster, extended abstract, tutorial, keynote, editorial, panel summary, or contains fewer than four pages of technical content. |
| EC4 | The study focuses only on test execution, test maintenance, project management, infrastructure, or unrelated domains and does not address test generation, requirements transformation, BDD/Gherkin, acceptance testing, or LLM-supported Software Engineering activities. |

---

# Screening Procedure

## Phase 1: Title and Abstract Screening

A study is included if it satisfies:

- IC1 (English)
- IC2 (Published in or after 2018)
- IC3 (Peer-reviewed)

A study is excluded if it violates any of:

- IC1
- IC2
- IC3
- EC1

Output:

- INCLUDE
- EXCLUDE
- UNSURE

---

## Phase 2: Full-Text Eligibility Assessment

Studies that pass Phase 1 are assessed against:

- IC4
- IC5
- EC2
- EC3
- EC4

A study is included if:

- It satisfies IC4 and IC5.
- It does not violate EC2, EC3, or EC4.

Output:

- INCLUDE
- EXCLUDE

---

# Mapping to Screening Files

## 02_screening_results.csv

### v1_decision

- INCLUDE
- EXCLUDE
- UNSURE

### v1_reason Examples

- Meets IC1/IC2/IC3
- Fails IC2 (< 2018)
- Duplicate (EC1)

### v2_decision

- INCLUDE
- EXCLUDE

### v2_reason Examples

- IC4
- IC4/IC5
- EC2
- EC3
- EC4

---

# Application to This Thesis

A study is considered highly relevant if it addresses one or more of the following:

- User Story Analysis
- Connextra User Stories
- Acceptance Criteria Generation
- Gherkin Scenario Generation
- Behavior-Driven Development (BDD)
- Requirements-to-Test Transformation
- Automated Acceptance Testing
- Large Language Models (LLMs) in Software Engineering
- GPT-based Test Generation

Studies directly supporting zero-shot user story-to-Gherkin generation are prioritized during final inclusion and evidence extraction.