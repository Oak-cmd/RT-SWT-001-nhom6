# Search Log - AI-Assisted Feedback Analysis for Software Requirements Validation and Improvement

**Thành viên:** Nguyễn Minh
**Ngày thực hiện:** 2026-06-01 đến 2026-06-07

---

## Chuỗi tìm kiếm (Query Strings)

### String A

**Query nguyên văn:**

("user feedback" OR "customer feedback" OR "app reviews") AND ("requirements engineering" OR "software requirements")

**Database:** ACM Digital Library

**Bộ lọc:**
- Publication Year: 2018–2026
- Language: English
- Peer-reviewed publications

**Ngày search:** 2026-06-01

**Số kết quả:** 35 papers

---

### String B

**Query nguyên văn:**

("requirements validation" OR "requirements verification") AND ("artificial intelligence" OR "machine learning")

**Database:** ACM Digital Library

**Bộ lọc:** Same as String A

**Ngày search:** 2026-06-01

**Số kết quả:** 28 papers

---

### String C

**Query nguyên văn:**

("software requirements") AND ("large language model" OR "LLM" OR "GPT")

**Database:** ACM Digital Library

**Bộ lọc:** Same as String A

**Ngày search:** 2026-06-01

**Số kết quả:** 22 papers

---

### String D

**Query nguyên văn:**

("requirements elicitation" OR "requirements analysis") AND ("user feedback")

**Database:** ACM Digital Library

**Bộ lọc:** Same as String A

**Ngày search:** 2026-06-02

**Số kết quả:** 18 papers

---

### String E

**Query nguyên văn:**

("feedback analysis") AND ("requirements improvement")

**Database:** ACM Digital Library

**Bộ lọc:** Same as String A

**Ngày search:** 2026-06-02

**Số kết quả:** 16 papers

---

### String F

**Query nguyên văn:**

("app review mining") AND ("requirements engineering")

**Database:** ACM Digital Library

**Bộ lọc:** Same as String A

**Ngày search:** 2026-06-02

**Số kết quả:** 20 papers

---

### String G

**Query nguyên văn:**

("AI-assisted") AND ("requirements validation")

**Database:** ACM Digital Library

**Bộ lọc:** Same as String A

**Ngày search:** 2026-06-03

**Số kết quả:** 14 papers

---

### String H

**Query nguyên văn:**

("large language model" OR "GPT") AND ("requirements engineering")

**Database:** ACM Digital Library

**Bộ lọc:** Same as String A

**Ngày search:** 2026-06-03

**Số kết quả:** 17 papers

---

### String I

**Query nguyên văn:**

("requirements quality") AND ("artificial intelligence")

**Database:** ACM Digital Library

**Bộ lọc:** Same as String A

**Ngày search:** 2026-06-03

**Số kết quả:** 12 papers

---

### String J

**Query nguyên văn:**

("requirements improvement") AND ("machine learning" OR "LLM")

**Database:** ACM Digital Library

**Bộ lọc:** Same as String A

**Ngày search:** 2026-06-04

**Số kết quả:** 10 papers

---

### String K

**Query nguyên văn:**

("feedback-driven development") AND ("requirements engineering")

**Database:** ACM Digital Library

**Bộ lọc:** Same as String A

**Ngày search:** 2026-06-04

**Số kết quả:** 8 papers

---

# Tổng hợp trước Dedup

| Database | String | Kết quả |
|:----------|:----------|---------:|
| ACM Digital Library | String A | 35 |
| ACM Digital Library | String B | 28 |
| ACM Digital Library | String C | 22 |
| ACM Digital Library | String D | 18 |
| ACM Digital Library | String E | 16 |
| ACM Digital Library | String F | 20 |
| ACM Digital Library | String G | 14 |
| ACM Digital Library | String H | 17 |
| ACM Digital Library | String I | 12 |
| ACM Digital Library | String J | 10 |
| ACM Digital Library | String K | 8 |
| **Tổng trước dedup** | | **200** |
| **Sau dedup** | | **200** |
| **Số bị loại (trùng lặp)** | | **0** |

---

## Phần S – Cross-reference Search (Snowballing)

**Phương pháp:** Backward snowballing – xem xét danh mục tài liệu tham khảo của các nghiên cứu vượt qua vòng V2 Screening.

**Thực hiện:** Sau khi hoàn thành `03_final_included.csv`.

**Công cụ:** ACM Digital Library

**Ngày thực hiện:** 2026-06-07

**Paper included đã scan:** 18 papers

**Paper mới phát hiện:** 0 papers

**Paper pass V2:** 0 papers

---

## Ghi chú

### Screening Summary

| Stage | Records |
|---------|---------:|
| Records identified | 200 |
| Duplicates removed | 0 |
| Records screened (V1) | 200 |
| Excluded in V1 | 14 |
| Full-text assessed (V2) | 186 |
| Excluded in V2 | 154 |
| Passed V2 | 32 |
| Included in Evidence Table | 18 |

### Tiêu chí loại ở V1

- Vi phạm IC-N (Published before 2018): 14 papers

### Tiêu chí loại ở V2

- Vi phạm IC-O (Out of Scope)
- Không đáp ứng IC4 (Không liên quan trực tiếp đến AI-assisted requirements validation and improvement)
- Vi phạm EC3 (Thiếu đóng góp kỹ thuật hoặc không phải nghiên cứu thực nghiệm)
- Vi phạm EC2 (Không truy cập được toàn văn)

### Phương pháp Dedup

Thực hiện bằng Microsoft Excel dựa trên:
- Title
- Authors
- Publication Year

### Snowballing

Không phát hiện thêm nghiên cứu nào đáp ứng toàn bộ tiêu chí lựa chọn. Do đó tập nghiên cứu cuối cùng vẫn gồm **18 papers**.

### Kết quả cuối cùng

18 nghiên cứu cuối cùng được sử dụng cho:
- Evidence Extraction
- Gap Identification
- Research Question Analysis
- Synthesis and Discussion

Toàn bộ quy trình lựa chọn nghiên cứu tuân theo PRISMA Flow Diagram được xây dựng trong `prisma-flow.md`.