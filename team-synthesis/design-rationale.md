\# Experiment Design Rationale \- LLM for Acceptance Test Automation  
Ngày: 2026-06-16 | GAP source: gap-analysis.md

\#\# Bảng Quyết Định

| Quyết định | Giá trị | Nguồn gốc |  
| :--- | :--- | :--- |  
| LLM/Tool | GPT-4o (version: gpt-4o-2024-05-13), Zero-shot, Temperature \= 0 | GAP-T: cột Tool/LLM (Cô lập năng lực gốc và đảm bảo tính tái lập) |  
| Dataset | Tập dữ liệu UFCG/VIRTUS chuẩn hóa sang định dạng Connextra User Stories (372 mẫu) | GAP-D / kế thừa từ Paper 6 và Paper 16 |  
| Metric chính | Cosine similarity tính bằng \`sentence-transformers/all-MiniLM-L6-v2\` | GAP-M: cột Metric (Đo lường độ tương đồng ngữ nghĩa) |  
| Metric phụ | Executable rate tính bằng \`behave 1.2.6\` \+ \`subprocess\` capture BLEU-4 tính bằng \`sacrebleu 2.3\` | Kế thừa từ Paper 6 (Cú pháp Gherkin) và Paper 4 (BLEU) |  
| Baseline type | Comparative & Human-level (So sánh đối chứng với Kịch bản Gherkin chuẩn do chuyên gia soạn thảo) | Claim type của RQ (Xác định năng lực tiệm cận chuyên gia) |  
| Threshold RQ1 | Cosine Similarity $0.80 | Case 3: Không có kết quả số từ trước (GAP-M), chạy mini-pilot 10 mẫu |  
| Threshold RQ2 | Executable Rate $90% | Case 2: Lấy giá trị sàn (floor value) từ kết quả của Paper 6 (SBES 2025\) |  
| Pipeline base | Cấu hình đánh giá độc lập mô hình theo Paper 4 (WEBIST 2025\) | Chọn Paper 4 vì có cùng hệ sinh thái thực nghiệm so sánh LLM |

\#\# Lý giải lựa chọn Metric chính  
 \*\*Tại sao chọn Cosine Similarity thay vì BLEU-4 làm metric chính:\*\* Cú pháp của kịch bản Gherkin cực kỳ linh hoạt (flexible syntax). Một kịch bản sinh ra có thể hoàn toàn đúng về mặt ngữ nghĩa và logic doanh nghiệp nhưng sử dụng tập từ vựng khác biệt so với nhãn chuyên gia, khiến BLEU-4 (vốn dựa trên lexical n-gram overlap) phạt điểm sai (penalize). Cosine similarity thông qua mô hình vector hóa ngữ nghĩa \`all-MiniLM-L6-v2\` mang lại tính trực giao và robust cao hơn trước các hiện tượng diễn đạt lại (paraphrase).

\#\# Lý giải threshold

 \*\*Threshold RQ1 (Cosine Similarity $\\ge$ 0.80) – Case 3:\*\* Do hiện tượng khuyết thiếu dữ liệu đo lường ngữ nghĩa trong y văn (Semantic Evaluation Gap), không có nghiên cứu đi trước báo cáo chỉ số cosine cụ thể cho tác vụ này. Nhóm nghiên cứu đã thực hiện một khảo sát thử nghiệm quy mô nhỏ (mini-pilot) gồm 10 mẫu thủ công trước khi nộp đề xuất (pre-proposal). Kết quả cho thấy mức tương đồng ngữ nghĩa 0.80 là điểm sàn phản ánh độ bảo toàn logic nghiệp vụ chính xác của mô hình mà không bị ảnh hưởng bởi nhiễu diễn đạt.

 \*\*Threshold RQ2 (Executable Rate $\\ge$ 90%) – Case 2:\*\* Dựa trên bảng thống kê thực nghiệm của các nghiên cứu đi trước, Paper 6 (SBES 2025\) báo cáo rằng các mô hình ngôn ngữ lớn đạt độ chính xác cú pháp tốt hơn hẳn tác vụ thủ công và đạt mốc "\>90% syntax accuracy cho các kịch bản tiêu chuẩn". Do bài báo này không thiết lập một ngưỡng đạt/trượt (pass/fail) tường minh, chúng tôi áp dụng quy tắc Case 2, trích xuất giá trị thấp nhất (floor \= 90% từ Paper 6\) làm ngưỡng threshold bắt buộc mà cấu hình deterministic của GPT-4o phải vượt qua.

\#\# Giả thuyết khoa học (Hypothesis) & Kiểm định thống kê (Statistical Test)

 \*\*Đối với RQ1 (Độ tương đồng ngữ nghĩa \- Đầu ra liên tục):\*\*  
   \*\*Giả thuyết:\*\*   
    H\_0: Điểm Cosine Similarity của kịch bản do GPT-4o sinh ra có giá trị trung vị nhỏ hơn hoặc bằng 0.80.  
    H\_1: Điểm Cosine Similarity của kịch bản do GPT-4o sinh ra có giá trị trung vị lớn hơn 0.80 (Mô hình bảo toàn ngữ nghĩa vượt ngưỡng kỳ vọng).  
   \*\*Kiểm định thống kê:\*\* Sử dụng kiểm định \*\*Wilcoxon signed-rank test\*\* (do phân phối điểm số tương đồng ngữ nghĩa thường lệch và là dữ liệu liên tục phụ thuộc).

 \*\*Đối với RQ2 (Tính đúng đắn cú pháp thực thi \- Đầu ra nhị phân Pass/Fail):\*\*  
   \*\*Giả thuyết:\*\*  
    H\_0: Tỷ lệ kịch bản chạy thành công không lỗi cú pháp (Executable Rate) của GPT-4o $\\le$ 90%.  
    H\_1: Tỷ lệ kịch bản chạy thành công không lỗi cú pháp (Executable Rate) của GPT-4o $\>$ 90% (Vượt qua giá trị sàn của thế hệ mô hình cũ).  
   \*\*Kiểm định thống kê:\*\* Sử dụng kiểm định \*\*Binomial exact test\*\* để đánh giá tỷ lệ thành công trên tổng số mẫu thực nghiệm nhị phân độc lập.