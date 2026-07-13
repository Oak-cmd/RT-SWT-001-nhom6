# GAP Statement from Evidence Table

## Evidence Summary

All reviewed papers in the evidence table focus on applying Large Language Models (LLMs), model-based approaches, Behavior-Driven Development (BDD), or automated transformations to support software testing and requirements engineering.

The literature demonstrates significant progress in:

- Automated test generation.
- Requirements-to-test transformation.
- User story analysis and refinement.
- Acceptance testing support.
- BDD/Gherkin-based software testing.

Most studies evaluate their approaches using traditional metrics such as:

- BLEU
- ROUGE
- Manual expert assessment
- Generation accuracy
- Productivity improvement
- Test coverage

However, the reviewed studies reveal several important research gaps.

## However, NO paper:

### 1. Tool / LLM Gap

Evaluates the performance of a frontier Large Language Model in a dedicated **zero-shot user story-to-Gherkin generation** setting.

Existing studies investigate:

- Rule-based transformations.
- Template-based approaches.
- Traditional NLP techniques.
- Early AI-assisted generation.
- Domain-specific LLM applications.

However, none directly evaluate GPT-4o or a comparable frontier LLM for generating complete Gherkin acceptance test scenarios from Connextra-format user stories without prompt engineering or fine-tuning.

### 2. Metric Gap 1

Uses **embedding-based semantic similarity** as a primary evaluation metric to quantitatively assess whether generated Gherkin scenarios preserve the original business intent expressed in user stories.

Most existing evaluations rely on:

- Manual inspection.
- Surface-text similarity.
- Coverage metrics.
- Productivity measurements.

Few studies measure semantic preservation using modern sentence embedding techniques.

### 3. Metric Gap 2

Measures the **executable rate** of generated scenarios using a dedicated **Gherkin parser** to verify syntactic correctness and execution readiness.

Many papers evaluate generated outputs qualitatively; however, they do not verify whether generated scenarios are executable within practical BDD toolchains.

### 4. Common Limitation Gap

Several studies identify challenges related to:

- Complex business logic.
- Conditional workflows.
- Multi-step interactions.
- Nested acceptance criteria.
- Ambiguous user requirements.

Nevertheless, no study provides a systematic evaluation of how business-logic complexity affects the quality of automatically generated Gherkin scenarios.

## GAP

Existing research demonstrates that AI techniques, LLMs, and BDD-related approaches can support requirements engineering and software testing activities.

However, there remains a lack of empirical evidence regarding whether frontier LLMs can simultaneously generate Gherkin acceptance test scenarios that are:

- Semantically faithful to business requirements.
- Structurally executable in BDD environments.

Furthermore, the impact of business-logic complexity on generation quality remains insufficiently explored.

As a result, the effectiveness of zero-shot LLM-based transformation from user stories to executable Gherkin scenarios remains unclear.

## Contribution

This study addresses the identified research gap by evaluating a frontier Large Language Model in a **zero-shot user story-to-Gherkin generation task**.

The generated scenarios are assessed using two complementary evaluation metrics:

1. **Cosine semantic similarity** based on sentence embeddings to evaluate requirement preservation.
2. **Executable rate** based on automated Gherkin parsing to verify structural correctness and execution readiness.

The study additionally investigates performance under varying levels of business-logic complexity, providing empirical evidence for the applicability of LLM-assisted BDD automation in software engineering practice.

## Expected Contribution to Software Engineering

The study is expected to contribute:

- Empirical evidence on GPT-4o-based Gherkin generation.
- A reproducible evaluation framework for user story-to-Gherkin transformation.
- Quantitative measurements of semantic fidelity and executable correctness.
- Insights into the influence of business-logic complexity on generation performance.
- Practical guidance for adopting LLMs in Behavior-Driven Development workflows.