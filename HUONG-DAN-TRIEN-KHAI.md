# Hướng dẫn đưa Sổ thực tập FRT lên GitHub

Chỉ cần **một tài khoản GitHub** (của anh/chị), **một kho công khai**, làm trên trang web github.com, không cần gõ lệnh. Khoảng 15 phút.

## Cách hệ thống hoạt động

- Mọi người mở **cùng một đường link**, ví dụ `https://ten-tai-khoan.github.io/so-thuc-tap/`.
- Màn hình đầu tiên hỏi mật khẩu:

| Mật khẩu | Vào màn hình |
| --- | --- |
| `khoi12345` | Sổ thực tập của Khôi: case, câu hỏi, thuật ngữ, ghi chép, nhật ký |
| `m12345` | Mentor: tổng quan tiến độ và dòng thời gian mọi lần Khôi cập nhật |

- Dữ liệu của Khôi tự lưu vào **một file `.md` duy nhất** trong chính kho đó (nhánh `data`). Mỗi lần lưu là một bản ghi có ngày giờ, nên mentor xem được toàn bộ lịch sử.

---

## Bước 1. Tạo kho và tải code lên

1. Đăng nhập github.com → nút **+** góc trên phải → **New repository**.
2. *Repository name*: `so-thuc-tap`. Chọn **Public**. Tích **Add a README file** → **Create repository**.
3. Giải nén `so-thuc-tap-frt.zip`. Trong kho vừa tạo, bấm **Add file → Upload files**, kéo thả **tất cả các file** trong thư mục `so-thuc-tap` vào → **Commit changes**.
   - File `.nojekyll` có thể bị ẩn trên máy (Mac: `Cmd + Shift + .` trong Finder; Windows: bật *Hidden items*). Thiếu file này webapp vẫn chạy.

## Bước 2. Bật GitHub Pages

1. Trong kho → **Settings** → mục **Pages** ở cột trái.
2. *Source*: **Deploy from a branch**. *Branch*: **main**, thư mục **/ (root)** → **Save**.
3. Đợi 1–3 phút, tải lại trang. Khi thấy *"Your site is live at …"*, mở link đó: thấy màn hình nhập mật khẩu là đã chạy.

## Bước 3. Tạo token để webapp được ghi dữ liệu

1. Ảnh đại diện → **Settings** → cuối cột trái **Developer settings** → **Personal access tokens** → **Fine-grained tokens** → **Generate new token**.
2. Điền:
   - *Token name*: `so-thuc-tap`
   - *Expiration*: **Custom**, chọn ngày sau khi kết thúc đợt thực tập (ví dụ 4–6 tháng)
   - *Repository access*: **Only select repositories** → chọn `so-thuc-tap`
   - *Permissions → Repository permissions → Contents*: **Read and write**
3. **Generate token**, rồi **sao chép token** (bắt đầu bằng `github_pat_`). GitHub chỉ hiện một lần.

## Bước 4. Kết nối trong webapp (làm một lần)

1. Mở link webapp, nhập mật khẩu **`m12345`**.
2. Chọn mục **Kết nối GitHub** ở menu trái, điền:
   - *Tên tài khoản GitHub*: tên tài khoản của anh/chị
   - *Tên kho*: `so-thuc-tap`
   - *Token*: token vừa sao chép
   - *Mật khẩu của Khôi*: `khoi12345`
3. Bấm **Kết nối**. Thấy *"Đã kết nối"* là xong. Webapp tự tạo nhánh `data` để lưu hồ sơ và file `config.json` chứa token **đã được mã hóa** bằng mật khẩu.
4. Đợi 1–2 phút để GitHub Pages cập nhật.

**Xong.** Gửi cho Khôi đường link và mật khẩu `khoi12345`.

---

## Kiểm tra nhanh

1. Khôi mở link, nhập `khoi12345`, vào **Case 1**, gõ thử một câu trả lời B1. Khoảng 15 giây sau, thanh trên cùng báo *"Đã lưu lên GitHub"*.
2. Anh/chị mở link, nhập `m12345`, bấm **Làm mới**: dòng thời gian có mục *"1 câu trả lời B1 (Case 1)"*.

## Dùng hằng ngày

**Khôi**
- Mở link, nhập mật khẩu. Tích *Ghi nhớ trên thiết bị này* để lần sau không phải nhập lại.
- Gõ là tự lưu, không cần bấm nút. Bấm **Đăng xuất** nếu dùng máy chung.
- Cài lên màn hình điện thoại: iPhone (Safari) nút Chia sẻ → *Thêm vào MH chính*; Android (Chrome) menu ⋮ → *Thêm vào màn hình chính*.

**Mentor**
- Mở link, nhập `m12345`: xem tổng quan, bảng hoạt động 28 ngày, dòng thời gian từng lần lưu kèm *Xem chi tiết*.
- Đọc toàn bộ hồ sơ hiện tại: bấm *mở file trên GitHub* ngay trong màn hình mentor.

## Xử lý sự cố

| Hiện tượng | Cách xử lý |
| --- | --- |
| Mở link báo 404 | Đợi thêm vài phút sau khi bật Pages; kiểm tra lại Bước 2 |
| Khôi thấy "Chưa kết nối GitHub" | Bước 4 chưa xong, hoặc Pages chưa cập nhật. Đợi 2 phút, Khôi bấm **Đăng xuất** rồi đăng nhập lại |
| "Token không hợp lệ" khi kết nối | Dán thiếu ký tự hoặc token hết hạn; tạo token mới (Bước 3) |
| "Không tìm thấy kho" khi kết nối | Kiểm tra tên tài khoản, tên kho, và token đã chọn đúng kho `so-thuc-tap` |
| Thanh trạng thái báo "chưa lên được GitHub" | Mất mạng. Dữ liệu vẫn an toàn trên máy, app tự đẩy lên khi Khôi mở lại có mạng |
| Khôi đổi máy | Đăng nhập trên máy mới, vào **Cài đặt** → *Tải bản mới nhất từ GitHub* |

## Khi token hết hạn

GitHub gửi email nhắc trước. Tạo token mới (Bước 3), rồi làm lại Bước 4. Sau 1–2 phút, Khôi đăng xuất và đăng nhập lại.

## Lưu ý về mức độ riêng tư

- Theo thiết kế này, **kho và hồ sơ của Khôi là công khai**: ai có đường link kho GitHub đều đọc được file hồ sơ. Không ghi thông tin nhạy cảm vào sổ.
- Mật khẩu chỉ lưu dưới dạng mã băm, token được mã hóa bằng mật khẩu. Tuy vậy, mật khẩu ngắn như hiện tại vẫn có thể bị dò ra bởi người cố tình. Khi đó, người đó có thể sửa dữ liệu trong kho này (không ảnh hưởng gì khác trong tài khoản). Mọi phiên bản cũ vẫn còn trong lịch sử GitHub nên luôn khôi phục được.
- Muốn đổi mật khẩu: cần sửa hai mã băm trong `index.html` (biến `ROLE_SHA`). Nếu cần, nhờ người hỗ trợ kỹ thuật làm và chạy lại Bước 4.

## Sửa nội dung case sau này

Trong kho, mở `index.html` → biểu tượng bút chì → sửa trong các biến `READ`, `CASES`, `SUMMARY` ở đầu đoạn `<script>` → **Commit changes**. Không đổi thứ tự các câu hỏi đã có câu trả lời.
