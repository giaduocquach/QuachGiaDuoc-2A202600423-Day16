# Day 16 Submission
**Đề tài:** AI Skill-Gap Analyzer

## Members
- **Quách Gia Được** - MSSV: 2A202600423

## 1. Idea reframed
**Original idea:**
> Dùng AI để tự động chấm điểm CV, sửa lỗi chính tả và thiết kế lại CV cho sinh viên mới ra trường.

**Reframed as a product opportunity:**
> Nhận thấy việc chỉ làm đẹp CV không giúp tăng tỷ lệ trúng tuyển thực tế, cơ hội nằm ở việc xây dựng một hệ thống sử dụng NLP và Vector Similarity để phân tích "độ vênh" (skill gap) giữa CV của ứng viên và các Job Description (JD) trên thị trường. Hệ thống không chỉ chấm điểm độ khớp mà còn tự động chỉ ra các kỹ năng, chứng chỉ cốt lõi còn thiếu và đề xuất lộ trình bổ sung để tăng khả năng vượt qua vòng lọc hồ sơ.

## 2. Customer / Segment Card
- **Segment name:** Sinh viên năm cuối/mới ra trường khối ngành CNTT, Khoa học Dữ liệu (từ các trường kỹ thuật như Bách khoa) đang tìm việc Fresher/Junior.
- **Operational context:** Đang rải CV hàng loạt trên các nền tảng tuyển dụng nhưng tỷ lệ nhận được lịch phỏng vấn (conversion rate) cực kỳ thấp.
- **Recurring workflow:** Tìm tin tuyển dụng -> Nộp CV có sẵn -> Chờ đợi -> Nhận email từ chối tự động từ hệ thống của công ty.
- **Pain moment:** Thời điểm nhận email đánh trượt vòng hồ sơ mà hoàn toàn mù mờ, không biết bản thân đang hổng kỹ năng chuyên môn hay công cụ cụ thể nào so với yêu cầu của dự án đó.
- **Why now:** Doanh nghiệp đang thắt chặt ngân sách đào tạo ứng viên mới, yêu cầu ứng viên phải có sẵn các bộ từ khóa công nghệ sát với thực chiến ngay từ đầu.
- **Access path:** Tiếp cận trực tiếp qua các hội nhóm sinh viên IT, diễn đàn Data Science, hoặc mạng lưới cựu sinh viên tại trường đại học.
- **One-sentence description:** > Sinh viên khối ngành dữ liệu/công nghệ đang đánh mất cơ hội việc làm vì rải CV mù quáng mà không biết năng lực hiện tại "vênh" ở đâu so với nhu cầu thực tế của thị trường.

## 3. Need Map (2-3 needs)
### Need #1 (priority)
- **Statement (JTBD):** When [tôi apply vào một vị trí cụ thể nhưng bị loại ngay từ vòng gửi CV], I want [biết chính xác từ khóa kỹ năng nào tôi đang thiếu hoặc yếu so với JD đó], so I can [chủ động bổ sung bằng các khóa học ngắn hạn hoặc làm project cá nhân để bù đắp].
- **Current workaround:** Tự ngồi đọc JD để đoán mò, lên mạng hỏi review phỏng vấn công ty, hoặc nhắn tin hỏi anh chị đi trước (hiếm khi có câu trả lời chi tiết).
- **Pain signal:** Rải 50 CV nhưng chỉ nhận được 1-2 lịch phỏng vấn; lãng phí thời gian thất nghiệp, stress vì nghi ngờ năng lực bản thân.
- **Evidence / proxy evidence:** Tỷ lệ hồ sơ sinh viên bị loại ở vòng screening thường trên 70%. Nỗi đau này tồn tại ngay cả khi AI chưa xuất hiện.
- **Why underserved:** Các nền tảng tuyển dụng chỉ hiển thị phần trăm độ khớp (matching) chung chung, không chỉ ra được cụ thể khoảng trống kỹ thuật nằm ở đâu.

