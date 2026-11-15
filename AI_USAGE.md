# AI Usage Log

## 1. Công cụ AI
- Claude (Anthropic): hướng dẫn các bước làm bài, soạn bản nháp, giải thích mã.
- Google Gemini: tạo 4 ảnh minh họa sản phẩm mẫu.
- GitHub Copilot trong VS Code: tạo cấu trúc thư mục và các file ban đầu của dự án (css, images, khao-sat, index.html, README.md, AI_USAGE.md) bằng đoạn lệnh PowerShell.

## 2. Mục đích sử dụng
- Hướng dẫn quy trình làm bài và đưa bài lên GitHub.
- Soạn bản nháp bảng khảo sát từ ảnh chụp màn hình do tôi tự chụp.
- Đề xuất bố cục thẻ sản phẩm và tạo mã HTML/CSS ban đầu.
- Giải thích các thành phần HTML/CSS.
- Tạo ảnh minh họa sản phẩm (Gemini).

## 3. Prompt đã sử dụng
- Prompt gửi Gemini (tóm tắt nội dung yêu cầu): tạo 4 ảnh minh họa sản phẩm gồm bút marker màu, lọ màu nhuộm vải, sơn custom giày và bút chì màu, dùng làm ảnh mẫu cho trang web bài tập.
- Prompt gửi Claude (Prompt 1 trong đề bài): "Bạn là chuyên gia phân tích nghiệp vụ và thiết kế trải nghiệm người dùng cho website thương mại điện tử. Tôi đang khảo sát website: Vihand Group, https://vihand.com.vn. Hãy giúp tôi lập bảng phân tích các khu vực: trang chủ, danh mục sản phẩm, chi tiết sản phẩm, tìm kiếm, giỏ hàng. Với mỗi khu vực, hãy nêu: mục đích của chức năng, thành phần giao diện cần có, điểm thuận tiện đối với khách hàng, một vấn đề có thể phát sinh, một đề xuất cải tiến. Không khẳng định những tính năng chưa được kiểm chứng. Phân biệt rõ nhận xét dựa trên quan sát và đề xuất của AI."
- Các yêu cầu khác gửi Claude: hướng dẫn từng bước làm bài tập Chương 1; soạn lại index.html và style.css (4 sản phẩm mẫu, nút màu hồng); hướng dẫn kiểm tra giao diện điện thoại và đưa bài lên GitHub.

## 4. Kết quả AI đề xuất
- Bố cục lưới 4 cột, thẻ sản phẩm gồm ảnh, thương hiệu, tên, mô tả, giá và hai nút.
- Responsive: 4 cột, 2 cột, 1 cột theo độ rộng màn hình.
- Mã HTML tách riêng index.html và CSS tách riêng css/style.css.
- 4 ảnh minh họa do Gemini tạo.

## 5. Kiểm tra và điều chỉnh
- Đã chạy trang bằng Live Server và mở trên trình duyệt.
- Đã kiểm tra giao diện ở nhiều độ rộng màn hình: 4 cột, 2 cột, 1 cột.
- Đã đối chiếu kết quả phân tích của AI với website Vihand thật, loại bỏ các nhận xét không đúng (xem khao-sat/phan-tich-ai.md).
- Điểm tôi tự điều chỉnh: chọn tông màu hồng cho nút và nền ảnh; đổi chữ nút "Liên hệ báo giá" thành "Báo giá" vì nút bị rớt dòng; đổi tên file ảnh cho khớp đường dẫn trong code (product-1.jpg.png thành product-1.png); hoán đổi ảnh ở thẻ 3 và thẻ 4 cho khớp tên sản phẩm.
- Không sử dụng: ảnh, giá thật hay mô tả thật từ website tham khảo. Toàn bộ dữ liệu sản phẩm là dữ liệu mẫu.

## 6. Phần tôi hiểu và có thể giải thích
- display: grid và grid-template-columns: repeat(4, 1fr) dùng để chia cột đều nhau.
- @media (max-width: ...) đổi số cột theo kích thước màn hình (responsive).
- Biến CSS (:root, --pink) giúp đổi màu chủ đạo ở một chỗ.
- object-fit: cover giúp ảnh lấp đầy ô mà không bị méo.
- Cấu trúc HTML: header, main, section, article, img, a.