# Day 16 Submission - Phiên bản B
**Đề tài:** AI Skill-Gap Analyzer

## Members
- **Quách Gia Được** - 2A202600423

## 1. Idea reframed
**Original idea:**
> Dùng AI để tự động chấm điểm CV, sửa lỗi chính tả và thiết kế lại CV cho sinh viên mới ra trường.

**Reframed as a product opportunity:**
> Insight cốt lõi là 70% trong số 50.000 sinh viên IT ra trường mỗi năm tại Việt Nam phải đào tạo lại mới làm việc được trong dự án thực tế. Việc làm đẹp CV bằng template không giải quyết được vấn đề thiếu hụt năng lực. Cơ hội thực sự là một nền tảng "Skill-gap Intelligence" để phân tích từ khóa kỹ năng trong CV đối chiếu với JD thực tế, từ đó chỉ ra những lỗ hổng công nghệ (VD: thiếu kỹ năng RAG, MLOps) và tự động đề xuất các chứng chỉ vi mô (micro-credentials) để ứng viên lấp đầy ngay lập tức.

## 2. Customer / Segment Card
- **Segment name:** Sinh viên năm 4 và Fresher ngành IT (dưới 1 năm kinh nghiệm) tại các thành phố lớn.
- **Operational context:** Bối cảnh thị trường IT 2026 cạnh tranh gay gắt, cung vượt cầu. Ứng viên rải hàng chục CV trên các nền tảng nhưng liên tục bị loại ở vòng screening.
- **Recurring workflow:** Tìm tin tuyển dụng -> Nộp CV -> Nhận email từ chối chung chung -> Hoang mang sửa lại CV -> Nộp tiếp.
- **Pain moment:** Khi bị loại hồ sơ khỏi một công ty Product yêu thích mà không nhận được feedback lý do, khiến họ mất định hướng học tập và rơi vào rủi ro thất nghiệp dài hạn.
- **Why now:** Năm 2026, yêu cầu tuyển dụng Data/AI chuyển dịch mạnh mẽ (đòi hỏi MLOps, LLMOps, Data Governance thay vì chỉ code Python cơ bản). Ứng viên bắt buộc phải nâng cấp kỹ năng liên tục để không bị đào thải.
- **Access path:** Hợp tác với các CLB học thuật (như tại ĐH Bách Khoa), các cộng đồng sinh viên IT, và các KOL hướng nghiệp.
- **One-sentence description:** > Sinh viên IT/Data mới ra trường đang tuyệt vọng vì rải CV không ai gọi, cần công cụ chỉ ra chính xác mình đang thiếu kỹ năng công nghệ gì so với thị trường khắt khe năm 2026.

## 3. Need Map (2-3 needs)
### Need #1 (priority)
- **Statement (JTBD):** When [tôi apply vào vị trí công việc mong muốn nhưng bị rớt hồ sơ], I want [biết chính xác framework hoặc công nghệ nào (ví dụ: Vector DB hay Fine-tuning) mà JD yêu cầu nhưng CV tôi chưa có], so I can [dừng rải CV vô ích và tập trung học đúng khóa học ngắn hạn để bổ sung].
- **Current workaround:** Đọc đi đọc lại JD một cách thủ công, nhắn tin hỏi những người đi trước trên LinkedIn hoặc đăng bài hỏi ẩn danh trên diễn đàn.
- **Pain signal:** Tốn nhiều tháng thất nghiệp rải CV; hoang mang và tốn tiền mua các khóa học trực tuyến không đúng trọng tâm.
- **Evidence / proxy evidence:** Việc thiếu vắng các kỹ năng nâng cao như RAG hay an ninh mạng khiến sinh viên không vượt qua được vòng lọc hồ sơ của doanh nghiệp. Sự chênh lệch giữa năng lực và đòi hỏi thực tế là cực kỳ rõ ràng.
- **Why underserved:** Các nền tảng job board hiện tại (TopCV, VietnamWorks) chỉ cung cấp tỷ lệ % matching dựa trên keyword đơn giản, không phân tích theo ngữ cảnh sâu (semantic search) để đưa ra lộ trình "vá lỗi".

### Need #2
- **Statement (JTBD):** When [tôi nhận ra mình thiếu kỹ năng thực chiến], I want [nhận được đề xuất chính xác các khóa học hoặc project mẫu có độ uy tín cao để thực hành], so I can [đưa chứng chỉ đó vào CV để tăng tỷ lệ đỗ ở lần apply tiếp theo].
- **Current workaround:** Tự tìm kiếm các khóa học trên Coursera, Udemy hoặc các trung tâm bên ngoài mà không biết khóa nào thực sự được nhà tuyển dụng Việt Nam công nhận.
- **Pain signal:** Học lan man, tốn tiền bạc nhưng CV vẫn không có "sức nặng" khi phỏng vấn.
- **Evidence / proxy evidence:** Việc học CNTT từ xa, bổ sung chứng chỉ liên tục đang là xu hướng tất yếu của ngành để thích ứng từ năm 2026 trở đi.
- **Why underserved:** Chưa có sự liên kết chặt chẽ giữa công cụ phân tích đánh giá CV và các nhà cung cấp giáo dục (E-learning).

