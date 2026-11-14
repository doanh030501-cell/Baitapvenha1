# AI Usage Log

## 1. Công cụ AI
- Claude (Anthropic): hướng dẫn các bước làm bài, soạn bản nháp, giải thích mã.
- Google Gemini: tạo 4 ảnh minh họa sản phẩm mẫu.
- GitHub Copilot trong VS Code: [ĐIỀN: ghi việc Copilot đã làm, ví dụ tạo cấu trúc thư mục và file ghi chú trong thư mục khao-sat. Nếu bạn không dùng thì xóa dòng này]

## 2. Mục đích sử dụng
- Hướng dẫn quy trình làm bài và đưa bài lên GitHub.
- Soạn bản nháp bảng khảo sát từ ảnh chụp màn hình do tôi tự chụp.
- Đề xuất bố cục thẻ sản phẩm và tạo mã HTML/CSS ban đầu.
- Giải thích các thành phần HTML/CSS.
- Tạo ảnh minh họa sản phẩm (Gemini).

## 3. Prompt đã sử dụng
- Prompt gửi Gemini để tạo ảnh: [ĐIỀN: dán nguyên câu bạn đã gõ cho Gemini]
- Prompt gửi Claude: [ĐIỀN: ghi 1 đến 2 câu chính bạn đã hỏi, ví dụ "hướng dẫn mình làm từng bước bài tập chương 1", "soạn lại index.html và style.css, đổi nút sang màu hồng"]

## 4. Kết quả AI đề xuất
- Bố cục lưới 4 cột, thẻ sản phẩm gồm ảnh, thương hiệu, tên, mô tả, giá và hai nút.
- Responsive: 4 cột, 2 cột, 1 cột theo độ rộng màn hình.
- Mã HTML tách riêng index.html và CSS tách riêng css/style.css.
- 4 ảnh minh họa do Gemini tạo.

## 5. Kiểm tra và điều chỉnh
- Đã chạy trang bằng Live Server và mở trên trình duyệt.
- Đã kiểm tra giao diện ở nhiều độ rộng màn hình: 4 cột, 2 cột, 1 cột.
- Điểm tôi tự điều chỉnh: chọn tông màu hồng cho nút và ô ảnh; đổi chữ nút "Liên hệ báo giá" thành "Báo giá" vì nút bị rớt dòng; [ĐIỀN: thêm điểm khác bạn đã sửa, ví dụ đổi tên file ảnh cho khớp code, đổi vị trí ảnh cho khớp tên sản phẩm].
- Không sử dụng: ảnh, giá thật hay mô tả thật từ website tham khảo. Toàn bộ dữ liệu sản phẩm là dữ liệu mẫu.

## 6. Phần tôi hiểu và có thể giải thích
- display: grid và grid-template-columns: repeat(4, 1fr) dùng để chia cột đều nhau.
- @media (max-width: ...) đổi số cột theo kích thước màn hình (responsive).
- Biến CSS (:root, --pink) giúp đổi màu chủ đạo ở một chỗ.
- object-fit: cover giúp ảnh lấp đầy ô mà không bị méo.
- Cấu trúc HTML: header, main, section, article, img, a.