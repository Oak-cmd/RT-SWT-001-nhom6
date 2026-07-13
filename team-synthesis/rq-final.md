# rq-final.md

# Final Research Question (RQ)

## Official RQ

Does **GPT-4o zero-shot (temperature = 0)** generate Gherkin acceptance test scenarios from **Connextra-format user stories** that achieve:

1. **Cosine semantic similarity ≥ 0.85** compared with expert-written Gherkin scenarios, and
2. **Executable syntax rate ≥ 80%** when validated using a Gherkin parser?

---

## Final PICO

| Element | Definition |
|----------|------------|
| **P (Population)** | Connextra-format user stories collected from real software engineering projects |
| **I (Intervention)** | GPT-4o zero-shot generation of Gherkin acceptance test scenarios |
| **C (Comparison)** | Expert-written Gherkin scenarios created from the same user stories |
| **O (Outcome)** | (1) Cosine semantic similarity using all-MiniLM-L6-v2, (2) Executable syntax rate validated by parser |

## Justification

The merged SLR consistently identified:
- GPT-4/GPT-4o as the strongest family of models.
- Lack of embedding-based semantic similarity evaluation.
- Lack of studies combining semantic preservation and executable validation.
- Absence of a dedicated GPT-4o zero-shot evaluation on Connextra user stories.
