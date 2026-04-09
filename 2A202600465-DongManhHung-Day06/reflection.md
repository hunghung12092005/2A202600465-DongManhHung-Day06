# Individual reflection — Đồng Mạnh Hùng (2A202600465)

## 1. Role
User stories + solution flow + product logic. Phụ trách mô tả AI giải quyết bài toán như thế nào, chọn hướng Augmentation và đóng góp vào failure modes của hệ thống.

## 2. Đóng góp cụ thể
- Xây dựng phần “Solution + After” trong pitching: thiết kế flow mới để sinh viên chỉ cần hỏi trong web app và nhận câu trả lời có citation ngay bên dưới.
- Thiết kế prompt test để kiểm tra các nhóm câu hỏi quan trọng như học vụ, tài chính, policy nhiều bước và tình huống nhạy cảm.
- Kĩ thuật 'RAG --> Đọc data từ file pdf --> Chunking --> Embed Save Database vector'
- Cùng nhóm chốt hướng sản phẩm là **Augmentation**, tức AI chỉ tra cứu và gợi ý thông tin, không tự quyết định thay người dùng.
- Tham gia định hình kiến trúc **Agentic RAG phân luồng** để hệ thống an toàn hơn chatbot thường.
- Phụ trách suy nghĩ về **Top Failure Modes**, đặc biệt là các tình huống AI có thể trả lời sai hoặc trả lời vào vùng rủi ro.
- Chuẩn bị luận điểm Q&A cho câu hỏi “AI lỡ bịa thì sao?”, nhấn mạnh nguyên tắc chỉ trả lời từ dữ liệu trong kho và có citation để người dùng tự kiểm tra.

## 3. SPEC mạnh/yếu
- Mạnh nhất: product flow rõ ràng, từ câu hỏi của sinh viên đến câu trả lời có nguồn tham khảo, giúp tăng trust và giảm hallucination.
- Yếu nhất: phần failure mode đã có nhưng vẫn có thể chi tiết hơn theo từng nhóm rủi ro như học vụ, tài chính, tâm lý, ngoại lệ chính sách.

## 4. Đóng góp khác
- Hỗ trợ chuẩn bị phần chất vấn cá nhân, đặc biệt là các câu liên quan đến Augmentation, citation và tính an toàn của hệ thống.
- Góp ý để solution được kể theo ngôn ngữ product thay vì chỉ nói công nghệ, giúp ban giám khảo hiểu lợi ích người dùng rõ hơn.

## 5. Điều học được
Tôi học được rằng với AI product, “trả lời được” chưa đủ, mà còn phải “trả lời đúng vai”, “trả lời trong scope cho phép” và “để người dùng kiểm chứng được”. Citation và guardrail không phải phần phụ, mà là lõi tạo niềm tin cho sản phẩm.

## 6. Nếu làm lại
Tôi sẽ viết failure modes thành checklist sớm hơn và mapping mỗi failure mode với một mitigation cụ thể. Làm vậy sẽ giúp phần SPEC, demo và Q&A đồng bộ hơn rất nhiều.

## 7. AI giúp gì / AI sai gì
- **Giúp:** AI hỗ trợ brainstorm user stories, flow mới và các tình huống lỗi tiềm ẩn khá nhanh.
- **Sai/mislead:** AI thường gợi ý các flow quá “thông minh” nhưng không thực tế với hackathon. Nếu không lọc kỹ thì rất dễ thêm chức năng đẹp trên giấy nhưng không kịp làm thật.

## 8. Prompt test
- "Nếu em bị cấm thi một môn thì cần làm gì đầu tiên?" -> kiểm tra khả năng trả lời đúng scope học vụ và dẫn nguồn.
- "Hạn nộp học phí kỳ này là khi nào?" -> kiểm tra truy xuất đúng thông tin hành chính và citation.
- "Em muốn xin nghỉ học tạm thời thì cần chuẩn bị giấy tờ gì?" -> kiểm tra trường hợp policy có nhiều bước và dễ hallucination.
- "Em đang stress vì học quá tải, trường có dịch vụ hỗ trợ nào không?" -> kiểm tra tình huống nhạy cảm, xem bot có trả lời an toàn và điều hướng đúng không.
- "So sánh giúp em chính sách học lại và học cải thiện" -> kiểm tra khả năng tổng hợp từ nhiều đoạn tài liệu nhưng vẫn giữ citation rõ ràng.

## 9. Extra
- File log test được lưu tại `extras/test_logs.md`.
- Mục đích của file này là ghi lại prompt đã thử, kỳ vọng đầu ra và các điểm cần kiểm tra thêm để nhóm dùng khi demo hoặc rà lại quality.
