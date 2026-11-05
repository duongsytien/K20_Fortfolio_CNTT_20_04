## V8 – Portfolio
# AI Log – Lab 5

## Báo lỗi và sửa lỗi

### 1) Mismatch giới hạn ký tự của textarea
- Bước tái hiện: Mở form liên hệ và kiểm tra thuộc tính `maxlength` của ô nội dung.
- Nguyên nhân: HTML đặt `maxlength="600"` nhưng mô tả hiển thị và quy tắc nghiệp vụ yêu cầu nhập từ 10 đến 500 ký tự.
- Sửa: Đổi `maxlength="600"` thành `maxlength="500"` trong `index.html`.
- Kiểm tra lại: Xác nhận ô nhập hiện đúng giới hạn 500 ký tự và nhãn mô tả đồng bộ với form.

### 2) CSS transition bị sai cú pháp
- Bước tái hiện: Xem CSS cho `.button`, hover/active không có hiệu ứng mượt như mong đợi.
- Nguyên nhân: `transition` thiếu dấu phẩy giữa các thuộc tính, nên cú pháp CSS không hợp lệ.
- Sửa: Chuyển `transition` sang dạng đúng: `background-color 180ms ease, color 180ms ease, box-shadow 180ms ease, transform 180ms ease`.
- Kiểm tra lại: Kiểm tra trên browser thấy hiệu ứng hover/active hoạt động mượt hơn.

### 3) Từ khóa `tranform` sai chính tả
- Bước tái hiện: Card không có hiệu ứng di chuyển khi hover.
- Nguyên nhân: `transition: tranform 180ms ease;` có lỗi chính tả `tranform` thay vì `transform`.
- Sửa: Đổi `tranform` thành `transform` trong `.card`.
- Kiểm tra lại: Hover trên card now có hiệu ứng `translateY` như mục tiêu.

### 4) Thẻ link CSS bị lặp trong `index.html`
- Bước tái hiện: Mở DevTools/kiểm tra tài nguyên tải trang, thấy stylesheet được nạp lặp.
- Nguyên nhân: Có hai thẻ `<link rel="stylesheet" href="css/style.css">`, một thẻ ở đầu và một thẻ ở cuối body.
- Sửa: Xóa thẻ lặp ở cuối `body`.
- Kiểm tra lại: Tránh tải trùng CSS và giữ cấu trúc HTML sạch hơn.

## Kết luận
Các lỗi trên đã được sửa trực tiếp tại [index.html](../index.html) và [css/style.css](style.css). Mục tiêu của lab là form nhập liệu, tương tác focus, hover và transition đúng chuẩn HTML5/CSS3.
