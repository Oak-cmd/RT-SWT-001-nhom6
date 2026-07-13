# PRISMA Flowchart

**Topic:** LLM for Acceptance Test Automation (BDD/Gherkin)

```
┌──────────────────────────────────────────┐
│        Records từ database searching     │
│  String A (google scholar): 20           │
│  String B (google scholar): 20           │
│  String C (google scholar): 10           │
│  Tổng: 50                               │
└──────────────────┬───────────────────────┘
                   │
                   ▼
┌──────────────────────────────────────────┐
│         Sau khi xóa duplicate            │
│              (N = 46)                    │
└──────────────────┬───────────────────────┘
                   │
                   ▼ Vòng 1: Title + Abstract Screening
┌──────────────────────────────────────────┐
│         Records được screening           │
│              (N = 11)                    │
└──────────────────┬───────────────────────┘
                   │
        ┌──────────┴──────────┐
        ▼                     ▼
┌──────────────┐    ┌───────────────────────┐
│  INCLUDE +   │    │  Excluded (N = 35)    │
│  UNSURE      │    │  Reasons: EC1, 3, 5   │
│  (N = 11)    │    │           IC2 - IC5   │
└──────┬───────┘    └───────────────────────┘
       │
       ▼ Vòng 2: Full-text Screening
┌──────────────────────────────────────────┐
│     Full-text assessed (N = 8)           │
└──────────────────┬───────────────────────┘
                   │
        ┌──────────┴──────────┐
        ▼                     ▼
┌──────────────┐    ┌─────────────────────┐
│  Included    │    │  Excluded (N = 4)   │
│  trong ET    │    │  Reasons: IC2, EC4  │
│  (N = 7)     │    └─────────────────────┘
└──────────────┘
```

> Cập nhật số liệu sau khi hoàn thành screening vòng 1 và vòng 2.
