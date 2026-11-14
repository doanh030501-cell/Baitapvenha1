
# NHIỆM VỤ 3 - XÂY DỰNG MỘT CẢI TIẾN GIAO DIỆN BẰNG HTML/CSS

## 5.1. Bước 1 - Xác định vấn đề

### 1. Website tham khảo

- Tên website: Vihand Group
- Website: https://vihand.com.vn/
- Trang tham khảo: https://vihand.com.vn/sharpie-products/page/2/
- Khu vực lựa chọn cải tiến: Thẻ sản phẩm trong danh sách sản phẩm Sharpie.

### 2. Mô tả giao diện hiện tại

Qua quá trình khảo sát, danh sách sản phẩm Sharpie trên website Vihand được trình bày dưới dạng lưới.

Mỗi sản phẩm có hình ảnh, tên và thông tin giá hiển thị dưới dạng "Liên hệ".

Website cũng cung cấp các tùy chọn thay đổi số lượng sản phẩm hiển thị, cách trình bày và sắp xếp danh sách.

Tuy nhiên, trong giao diện đã khảo sát, các thẻ sản phẩm chưa có nút thao tác nổi bật để khách hàng nhanh chóng xem thông tin chi tiết hoặc liên hệ báo giá.

### 3. Vấn đề cần cải thiện

- Thông tin giá chủ yếu hiển thị dưới dạng "Liên hệ", chưa có mức giá cụ thể để khách hàng so sánh trực tiếp.
- Nút thao tác trên thẻ sản phẩm chưa nổi bật.
- Khách hàng có thể phải thực hiện thêm thao tác để tìm cách liên hệ khi quan tâm đến sản phẩm.
- Thông tin phân loại sản phẩm chưa được nhấn mạnh trên từng thẻ, có thể gây khó khăn khi lựa chọn giữa các dòng bút.

### 4. Mục tiêu cải tiến

Thiết kế lại thẻ sản phẩm Sharpie nhằm:

- Giúp khách hàng dễ nhận diện sản phẩm.
- Làm rõ tên, hình ảnh và nhóm sản phẩm.
- Hiển thị trạng thái giá "Liên hệ" dễ nhận biết.
- Làm nổi bật nút xem chi tiết và liên hệ báo giá.
- Cải thiện khả năng sử dụng trên máy tính và điện thoại.

### 5. Phương án cải tiến

Tôi lựa chọn thiết kế lại thẻ sản phẩm Sharpie, tập trung vào việc trình bày thông tin rõ ràng và hỗ trợ thao tác của khách hàng.

Mỗi thẻ sản phẩm sẽ gồm:

1. Hình ảnh sản phẩm.
2. Nhóm hoặc loại bút.
3. Tên sản phẩm.
4. Mô tả ngắn.
5. Thông tin giá: "Liên hệ".
6. Nút "Xem chi tiết".
7. Nút "Liên hệ báo giá".

Phương án chỉ cải tiến giao diện, không xây dựng hệ thống mua hàng hoặc thanh toán trực tuyến.

---

## 5.2. Bước 2 - Nhờ AI đề xuất giao diện

### 1. Công cụ AI sử dụng

ChatGPT - OpenAI.

### 2. Khu vực yêu cầu AI hỗ trợ

Cải tiến giao diện thẻ sản phẩm Sharpie trên website Vihand bằng HTML5 và CSS3.

Đối tượng sử dụng: Khách hàng mua sắm trực tuyến tại Việt Nam.

### 3. Kết quả AI đề xuất

#### 3.1. Bố cục giao diện

AI đề xuất xây dựng một trang giao diện gồm:

- Phần tiêu đề: "Danh sách sản phẩm Sharpie".
- Phần giới thiệu ngắn về sản phẩm.
- Khu vực danh sách gồm tối thiểu 4 sản phẩm.
- Các sản phẩm được trình bày dưới dạng lưới.

Mỗi thẻ sản phẩm được chia thành hai phần:

Phần hình ảnh:
- Hiển thị hình ảnh sản phẩm.
- Sử dụng kích thước đồng nhất.
- Giữ nguyên tỷ lệ ảnh để tránh biến dạng.

Phần thông tin:
- Hiển thị loại bút.
- Tên sản phẩm.
- Mô tả ngắn.
- Trạng thái giá "Liên hệ".
- Nút "Xem chi tiết".
- Nút "Liên hệ báo giá".

Các thành phần được sắp xếp theo thứ tự từ thông tin nhận diện đến thao tác, giúp khách hàng dễ quan sát.

#### 3.2. Các thành phần HTML cần sử dụng

| Thẻ HTML | Vai trò |
|---|---|
| header | Chứa tiêu đề hoặc phần đầu trang. |
| main | Chứa nội dung chính của website. |
| section | Phân chia khu vực danh sách sản phẩm. |
| article | Đại diện cho từng thẻ sản phẩm. |
| img | Hiển thị hình ảnh sản phẩm. |
| h1 | Hiển thị tiêu đề chính của trang. |
| h2 | Hiển thị tiêu đề khu vực sản phẩm. |
| h3 | Hiển thị tên từng sản phẩm. |
| p | Hiển thị mô tả và thông tin giá. |
| a | Tạo liên kết xem chi tiết hoặc liên hệ. |

