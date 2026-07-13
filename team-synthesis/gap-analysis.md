# GAP Analysis - LLM for Acceptance Test Automation
Evidence table: N = 24 paper | Ngày: 2026-05-31

## Bảng GAP

| Cột | Phát hiện | Loại GAP | Phản chứng |
| :--- | :--- | :--- | :--- |
| Tool/LLM | Thiếu cấu hình thực nghiệm zero-shot mang tính xác định cao (temperature = 0) để cô lập năng lực gốc của GPT-4o. | GAP-T | ✅ Kiểm tra 24 paper |
| Dataset | Các nghiên cứu có xu hướng sử dụng tập dữ liệu nội bộ/đóng (proprietary datasets), gây cản trở khả năng tái lập. | GAP-D | ✅ |
| Metric | Chưa kết hợp đồng thời kiểm tra cú pháp thực thi và đo lường độ tương đồng ngữ nghĩa bằng embedding làm chỉ số chính. | GAP-M | ✅ |
| Hạn chế | Nhiều bài báo tự thừa nhận kết quả bị không xác định (non-deterministic) hoặc thiếu benchmark công khai để đối chứng. | GAP-S | ✅ |

## GAP Chính: [GAP-S]
Hiện tại chưa có nghiên cứu thực nghiệm nào đánh giá cấu hình zero-shot hoàn toàn mã nguồn mở và có tính xác định cao (temperature = 0) của GPT-4o trong việc sinh kịch bản Gherkin từ user story nhằm đảm bảo tính tái lập (reproducibility).

## GAP Secondary (nếu có): [GAP-M]
Thiếu một khung đánh giá toàn diện kết hợp đồng thời cả tính đúng đắn cú pháp (executable syntax validation) và độ bảo toàn ngữ nghĩa dựa trên không gian vector (embedding-based semantic similarity).

## Chi tiết kiểm tra phản chứng
| Paper | Đã làm không? | Ghi chú |
| :--- | :--- | :--- |
| Paper 4 (WEBIST · 2025) | Không | Đánh giá GPT-4o nhưng thừa nhận đầu ra bị non-deterministic qua các lần chạy (chưa khóa temperature = 0). |
| Paper 5 (IEEE Access · 2025) | Không | Sử dụng GPT-4o nhưng áp dụng kỹ thuật few-shot chain prompting phức tạp thay vì zero-shot baseline. |
| Paper 8 (IEEE/ACM AST · 2025) | Không | Kiểm thử trên dữ liệu đóng của doanh nghiệp đối tác thông qua pipeline AutoUAT + Test Flow, không thể tái lập công khai. |
| Paper 12 (arXiv · 2026) | Không | Thử nghiệm cấu hình zero-shot nhưng chạy trên 500 user stories nội bộ, tự xác nhận hạn chế về khả năng tái lập và thiếu benchmark công khai. |
| Paper 16 (SBES · 2025) | Không | Sử dụng biến thể GPT-4o Mini đi kèm với kỹ thuật tối ưu hóa prompt tùy chỉnh (US-Prompt) thay vì cấu hình zero-shot tiêu chuẩn. |

## Feasibility Check – GAP Chính
| Tiêu chí | Mức | Ghi chú |
| :--- | :--- | :--- |
| Dataset | ✅ | Có thể sử dụng tập dữ liệu công khai sẵn có (như dữ liệu UFCG/VIRTUS của Paper 6) hoặc tập mẫu chuẩn định dạng Connextra. |
| Tool/API | ⚠️ | Cần trả phí bản quyền gọi API cho GPT-4o, tuy nhiên tổng chi phí thực nghiệm cho tập mẫu zero-shot là rất nhỏ (< $5). |
| Compute | ✅ | Việc gọi API và chạy các script đo lường metric không yêu cầu huấn luyện mô hình, môi trường CPU hoặc Google Colab miễn phí là đủ. |
| Ground truth | ✅ | Việc kiểm tra cú pháp Gherkin có thể tự động hóa qua thư viện/parser, nhãn tương đồng ngữ nghĩa tính bằng mô hình embedding có sẵn. |
| Skills | ✅ | Đội ngũ có khả năng làm chủ các thư viện Python cơ bản phục vụ gọi API, xử lý chuỗi và tính toán khoảng cách vector ngữ nghĩa. |
| Thời gian | ✅ | Kiến trúc zero-shot tối giản, loại bỏ các bước tinh chỉnh (fine-tuning) hay RAG phức tạp, đảm bảo hoàn thành sớm và có buffer > 1 tuần. |
| Contribution | ✅ | Cung cấp một kết quả baseline nền tảng, minh bạch và có tính xác định cao để cộng đồng nghiên cứu SE có thể đối chứng và tái lập trực tiếp. |

**Kết quả:** [0] ❌ / [1] ⚠️ -> [An toàn]