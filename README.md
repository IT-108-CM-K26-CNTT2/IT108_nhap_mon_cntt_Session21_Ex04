# Bài 4: Đánh giá công cụ hỗ trợ xử lý lỗi lập trình

## 1. Bảng so sánh

| Tiêu chí | Google Search (StackOverflow) | AI Assistant |
|---|---|---|
| **Độ chính xác** | Dựa trên thực tế, được cộng đồng kiểm chứng (upvote/tick xanh). | Trực diện theo log lỗi, nhưng dễ sai lệch với kiến trúc dự án phức tạp. |
| **Tính cập nhật** | Tức thời, phản ánh ngay các lỗi từ bản cập nhật mới nhất. | Bị giới hạn bởi thời gian cắt dữ liệu huấn luyện. |
| **Khả năng giải thích** | Phụ thuộc vào người trả lời, thường cung cấp mã lệnh để dùng ngay. | Cực kỳ chi tiết, giải thích rõ cơ chế từng lệnh và dễ dàng hỏi đáp thêm. |
| **Rủi ro (Hallucination)** | Không có. Chỉ có rủi ro áp dụng nhầm bài viết cũ. | Có nguy cơ bịa đặt tham số dòng lệnh hoặc file cấu hình không tồn tại. |

## 2. Trường hợp bắt buộc phải dùng Google Search để đảm bảo an toàn

### 2.1. Phát hiện tiến trình lạ có mã độc

Phải dùng Google để tra cứu tên tiến trình nhằm xác minh mã độc. Tuyệt đối không tin AI, vì AI có thể suy đoán hoặc nhầm lẫn sang một tiến trình hệ thống hợp lệ rồi khẳng định là an toàn, khiến mình bỏ qua và gây nguy hiểm.

### 2.2. Thực thi lệnh hệ thống quyền cao (Root/Admin)

Cần dùng Google đối chiếu tài liệu chính thức trước khi chạy các lệnh ép buộc dừng tiến trình, tránh việc AI cấp sai tham số làm sập hệ thống hoặc mất dữ liệu.

## 3. Kết luận

- **AI Assistant** phù hợp để giải thích lỗi, hiểu cơ chế và hỏi đáp nhanh.
- **Google Search (StackOverflow)** phù hợp khi cần thông tin cập nhật, đã được kiểm chứng.
- Với các tác vụ **liên quan đến bảo mật hoặc quyền cao**, luôn đối chiếu với nguồn chính thống trước khi thực thi.
