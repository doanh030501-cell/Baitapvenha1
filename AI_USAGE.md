# AI Usage Log

## 1. Công cụ AI sử dụng
- **Claude (Anthropic):** Hỗ trợ hướng dẫn quy trình làm bài, soạn bản nháp phân tích website, viết mã giao diện mẫu và giải thích cú pháp code.
- **Google Gemini:** Tạo bộ 4 hình ảnh minh họa sản phẩm mẫu phục vụ thiết kế giao diện.
- **GitHub Copilot (trong VS Code):** Hỗ trợ tạo lệnh PowerShell để khởi tạo nhanh cấu trúc thư mục và các tệp tin ban đầu (`css`, `images`, `khao-sat`, `index.html`, `README.md`, `AI_USAGE.md`).

## 2. Mục đích sử dụng
- Xây dựng lộ trình thực hiện bài tập Chương 1 và quy trình đưa dự án lên GitHub.
- Lập bản nháp bảng khảo sát nghiệp vụ từ dữ liệu thực tế của website tham khảo.
- Đề xuất bố cục thẻ sản phẩm và khởi tạo mã nguồn HTML/CSS ban đầu.
- Giải thích cơ chế hoạt động của các thuộc tính HTML/CSS được sử dụng.
- Tạo bộ ảnh sản phẩm đồng bộ để làm dữ liệu mẫu cho trang web.

## 3. Prompt đã sử dụng
- **Prompt 1 – Phân tích website (gửi Claude):** *"Bạn là chuyên gia phân tích nghiệp vụ và thiết kế trải nghiệm người dùng cho website thương mại điện tử. Tôi đang khảo sát website: Vihand Group, https://vihand.com.vn. Hãy giúp tôi lập bảng phân tích các khu vực: trang chủ, danh mục sản phẩm, chi tiết sản phẩm, tìm kiếm, giỏ hàng. Với mỗi khu vực, hãy nêu: mục đích của chức năng, thành phần giao diện cần có, điểm thuận tiện đối với khách hàng, một vấn đề có thể phát sinh, một đề xuất cải tiến. Không khẳng định những tính năng chưa được kiểm chứng. Phân biệt rõ nhận xét dựa trên quan sát và đề xuất của AI."*
- **Các yêu cầu khác gửi Claude:** Hướng dẫn từng bước hoàn thiện bài tập Chương 1; viết mã `index.html` và `style.css` cho 4 sản phẩm mẫu với nút bấm màu hồng; hướng dẫn kiểm thử giao diện trên điện thoại và đẩy dự án lên GitHub.
- **Prompt gửi Gemini (tóm tắt):** Tạo 4 ảnh minh họa sản phẩm gồm bút marker màu, lọ màu nhuộm vải, sơn custom giày và bút chì màu để làm ảnh mẫu cho bài tập thiết kế web.

## 4. Kết quả AI đề xuất
- **Phân tích nghiệp vụ:** Bảng đánh giá 5 khu vực chức năng của `vihand.com.vn`, phân tách giữa quan sát giao diện và đề xuất cải tiến.
- **Giao diện & Bố cục:** Thiết kế lưới 4 cột; mỗi thẻ sản phẩm bao gồm ảnh, thương hiệu, tên, mô tả, giá bán và 2 nút thao tác.
- **Kỹ thuật:** Tách riêng tệp cấu trúc (`index.html`) và tệp định dạng (`css/style.css`); hỗ trợ hiển thị responsive (4 cột trên máy tính, 2 cột trên máy tính bảng, 1 cột trên điện thoại).
- **Tài nguyên:** Bộ 4 ảnh minh họa sản phẩm do Gemini tạo.

## 5. Kiểm tra và điều chỉnh thực tế
- **Kiểm thử vận hành:** Đã chạy thử trang web bằng Live Server trên trình duyệt và kiểm tra độ hiển thị responsive ở đủ 3 mức khung hình (4 cột, 2 cột, 1 cột).
- **Đối chiếu khảo sát:** Đã kiểm tra lại toàn bộ nhận xét của AI trên website thực tế `vihand.com.vn`, loại bỏ các nội dung suy đoán không chính xác *(chi tiết lưu tại `khao-sat/phan-tich-ai.md`)*.
- **Các chỉnh sửa trực tiếp của sinh viên:**
  - Thiết lập tông màu hồng chủ đạo cho hệ thống nút và nền khung ảnh.
  - Rút gọn nhãn nút từ *"Liên hệ báo giá"* thành *"Báo giá"* để khắc phục lỗi rớt dòng gây lệch bố cục.
  - Sửa lỗi tên tệp ảnh (`product-1.jpg.png` thành `product-1.png`) để khớp với đường dẫn trong HTML.
  - Hoán đổi hình ảnh giữa thẻ sản phẩm số 3 và số 4 để hiển thị đúng với tên sản phẩm.
- **Tính minh bạch dữ liệu:** Không sử dụng hình ảnh, giá bán hay mô tả thật từ website `vihand.com.vn`; toàn bộ nội dung trên trang đều là dữ liệu mẫu.

## 6. Kiến thức sinh viên hiểu và có thể giải thích
- `display: grid` và `grid-template-columns: repeat(4, 1fr)`: Chia bố cục thành 4 cột có độ rộng bằng nhau.
- `@media (max-width: ...)`: Điều chỉnh số lượng cột hiển thị linh hoạt theo kích thước màn hình (Responsive Web Design).
- Biến CSS (`:root`, `--pink`): Lưu trữ mã màu chủ đạo tại một nơi để dễ dàng quản lý và đồng bộ toàn trang.
- `object-fit: cover`: Giúp hình ảnh lấp đầy khung chứa mà không bị biến dạng tỷ lệ.
- Cấu trúc thẻ HTML ngữ nghĩa: Hiểu rõ chức năng của `<header>`, `<main>`, `<section>`, `<article>`, `<img>` và `<a>`.
