# Tra cứu phạt nguội

Dự án này cho phép nhanh chóng tạo server để tra cứu các vi phạm giao thông sử dụng số biển số xe. Sử dụng dữ liệu từ csgt.vn

## Tính năng

- Nhanh chóng tạo REST API để tra cứu vi phạm giao thông
- Auto retry nếu xác minh captcha thất bại
- Trích xuất và hiển thị thông tin vi phạm giao thông

## Cài đặt

### Yêu cầu

- Node.js (phiên bản 14 hoặc cao hơn)
- npm (Trình quản lý gói Node)

### Các bước

1. Clone repository:

   ```sh
   git clone https://github.com/anyideaz/phatnguoi-api.git
   cd phatnguoi-api
   ```

2. Cài đặt các dependency:

   ```sh
   npm install
   ```

## Sử dụng

### Chạy server REST API

1. Chạy server:

   ```sh
   node server.js
   ```

2. Gửi yêu cầu GET đến endpoint `/api` với tham số `licensePlate`:

   ```sh
   curl "http://localhost:3000/api?licensePlate=30H47465"
   ```

## Cấu trúc dự án

- `apiCaller.js`: Chứa logic chính để tương tác với API tra cứu vi phạm giao thông.
- `extractTrafficViolations.js`: Hàm tiện ích để trích xuất thông tin vi phạm giao thông từ phản hồi API.
- `server.js`: Thiết lập server Express.js với endpoint REST API.

## Giấy phép

Dự án này được cấp phép theo Giấy phép MIT. Xem tệp [LICENSE](LICENSE) để biết chi tiết.
