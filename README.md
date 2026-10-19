# Sổ thực tập FRT – Gia Khôi

Webapp một trang để Khôi học và ghi chép trong đợt thực tập bán hàng 12 tuần tại FRT, và để mentor theo dõi tiến độ. Chạy trên GitHub Pages, lưu dữ liệu vào một file `.md` trong chính kho này. Không cần máy chủ.

**Hướng dẫn cài đặt: [HUONG-DAN-TRIEN-KHAI.md](HUONG-DAN-TRIEN-KHAI.md)** (4 bước, khoảng 15 phút).

## Đăng nhập

Một đường link chung, màn hình đầu hỏi mật khẩu:

| Mật khẩu | Màn hình |
| --- | --- |
| `khoi12345` | Sổ thực tập của Khôi |
| `m12345` | Mentor: theo dõi tiến độ, kết nối GitHub |

## Chức năng

**Khôi:** Hôm nay (tuần hiện tại, việc đến hạn, tiến độ) · Ghi chép hằng ngày · Nhật ký tuần · Case 1 FPT Shop, Case 2 Long Châu, Case 3 Thế Giới Di Động (câu hỏi B1–B4, đọc thêm, Tự soi, Bảng giả định, Sổ thuật ngữ, Nhật ký cập nhật) · Tra cứu · Buổi tổng kết đúc kết · Cài đặt.

**Mentor:** tổng quan tiến độ, bảng hoạt động 28 ngày, dòng thời gian mọi lần lưu với tóm tắt (ví dụ "2 câu trả lời B1 (Case 1)", "1 thuật ngữ mới") và chi tiết nội dung.

## Lưu trữ

- Tự lưu trên máy sau mỗi lần gõ; tự đẩy lên GitHub sau 15 giây, khi rời tab hoặc đóng app, và khi mở lại app nếu còn thay đổi chưa lên.
- Hồ sơ: file `ho-so-thuc-tap-frt.md` ở nhánh `data` của kho. Mỗi lần lưu là một commit, giữ toàn bộ lịch sử.
- `config.json` (do webapp tạo ở bước kết nối) chứa token GitHub đã mã hóa bằng mật khẩu.

## Các file

| File | Vai trò |
| --- | --- |
| `index.html` | Toàn bộ webapp |
| `manifest.webmanifest`, `icon-*.png`, `apple-touch-icon.png`, `favicon-32.png` | Biểu tượng, cài lên màn hình điện thoại |
| `.nojekyll` | Báo GitHub Pages phục vụ file nguyên trạng |
| `HUONG-DAN-TRIEN-KHAI.md` | Hướng dẫn cài đặt và xử lý sự cố |
