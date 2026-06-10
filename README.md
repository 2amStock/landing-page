# Hướng dẫn triển khai Landing Page FamiHub

Đây là trang web tĩnh (Static Website) siêu nhẹ dùng để người dùng tải file `.apk` của ứng dụng FamiHub.

## 1. Cập nhật file APK
- Bạn chỉ cần copy file cài đặt Android của bạn (ví dụ: `app-release.apk` sinh ra từ Flutter) vào thư mục này.
- **Quan trọng:** Đổi tên file đó thành `famihub.apk` (trùng với tên link tải trong file `index.html`). 
- Hoặc nếu bạn muốn giữ nguyên tên file APK của bạn, hãy mở `index.html` và sửa dòng `<a href="famihub.apk" ...>` thành tên file của bạn.

## 2. Cách đưa trang web này lên mạng miễn phí (Host)

Vì đây là trang web tĩnh, bạn có thể sử dụng các dịch vụ Host miễn phí tốt nhất hiện nay như **Vercel**, **Netlify**, hoặc **Surge**. Cách nhanh nhất là dùng Surge hoặc Vercel:

### Cách 1: Dùng Vercel (Khuyên dùng)
1. Cài đặt Node.js nếu máy bạn chưa có.
2. Mở Terminal (Command Prompt) tại thư mục `famihub_landing_page` này.
3. Chạy lệnh: `npm i -g vercel` (để cài đặt Vercel CLI).
4. Chạy lệnh: `vercel`
5. Đăng nhập và cứ nhấn `Enter` để đồng ý với các thiết lập mặc định. Vercel sẽ tự động upload thư mục này lên và cấp cho bạn một đường link HTTPS (VD: `https://famihub-landing.vercel.app`).

### Cách 2: Dùng Surge (Siêu nhanh)
1. Mở Terminal tại thư mục này.
2. Chạy lệnh: `npm i -g surge`
3. Chạy lệnh: `surge`
4. Tạo tài khoản nhanh ngay trên Terminal và nhập tên miền tùy ý (VD: `famihub-app.surge.sh`).

## 3. Tạo mã QR Code
1. Sau khi đã có link web (VD: `https://famihub-landing.vercel.app`), hãy truy cập các trang tạo mã QR miễn phí như: [QR Code Generator](https://www.qr-code-generator.com/) hoặc [QRCode Monkey](https://www.qrcode-monkey.com/).
2. Dán link web của bạn vào.
3. Tải hình ảnh mã QR về. 
4. Người dùng chỉ cần quét mã QR này, họ sẽ được đưa đến trang Landing Page tuyệt đẹp vừa tạo và bấm nút để tải file APK về máy.
