# PRISMA Flow Diagram

**Topic:** LLM for Acceptance Test Automation (BDD/Gherkin)  
**Search date:** May 2026

---

```
┌─────────────────────────────────────────────────────────┐
│            Records identified from database searching    │
│   String A (IEEE Xplore, May 27):   35 records          │
│   String B (IEEE Xplore, May 31):  103 records          │
│   Tổng cộng:                       123 records          │
└──────────────────────────┬──────────────────────────────┘
                           │
                           ▼  Xóa duplicate (N = 15)
┌─────────────────────────────────────────────────────────┐
│               Sau khi xóa duplicate                      │
│                      N = 108                             │
└──────────────────────────┬──────────────────────────────┘
                           │
                           ▼  Vòng 1: Title + Abstract Screening
              ┌────────────┴────────────┐
              ▼                         ▼
┌─────────────────────┐    ┌───────────────────────────────┐
│  Records screened   │    │  Excluded (N = 86)             │
│     (N = 108)       │    │  EC1 – Duplicate (N = 1)       │
│                     │    │  EC4 – Test execution/         │
│  INCLUDE: N = 37    │    │        maintenance only        │
│                     │    │        (N = 85)                │
└──────────┬──────────┘    └───────────────────────────────┘
           │
           ▼  Vòng 2: Full-text Screening
┌─────────────────────────────────────────────────────────┐
│                Full-text assessed (N = 37)               │
└──────────────────────────┬──────────────────────────────┘
                           │
              ┌────────────┴────────────┐
              ▼                         ▼
┌─────────────────────┐    ┌───────────────────────────────┐
│  Included in        │    │  Excluded (N = 2)              │
│  Evidence Table     │    │  EC4 – Out of scope BDD/LLM    │
│     (N = 35)        │    │        test generation (N = 2) │
└─────────────────────┘    └───────────────────────────────┘
```

---

## Ghi chú

- **String A:** IEEE Xplore export ngày 27/05/2026 — 35 records
- **String B:** IEEE Xplore export ngày 31/05/2026 — 103 records
- **15 records** xuất hiện ở cả hai search strings (String A & String B) → xóa duplicate
- **37 records** pass Vòng 1 (INCLUDE) → tiến hành full-text review
- **35 papers** được đưa vào Evidence Table sau full-text screening

| Bước | N |
|------|---|
| Records identified | 123 |
| After duplicate removal | 108 |
| Passed Vòng 1 (INCLUDE) | 37 |
| Excluded Vòng 1 | 86 |
| — EC1: Duplicate | 1 |
| — EC4: Test execution/maintenance only | 85 |
| Passed Vòng 2 (INCLUDE) | 35 |
| Excluded Vòng 2 | 2 |
| — EC4: Out of scope | 2 |
| **Final included in Evidence Table** | **35** |
