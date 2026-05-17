# GameStore 🎮

GameStore là một website thương mại điện tử chuyên cung cấp các trò chơi máy tính bản quyền, tài khoản Premium và Gift Code chất lượng cao. Dự án nhắm tới việc cung cấp trải nghiệm mua sắm mượt mà, giao diện sống động (glassmorphism/dark mode) và hệ thống API mạnh mẽ.

## ✨ Điểm nổi bật
- **Giao diện hiện đại:** Được xây dựng hoàn toàn bằng HTML, CSS (Vanilla) và JavaScript thuần, tối ưu hoá với Dark Theme, micro-animations và các hiệu ứng nổi bật nhằm đem tới cảm giác "Gaming" chuyên nghiệp.
- **Backend ASP.NET Core:** Sử dụng C# ASP.NET Core Web API với Dapper ORM để xử lý truy vấn tốc độ cao.
- **Cơ sở dữ liệu SQL Server:** Lưu trữ toàn bộ thông tin người dùng, ví điện tử, sản phẩm, mã giảm giá và lịch sử giao dịch.
- **Tính năng nổi bật:** 
  - Đăng ký / Đăng nhập (JWT Auth).
  - Giỏ hàng & Thanh toán giả lập qua các loại ví điện tử (MoMo, ZaloPay), thẻ Ngân hàng với mã QR chi tiết.
  - Quản lý bộ sưu tập thư viện hình ảnh game tự động thích ứng với cấu trúc dự phòng cao cấp (hỗ trợ hiển thị ảnh Youtube chất lượng cao).
  - Động bộ hoá thông tin khuyến mãi, giờ vàng giá sốc (Flash Sale) và Danh mục trên trang chủ.

## 🛠 Nền tảng công nghệ
- **Frontend:** HTML5, CSS3, ES6 JavaScript. 
- **Backend:** C# (.NET 8.0)
- **Database:** Microsoft SQL Server
- **Công cụ Server (Tùy chọn Frontend):** Laragon dùng để Host HTML (Môi trường phát triển cục bộ).

## 🚀 Hướng dẫn cài đặt & Khởi chạy

### 1. Chuẩn bị cơ sở dữ liệu
- Mở SQL Server Management Studio (hoặc công cụ tương tự).
- Chạy script SQL nằm trong thư mục `database/gamestore.sql` để khởi tạo bảng và seed dữ liệu mẫu.
- Đảm bảo SQL Server của bạn có cấu hình tài khoản phù hợp (VD: `User Id=sa; Password=123`).

### 2. Khởi chạy Backend API
Dự án Backend nằm gọn trong thư mục `GameStoreApi`.
```bash
cd GameStoreApi
dotnet build
dotnet run
```
API sẽ lắng nghe tại cổng `http://localhost:3000` (hoặc cấu hình tương ứng trong thư mục `Properties/launchSettings.json`).

### 3. Cấu hình Frontend (Client)
Tất cả các file HTML gốc nằm ngoài thư mục `GameStoreApi`.
- Có thể sử dụng **Live Server** trên VS Code hoặc **Laragon** (trỏ virtual host vào thư mục gốc `gamestore`).
- Cấu hình file `js/api.js`: Đảm bảo biến trỏ đến backend API là đúng (Mặc định: `http://localhost:3000/api`).

### 4. Truy cập trang web
Sau khi server và API chạy, truy cập vào trang `index.html` (ví dụ `http://localhost/gamestore` hoặc `http://127.0.0.1:5500`) trên trình duyệt để trải nghiệm tính năng web!

---

## 🏗 Cấu trúc thư mục chính
```text
gamestore/
├── css/             # Stylesheets (Giao diện tổng quát, các trang con, auth)
├── js/              # Chứa logic frontend (api.js, main.js, cart.js...)
├── database/        # Chứa schema SQL để deploy DB
├── GameStoreApi/    # Mã nguồn Backend ASP.NET Core rẽ nhánh
├── index.html       # Trang chủ cửa hàng
├── detail.html      # Trang chi tiết thông tin sản phẩm
├── checkout.html    # Giao diện đặt hàng 
├── payment.html     # Cổng thanh toán (QR Code, Bank)
├── login.html       # Cổng đăng nhập/đăng ký
└── ...
```

## 📜 Giấy phép
Bản quyền © 2026 GameStore. Dự án phục vụ mục đích học tập và phát triển ứng dụng Web Nâng Cao.