Các thành phần HTML5 được lựa chọn nhằm giúp mã nguồn có cấu trúc rõ ràng, dễ đọc và dễ chỉnh sửa.

#### 3.3. Cách tổ chức CSS

CSS được đặt trong file riêng:

css/style.css

Các nhóm CSS dự kiến bao gồm:

1. Thiết lập chung:
- Font chữ.
- Màu sắc.
- Khoảng cách.
- Kích thước phần tử.

2. Bố cục trang:
- Chiều rộng nội dung.
- Căn chỉnh tiêu đề.
- Khoảng cách giữa các khu vực.

3. Danh sách sản phẩm:
- Sử dụng CSS Grid.
- Quy định số cột và khoảng cách giữa các thẻ.

4. Thẻ sản phẩm:
- Hình ảnh.
- Tên sản phẩm.
- Mô tả.
- Thông tin giá.
- Nút thao tác.

5. Responsive:
- Sử dụng Media Query.
- Điều chỉnh bố cục theo kích thước màn hình.

CSS được tổ chức theo từng nhóm để thuận tiện trong quá trình kiểm tra và chỉnh sửa.

#### 3.4. Cách hiển thị trên máy tính và điện thoại

Trên máy tính:
- Hiển thị 4 sản phẩm trên một hàng.
- Các thẻ có chiều rộng và khoảng cách đồng đều.
- Thông tin và nút thao tác được căn chỉnh rõ ràng.

Trên máy tính bảng:
- Hiển thị 2 sản phẩm trên một hàng.
- Điều chỉnh khoảng cách phù hợp.

Trên điện thoại:
- Hiển thị 1 sản phẩm trên một hàng.
- Hình ảnh và văn bản được điều chỉnh kích thước.
- Nút thao tác đủ lớn để dễ nhấn.
- Không để nội dung tràn ra ngoài màn hình.

#### 3.5. Những điểm cần kiểm tra về khả năng sử dụng

Sau khi xây dựng giao diện, cần kiểm tra:

1. Hình ảnh:
- Hiển thị đầy đủ.
- Không bị méo hoặc mất ảnh.

2. Nội dung:
- Tên sản phẩm dễ đọc.
- Mô tả rõ ràng.
- Thông tin giá dễ nhận biết.

3. Nút thao tác:
- Có nhãn rõ ràng.
- Dễ nhìn và dễ nhấn.
- Liên kết hoạt động đúng nếu được thiết lập.

4. Bố cục:
- Các thẻ sản phẩm đồng đều.
- Khoảng cách hợp lý.
- Không có nội dung chồng lên nhau.

5. Responsive:
- Hiển thị tốt trên máy tính.
- Hiển thị tốt trên điện thoại.
- Không xuất hiện thanh cuộn ngang không cần thiết.

---

### 4. Phương án thiết kế được lựa chọn

Sau khi xem xét đề xuất từ AI, tôi lựa chọn phương án thiết kế lại thẻ sản phẩm Sharpie theo bố cục dạng lưới.

Trang giao diện cải tiến sẽ có tối thiểu 4 sản phẩm mẫu, mỗi sản phẩm gồm:

- Hình ảnh.
- Tên sản phẩm.
- Thông tin giá.
- Nút thao tác.

Ngoài các thành phần bắt buộc, tôi bổ sung phân loại sản phẩm và mô tả ngắn để hỗ trợ khách hàng lựa chọn.

Tôi lựa chọn giữ trạng thái giá "Liên hệ" vì website tham khảo chưa công khai giá bán cụ thể cho các sản phẩm được khảo sát.

Giao diện sử dụng phong cách đơn giản, dễ đọc và có khả năng thích ứng với nhiều kích thước màn hình.

### 5. Lý do lựa chọn phương án

- Phù hợp với vấn đề được phát hiện khi khảo sát.
- Tập trung cải tiến một khu vực cụ thể, không thiết kế lại toàn bộ website.
- Đáp ứng yêu cầu tối thiểu 4 sản phẩm mẫu.
- Có thể thực hiện bằng HTML5 và CSS3.
- Không yêu cầu backend, cơ sở dữ liệu hoặc thanh toán.
- Dễ kiểm tra và giải thích mã nguồn.

### 6. Phạm vi thực hiện

Bài tập chỉ tập trung xây dựng giao diện mô phỏng.

Không triển khai:
- Hệ thống đăng nhập.
- Cơ sở dữ liệu.
- Giỏ hàng hoạt động thực tế.
- Thanh toán trực tuyến.
- Hệ thống xử lý yêu cầu báo giá.

Nút thao tác có thể sử dụng liên kết đến website tham khảo hoặc kênh liên hệ phù hợp.

Việc sử dụng hình ảnh cần đảm bảo quyền sử dụng, không sao chép trái phép hình ảnh hoặc mã nguồn của website gốc.

### 7. Kết luận

Phương án cải tiến thẻ sản phẩm Sharpie được lựa chọn vì phù hợp với phạm vi bài tập và hướng đến việc cải thiện khả năng nhận diện thông tin và thao tác của khách hàng.

Đây là cơ sở để tiếp tục thực hiện mục 5.3 - Tạo mã nguồn bằng HTML5 và CSS3.

Lưu ý: Các vấn đề được nêu dựa trên phạm vi khảo sát đã thực hiện. Những chức năng chưa được kiểm chứng không được xem là hoàn toàn không tồn tại.
