GPP Sơ đồ - bản PWA

Các file:
- index.html: ứng dụng chính
- manifest.webmanifest: cấu hình cài ứng dụng
- service-worker.js: offline + phát hiện cập nhật
- icons/: icon cho tab, desktop, taskbar, mobile

Lưu ý quan trọng:
PWA chỉ hiện nút Cài đặt khi chạy qua HTTPS hoặc localhost. Nếu mở index.html trực tiếp bằng file:// thì Service Worker/PWA không hoạt động.

Khi phát hành bản mới:
1. Sửa nội dung index.html (hoặc file khác).
2. Tăng APP_VERSION trong service-worker.js, ví dụ 1.1.0 -> 1.1.1.
3. Upload lại toàn bộ thư mục lên hosting HTTPS.
4. Người dùng đang mở app sẽ thấy nút “Cập nhật” khi trình duyệt tải được Service Worker mới.


BẢN 1.1.1:
- Nút Cài đặt luôn hiển thị khi mở trong trình duyệt.
- Nếu mở trực tiếp file://, bấm Cài đặt sẽ giải thích cần HTTPS/localhost.
- Khi đủ điều kiện PWA, nút sẽ gọi hộp cài đặt của Chrome/Edge.
