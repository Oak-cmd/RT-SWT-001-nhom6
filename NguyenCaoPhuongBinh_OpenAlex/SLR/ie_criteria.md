# IE Criteria — Automated BDD and Gherkin Test Generation using LLMs
**Thành viên:** Nguyễn Cao Phương Bình
**RQ:** "Liệu GPT-4o (zero-shot, temperature=0) có thể sinh kịch bản BDD/Gherkin đạt Cosine Similarity >= 0.85 và Executable Rate >= 80% từ User Story format Connextra không?"
**PICO:** P=User Stories (Connextra format) | I=GPT-4o (zero-shot, temp=0) generating BDD/Gherkin | C=Expert-written scenarios / Other LLMs (GPT-4, Gemini, Claude) | O=Semantic Similarity & Syntactic Executable Rate

---

## Inclusion Criteria (IC) — paper PHẢI có đủ tất cả

| Mã | Tiêu chí |
| :--- | :--- |
| **IC-L** | Viết bằng tiếng Anh |
| **IC-Y** | Xuất bản từ 2018 đến nay — Lý do: LLM trong SE là lĩnh vực tiến triển cực nhanh, các nghiên cứu trước 2018 không còn tính thời sự cho GPT-4o. |
| **IC-T** | Đăng trên conference hoặc journal có phản biện (Peer-reviewed). |
| **IC-P** | Về task: Tự động tạo kịch bản kiểm thử (test scenarios) hoặc acceptance tests từ yêu cầu người dùng (PICO.P). |
| **IC-I** | Dùng kỹ thuật: Sử dụng Large Language Models (LLMs) và framework Behavior-Driven Development (BDD/Gherkin) (PICO.I). |
| **IC-E** | Có ít nhất 1 con số kết quả thực nghiệm về hiệu suất (thời gian, độ chính xác, coverage) trong Table hoặc Figure của paper gốc. |

## Exclusion Criteria (EC) — loại nếu BẤT KỲ điều kiện nào đúng

| Mã | Tiêu chí |
| :--- | :--- |
| **EC-D** | Trùng lặp với paper đã có trong danh sách (Deduplication). |
| **EC-A** | Không truy cập được full-text (Paywall hoặc không tìm thấy PDF/Text). |
| **EC-S** | Dưới 4 trang (extended abstract, poster, short paper, hoặc podcast show notes). |
| **EC-N** | Không có thực nghiệm định lượng (position paper, vision paper, tutorial, hoặc chỉ là opinion). |
| **EC-O** | Không về topic: Chỉ tập trung vào bảo trì test (maintenance) hoặc thực thi test (execution) mà không có khâu sinh (generation) tự động. |
| **EC-Dom**| Ngoài phạm vi (Domain): Nghiên cứu áp dụng cho thiết kế phần cứng (Hardware design) thay vì kỹ thuật phần mềm (Software Engineering). |