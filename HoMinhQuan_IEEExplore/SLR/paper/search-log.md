# Search Log — LLM for Acceptance Test Automation (BDD/Gherkin)
Thành viên: Hồ Minh Quân 
Ngày thực hiện: 2026-06-07

---

## Chuỗi tìm kiếm (Query Strings)

### String A
Query nguyên văn: `("user story" OR "requirements") AND ("Gherkin" OR "BDD") AND ("generation" OR "automation")`  
Database: IEEE Xplore / OpenAlex  
Bộ lọc: Không có bộ lọc  
Ngày search: 2026-06-07  
Số kết quả: 35

---

### String B
Query nguyên văn: `("Gherkin" OR "BDD") AND ("semantic similarity" OR "quality")`  
Database: IEEE Xplore / OpenAlex  
Bộ lọc: Không có bộ lọc  
Ngày search: 2026-06-07  
Số kết quả: 103

---

## Tổng hợp trước dedup

| Database | String | Kết quả |
| :---- | :---- | :---- |
| IEEE/OpenAlex | String A | 35 |
| IEEE/OpenAlex | String B | 103 |
| Tổng trước dedup | | 138 |
| Sau dedup (Thực tế) | | 123 |
| Số bị loại (Trùng lặp) | | 15 |

---

## Ghi chú về kết quả sàng lọc (Screening)

Dựa trên quy trình sàng lọc qua các file:

- **Tổng số bản ghi ban đầu:** 123 bài báo độc nhất
- **Sàng lọc V1 (Sơ bộ):** Có 37 bài báo được chọn (INCLUDE) và 86 bài bị loại — chủ yếu do tiêu chí EC4 (không liên quan đến sinh test, N = 85) hoặc EC1 (vi phạm nguyên tắc xuất bản, N = 1)
- **Sàng lọc V2 (Cuối cùng):** Sau khi thẩm định kỹ nội dung, còn lại **35 bài báo** được đưa vào kết luận cuối cùng (ID 11 và ID 115 đã bị loại ở giai đoạn này do chỉ bàn về thực thi hoặc quản lý thay vì sinh test)

---

## Danh sách tài liệu và Liên kết tải về

### ✅ Các bài báo có thể tải PDF tự do (IEEE Access — Open Access)

