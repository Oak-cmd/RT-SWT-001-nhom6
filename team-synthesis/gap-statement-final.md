# gap-statement-final.md

# Final GAP Statement

## Current Evidence

The reviewed literature demonstrates substantial progress in:
- Automated BDD scenario generation.
- User-story-to-Gherkin transformation.
- Acceptance test generation using LLMs.
- Test automation using GPT-4, GPT-3.5, Gemini, Claude and related models.

## Identified Research Gaps

### GAP 1 — Model Gap
No study directly evaluates GPT-4o in a dedicated zero-shot user-story-to-Gherkin setting focused on Connextra requirements.

### GAP 2 — Semantic Evaluation Gap
Most studies rely on BLEU, ROUGE, METEOR, syntax validation, expert judgment, or Likert ratings.
Embedding-based semantic similarity is rarely used as a primary outcome.

### GAP 3 — Combined Metric Gap
No identified study simultaneously evaluates:
- Semantic similarity preservation, and
- Executable syntax validation.

### GAP 4 — Reproducible Experimental Configuration Gap
Many studies use few-shot prompting, custom pipelines, or proprietary workflows.
A reproducible GPT-4o zero-shot configuration with temperature = 0 remains underexplored.

### GAP 5 — Connextra-Specific Gap
Very few studies focus specifically on Connextra-format user stories as the experimental population.

## Final Gap Statement

There is currently no empirical study that evaluates GPT-4o zero-shot generation of Gherkin acceptance test scenarios from Connextra-format user stories using both embedding-based semantic similarity and executable syntax validation as primary outcome measures.
