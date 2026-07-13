# PRISMA Flow Diagram — Automated BDD/Gherkin Test Generation

[Records từ database searching (N = 73)]  ← Tổng từ 11 Search Strings (A-K)
            ↓
[Sau khi xóa duplicate (N = 41)]  ← Số dòng trong 01_all_records.csv
            ↓
┌───────────────────────────────────────────────┐
│ Screened title + abstract (N = 41)            │
│  └─ Excluded (N = 5):                         │
│     EC-O=1 (ID 3), EC-Dom=1 (ID 17),          │
│     EC-N=2 (ID 19, 24), EC-S=1 (ID 31)        │
└───────────────────────────────────────────────┘
            ↓ 36 papers pass  ← Tổng (INCLUDE + UNSURE) trong 02_after_screening
            ↓
┌───────────────────────────────────────────────┐
│ Full-text assessed (N = 36)                   │
│  └─ Excluded (N = 17):                        │
│     EC-A=17 (No PDF / Paywall)                │
└───────────────────────────────────────────────┘
            ↓
[Final included (N = 19)]  ← Quyết định INCLUDE trong 03_final_included.csv

---

### Kiểm tra nhất quán (Self-check):

- **N sau dedup:** 41 (Khớp với số lượng bản ghi duy nhất ban đầu).
- **Excluded vòng 1:** 5 (Loại bỏ các bài không liên quan đến sinh test, domain phần cứng, SLR, hoặc podcast).
- **Full-text assessed:** 36 (Bao gồm 33 bài INCLUDE và 3 bài UNSURE từ V1).
- **Excluded vòng 2:** 17 (Loại bỏ do không có PDF hoặc bị chặn bởi Paywall theo tệp EXCLUDEs.txt).
- **Final included:** 19 (Các bài báo đã được đọc toàn văn PDF/Text và xác nhận đáp ứng đủ tiêu chí IC-L đến IC-E).