| ID | Authors | Title | Year | Venue | DOI | PDF Link |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
2. D. T. Penagos; N. Agudelo | Agile testing using user language automation with artificial intelligence in Enjisst | 2024 | 2024 IEEE Latin American Conference on Computational Intelligence (LA-CCI) | 10.1109/LA-CCI62337.2024.10814749 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10814749
3. K. Waitchasarn; A. Thongtak; T. Suwannasart | Generating Robot Framework Test Scripts from User Stories and Scenarios for Web Application Testing | 2023 | 2023 8th International Conference on Computer and Communication Systems (ICCCS) | 10.1109/ICCCS57501.2023.10151185 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10151185
4. M. Alferez; F. Pastore; M. Sabetzadeh; L. Briand; J. -R. Riccardi | Bridging the Gap between Requirements Modeling and Behavior-Driven Development | 2019 | 2019 ACM/IEEE 22nd International Conference on Model Driven Engineering Languages and Systems (MODELS) | 10.1109/MODELS.2019.00008 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=8906976
6. D. Stojanović; B. Pavković; N. Četić; M. Krunić; L. Vidaković | Unit Test Generation Multi-Agent AI System for Enhancing Software Documentation and Code Coverage | 2024 | 2024 32nd Telecommunications Forum (TELFOR) | 10.1109/TELFOR63250.2024.10819096 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10819096
7. P. von Olberg; L. Strey | Approach to Generating Functional Test Cases from BPMN Process Diagrams | 2022 | 2022 IEEE 30th International Requirements Engineering Conference Workshops (REW) | 10.1109/REW56159.2022.00042 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=9920124
9. A. A. Babikian; B. Chen; G. Mussbacher | Exploring Large Language Models for Requirements on String Values | 2025 | 2025 IEEE/ACM Workshop on Multi-disciplinary, Open, and RElevant Requirements Engineering (MO2RE) | 10.1109/MO2RE66661.2025.00009 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=11028238
10. S. B. Patel; S. Nigam; S. Mahale | Reverse-Engineering and Automating BDD for Modern Software Development with LLMs | 2025 | 2025 IEEE International Conference on Data and Software Engineering (ICoDSE) | 10.1109/ICoDSE68111.2025.11351772 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=11351772
11. E. Lee; J. Gong; Q. Cao | Object Oriented BDD and Executable Human-Language Module Specification | 2023 | 2023 26th ACIS International Winter Conference on Software Engineering, Artificial Intelligence, Networking and Parallel/Distributed Computing (SNPD-Winter) | 10.1109/SNPD-Winter57765.2023.10223873 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10223873
12. P. L. Fonseca; B. Lima; J. P. Faria | Streamlining Acceptance Test Generation for Mobile Applications Through Large Language Models: An Industrial Case Study | 2025 | 2025 40th IEEE/ACM International Conference on Automated Software Engineering (ASE) | 10.1109/ASE63991.2025.00273 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=11334650
13. Y. Hachaïchi; M. A. Ouerghi | The Role of Machine Learning and Large Language Models in Software Testing and Validation | 2025 | 2025 IEEE 22nd International Conference on Sciences and Techniques of Automatic Control and Computer Engineering (STA) | 10.1109/STA66620.2025.11364940 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=11364940
15. T. Storer; R. Bob | Behave Nicely! Automatic Generation of Code for Behaviour Driven Development Test Suites | 2019 | 2019 19th International Working Conference on Source Code Analysis and Manipulation (SCAM) | 10.1109/SCAM.2019.00033 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=8930836
16. M. Ferreira; L. Viegas; J. P. Faria; B. Lima | Acceptance Test Generation with Large Language Models: An Industrial Case Study | 2025 | 2025 IEEE/ACM International Conference on Automation of Software Test (AST) | 10.1109/AST66626.2025.00007 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=11081451
17. A. Chatterjee | AI driven Test Scenario Generator | 2025 | 2025 5th International Conference on Information Communication and Software Engineering (ICICSE) | 10.1109/ICICSE66971.2025.11430054 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=11430054
20. J. You; J. Tong; T. Yang; H. Wang | Test Requirement Modeling and Verification Method Oriented Towards Intelligent Characteristics of Autonomous Unmanned Equipment | 2025 | 2025 5th International Conference on Electronic Information Engineering and Computer Communication (EIECC) | 10.1109/EIECC67963.2025.11409501 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=11409501
28. J. Jagielski; C. Rojas; M. Abel | Exploratory Study on Private GPTs for LLM-Driven Test Generation in Software and Machine Learning Development | 2025 | 2025 2nd International Generative AI and Computational Language Modelling Conference (GACLM) | 10.1109/GACLM67198.2025.11232354 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=11232354
35. M. Nguyen; S. Wrede; N. Hochgeschwender | Automated Behaviour-Driven Acceptance Testing of Robotic Systems | 2025 | 2025 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS) | 10.1109/IROS60139.2025.11246121 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=11246121
38. S. S. Murugan; M. Balamurugan | Semantic-Contextual Automation of Scriptless BDD Testing for Intelligent Test Coverage Enhancement | 2025 | 2025 6th International Conference on Communication, Computing & Industry 6.0 (C2I6) | 10.1109/C2I666499.2025.11366954 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=11366954
41. O. Dukić; O. Ristić | Agentic BDD Testing of Dialog Systems: Stabilizing the Dialog Manager via Failure-Driven Evolution | 2025 | 2025 33rd Telecommunications Forum (TELFOR) | 10.1109/TELFOR67910.2025.11314366 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=11314366
48. R. K. C. Ragel; F. F. Balahadia | Visual Test Framework: Enhancing Software Test Automation with Visual Artificial Intelligence and Behavioral Driven Development | 2023 | 2023 IEEE 15th International Conference on Humanoid, Nanotechnology, Information Technology, Communication and Control, Environment, and Management (HNICEM) | 10.1109/HNICEM60674.2023.10589222 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10589222
50. N. Alinezhadtilaki; C. Evans | Assessing the Quality of Behavior-Driven Development Scenarios Using BERT | 2025 | 2025 IEEE 4th International Conference on Computing and Machine Intelligence (ICMI) | 10.1109/ICMI65310.2025.11141197 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=11141197
53. M. Galloy; M. Balfroid; B. Vanderose; X. Devroey | SelfBehave, Generating a Synthetic Behaviour-Driven Development Dataset using SELF-INSTRUCT | 2025 | 2025 IEEE International Conference on Software Testing, Verification and Validation Workshops (ICSTW) | 10.1109/ICSTW64639.2025.10962479 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10962479
54. J. Quispe; H. Cordova; L. Wong | Approach for Generating and Executing Acceptance Tests Based on Computer Vision and GPT-4 | 2026 | 2026 8th International Conference on Software Engineering and Computer Science (CSECS) | 10.1109/CSECS69124.2026.11541611 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=11541611
55. L. I. Matveeva; V. Kunštár; K. Jelemenská; P. Čičák | Comparison of Methods for Automated BDD Scenario Generation with NLP and AI | 2025 | 2025 5th International Conference on Electrical, Computer, Communications and Mechatronics Engineering (ICECCME) | 10.1109/ICECCME64568.2025.11277590 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=11277590
58. H. R. Lima; K. C. Souza; L. V. de Paula; L. M. C. e Martins; W. F. Giozza; R. T. de Sousa | Acceptance Tests over Microservices Architecture using Behaviour-Driven Development | 2021 | 2021 16th Iberian Conference on Information Systems and Technologies (CISTI) | 10.23919/CISTI52073.2021.9476643 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=9476643
60. R. Broer Bahaweres; E. Oktaviani; L. Kesuma Wardhani; I. Hermadi; A. Suroso; I. Permana Solihin; Y. Arkeman | Behavior-driven development (BDD) Cucumber Katalon for Automation GUI testing case CURA and Swag Labs | 2020 | 2020 International Conference on Informatics, Multimedia, Cyber and Information System (ICIMCIS) | 10.1109/ICIMCIS51567.2020.9354325 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=9354325
61. L. Chemnitz; D. Reichenbach; H. Aldebes; M. Naveed; K. Narasimhan; M. Mezini | Towards Code Generation from BDD Test Case Specifications: A Vision | 2023 | 2023 IEEE/ACM 2nd International Conference on AI Engineering – Software Engineering for AI (CAIN) | 10.1109/CAIN58948.2023.00031 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10164755
63. R. Ramler; C. Klammer | Enhancing Acceptance Test-Driven Development with Model-Based Test Generation | 2019 | 2019 IEEE 19th International Conference on Software Quality, Reliability and Security Companion (QRS-C) | 10.1109/QRS-C.2019.00096 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=8859410
65. Y. Wang; L. Jia; H. Cao; Z. Jing; H. Huang | Applications of Cucumber on Automated Functional Simulation Testing | 2021 | 2021 IEEE 21st International Conference on Software Quality, Reliability and Security Companion (QRS-C) | 10.1109/QRS-C55045.2021.00129 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=9741911
69. J. Xu; Q. Du; X. Li | A Requirement-based Regression Test Selection Technique in Behavior-Driven Development | 2021 | 2021 IEEE 45th Annual Computers, Software, and Applications Conference (COMPSAC) | 10.1109/COMPSAC51774.2021.00182 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=9529903
79. A. Chatterjee | Codeless and Scalable Solution For Microservice Test Automation | 2025 | 2025 5th International Conference on Information Communication and Software Engineering (ICICSE) | 10.1109/ICICSE66971.2025.11429894 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=11429894
83. Y. -J. Guo; S. -P. Ma; H. -J. Peng; Y. -S. Su | API Test Case Generation by Extracting HTTP Requests During Front-End Testing | 2024 | 2024 IEEE International Conference on e-Business Engineering (ICEBE) | 10.1109/ICEBE62490.2024.00013 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10784388
88. Y. Xiao; K. Zhang; J. Wang; X. Sheng; Y. Guo; M. Chen; Z. Ren; Z. Zheng; Z. Zhao | A Segmentation-Driven Editing Method for Bolt Defect Augmentation and Detection | 2026 | IEEE Transactions on Systems, Man, and Cybernetics: Systems | 10.1109/TSMC.2026.3655553 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=11372954
90. M. G. D. Santos; F. Petrillo; S. Hallé; Y. -G. Guéhéneuc | An approach to apply Automated Acceptance Testing for Industrial Robotic Systems | 2022 | 2022 Sixth IEEE International Conference on Robotic Computing (IRC) | 10.1109/IRC55401.2022.00066 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10023744
91. I. Yanjari; B. Marín; G. Giachetti | An open-source framework for cross-platform testing in agile projects | 2022 | 2022 41st International Conference of the Chilean Computer Science Society (SCCC) | 10.1109/SCCC57464.2022.10000346 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10000346
96. L. Riquelme; M. González; N. Aquino; L. Cernuzzi | MoFQA: An Approach for Automatic TDD Test Case Generation from MDD Models | 2018 | 2018 XLIV Latin American Computer Conference (CLEI) | 10.1109/CLEI.2018.00012 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=8786314
114. W. Ravelo-Méndez; C. Escobar-Vélasquez; M. Linares-Vásquez | Kraken-Mobile: Cross-Device Interaction-Based Testing of Android Apps | 2019 | 2019 IEEE International Conference on Software Maintenance and Evolution (ICSME) | 10.1109/ICSME.2019.00071 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=8918941
115. J. Saraiva; S. Soares | Privacy and Security Documents for Agile Software Engineering: An Experiment of LGPD Inventory Adoption | 2023 | 2023 ACM/IEEE International Symposium on Empirical Software Engineering and Measurement (ESEM) | 10.1109/ESEM56168.2023.10304806 | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10304806