### Need #2
- **Statement (JTBD):** When [tôi muốn lập kế hoạch chuyển dịch sự nghiệp từ Data Scientist (DS) lên các vị trí quản lý như PM/PO hoặc BrSE], I want [một lộ trình chuẩn hóa dựa trên năng lực yêu cầu thực tế của thị trường], so I can [tiết kiệm thời gian, tránh học lan man các kiến thức không cần thiết].
- **Current workaround:** Đăng ký các khóa đào tạo lý thuyết chung chung hoặc học lỏm kinh nghiệm qua các bài blog rời rạc.
- **Pain signal:** Tốn hàng triệu đồng mua nhầm khóa học không mang lại giá trị thực tế cho CV.
- **Evidence / proxy evidence:** Nhu cầu học thêm các chứng chỉ quản lý sản phẩm hoặc kỹ năng cầu nối (BrSE) ngày càng tăng cao trong giới kỹ thuật.
- **Why underserved:** Chưa có công cụ nào đủ khả năng phân tích chéo background hiện tại của ứng viên để cá nhân hóa lộ trình mới.

## 4. Strategy Statement
- **For** [sinh viên năm cuối/mới ra trường khối ngành công nghệ và khoa học dữ liệu]
- **who struggle with** [việc rải CV mù quáng mà không biết mình thiếu hụt kỹ năng gì so với JD],
- **our product helps them** [định vị chính xác năng lực bản thân và cá nhân hóa lộ trình lấp đầy skill-gap]
- **through** [một AI Agent sử dụng NLP và Vector Similarity so khớp từ khóa CV với hàng ngàn JD],
- **unlike** [các công cụ thiết kế CV bằng template hay đánh giá % matching chung chung],
- **because we can leverage** [công nghệ RAG liên tục cập nhật bộ từ khóa công nghệ mới nhất từ thị trường và tự động hóa việc đưa ra lời khuyên].

## 5. Moat Hypothesis
- **Moat mechanism:** Data compounding & Workflow learning
- **Flywheel mechanism:** Nếu chúng tôi triển khai 1000 lần trong thị trường hướng nghiệp, các yếu tố sau sẽ được cải thiện hệ thống:
    1. Kho dữ liệu về "kỹ năng thị trường đang khát" ngày càng chuẩn xác theo thời gian thực.
    2. AI tự động tối ưu hóa việc nhận diện mẫu CV và bộ kỹ năng dễ qua vòng lọc nhất.
    3. Sự tin tưởng của ứng viên tăng lên, tạo ra hiệu ứng mạng lưới dữ liệu hồ sơ.
- **Why competitors cannot replicate:** Lợi thế bền vững đến từ việc học sâu luồng dữ liệu lặp lại. Đối thủ dùng AI chung chung không có CSDL Vector chuyên sâu cho IT/Data sẽ chỉ đưa ra lời khuyên hời hợt.

## 6. Initial TAM/SAM/SOM view
| Layer | Estimate | Key assumptions | Confidence |
| :--- | :--- | :--- | :--- |
| **TAM** | $6M - $9M/year | 300k sinh viên/năm; 10% sẵn sàng trả $20-30/năm. | Medium |
| **SAM** | $1M - $1.5M/year | 40k-50k sinh viên khối ngành Kỹ thuật, IT, Data. | High |
| **SOM** | $100K/year | 3k-4k user trả phí trong 12-18 tháng đầu tại các trường top. | Medium |

- **Top 3 unknowns:**
    1. Mức độ sẵn sàng trả tiền (Willingness to pay) của sinh viên.
    2. Cách duy trì nguồn dữ liệu JD khổng lồ mà không vi phạm chính sách các sàn.
    3. Sự công nhận của nhà tuyển dụng đối với lộ trình do AI gợi ý.

- **Judgment:** Worth pursuing but not now (cần validate kỹ khả năng chi trả của tệp sinh viên).

## 7. Positioning Note (2 sentences)
- **What we are:** Chúng tôi là một công cụ AI phân tích "độ vênh" kỹ năng chuyên sâu, giúp ứng viên biết chính xác mình cần học thêm công nghệ gì để trúng tuyển.
- **What we are not / not yet:** Chúng tôi không phải là một cổng thông tin đăng tin tuyển dụng hay một công cụ thiết kế đồ họa template CV.

## 8. Self-assessment before Day 17
- **Mắt xích yếu nhất:** Market Size và Customer (khả năng chi trả của sinh viên thấp).
- **Open questions:**
    1. Tính năng MVP nào tạo ra "Aha moment" nhanh nhất?
    2. Có nên Pivot sang mô hình thu phí từ nhà tuyển dụng (B2B)?
    3. Cách xử lý đa định dạng file (PDF/Word) hiệu quả cho RAG?