## 4. Strategy Statement
- **For** [Sinh viên năm 4 và Fresher ngành IT/Data]
- **who struggle with** [việc liên tục trượt CV vì khoảng cách kỹ năng (skill gap) quá lớn so với yêu cầu thực tế],
- **our product helps them** [phát hiện chính xác lỗ hổng kiến thức và cung cấp lộ trình học tập tức thì]
- **through** [một hệ thống AI Agent dùng RAG đối chiếu ngữ nghĩa CV với kho dữ liệu JD thực tế của thị trường],
- **unlike** [các tính năng tính % matching hời hợt trên các trang web tuyển dụng truyền thống],
- **because we can leverage** [khả năng tổng hợp và liên kết trực tiếp các kỹ năng còn thiếu với các micro-credentials (chứng chỉ vi mô) đang có trên thị trường].

## 5. Moat Hypothesis
- **Moat mechanism:** Workflow embedding & Data Compounding (Domain-learning flywheel).
- **Flywheel mechanism:** 1. Ứng viên tải CV lên để phân tích -> Hệ thống thu thập được "khoảng trống kỹ năng" phổ biến nhất.
    2. Càng nhiều JD được đưa vào hệ thống, thuật toán bóc tách từ khóa (Market Demand Vector) càng chính xác.
    3. Hệ thống gợi ý khóa học -> Ứng viên học xong, update CV và trúng tuyển -> Thuật toán ghi nhận khóa học đó có "trọng số chuyển đổi" cao -> Lời khuyên cho ứng viên sau càng chất lượng.
- **Why competitors cannot replicate:** Đối thủ chỉ có LLM trả lời chung chung. Hệ thống của chúng ta sở hữu vòng lặp khép kín từ: Phân tích CV -> Lấp đầy kỹ năng (giáo dục) -> Kết quả tuyển dụng thực tế. 

## 6. Initial TAM/SAM/SOM view
| Layer | Estimate | Key assumptions | Confidence |
| :--- | :--- | :--- | :--- |
| **TAM** | $1.5M - $2M/year | 50.000 sinh viên IT ra trường mỗi năm. Giả định ARPPU = $30-$40/năm nếu họ trả tiền. | Medium |
| **SAM** | $300K - $400K/year | Tập trung vào top 20% sinh viên thuộc khối ngành AI/Data Science (khoảng 10.000 ứng viên) có nhu cầu cấp bách nâng cấp kỹ năng. | High |
| **SOM** | $30K - $50K/year | Đạt 1.000 - 1.500 users trả phí trong 12 tháng đầu, tập trung marketing tại ĐH Bách Khoa và các trường kỹ thuật top đầu. | Medium |

- **Top 3 unknowns:**
    1. Willingness to pay: Sinh viên IT thường có ngân sách hạn hẹp. Liệu họ có chịu trả phí định kỳ, hay mô hình nên chuyển sang Freemium (miễn phí phân tích, thu phí Affiliate từ việc bán chéo khóa học)?
    2. Data acquisition: Việc crawl dữ liệu hàng ngàn JD mới nhất mỗi ngày để làm CSDL Vector có vướng vấn đề pháp lý/điều khoản với các sàn tuyển dụng không?
    3. Tỷ lệ chuyển đổi học tập: Ứng viên biết mình thiếu kỹ năng, nhưng họ có thực sự bấm vào đăng ký học (Action) hay chỉ xem rồi bỏ qua?

- **Judgment:** [x] Worth pursuing but not now (Cần validate mô hình doanh thu Affiliate E-learning vs B2C Subscription trước tiên).

## 7. Positioning Note (2 sentences)
- **What we are:** Chúng tôi là "bác sĩ bắt bệnh" cho CV ngành IT, giúp ứng viên biết chính xác mình hổng kiến thức thực chiến nào và "kê đơn" khóa học để khắc phục.
- **What we are not / not yet:** Chúng tôi không phải là một sàn giao dịch việc làm hay một trung tâm đào tạo lập trình.

---

## 8. Cải thiện so với Phiên bản A (Iteration Reflection)
*(Dành cho Tiêu chí 5 - Iteration Quality của Day 16)*
- **Sắc bén hơn về Customer & Need:** Chuyển từ tệp khách hàng "sinh viên chung chung" sang đúng trọng tâm "Sinh viên rải CV trượt liên tục do bối cảnh thị trường IT 2026 thu hẹp". Việc này làm "Pain moment" đau và cấp bách hơn rất nhiều.
- **Đưa số liệu thực tế (Market Awareness):** Áp dụng dữ liệu thị trường thực tế (70% sinh viên IT cần đào tạo lại, xu hướng tuyển dụng đòi hỏi kỹ năng sâu như RAG, MLOps thay vì code thuần) để củng cố các luận điểm bằng chứng (Evidence), thay vì giả định.
- **Nâng cấp chiến lược Moat:** Cơ chế phòng thủ (Moat) không chỉ nằm ở việc thu thập dữ liệu, mà nâng lên thành vòng lặp (Flywheel) "Phân tích - Học tập - Đỗ phỏng vấn". Điều này biến sản phẩm từ một công cụ (tool) thành một nền tảng định hướng nghề nghiệp.
- **Xác định rủi ro kinh doanh cốt lõi:** Nhận diện rõ rủi ro sinh viên không có tiền trả (Unknown 1), từ đó chủ động mở đường cho việc cân nhắc Pivot sang mô hình kinh doanh Affiliate bán khóa học trong Day 17.
