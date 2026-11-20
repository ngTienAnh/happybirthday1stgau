# Thiệp mời sinh nhật 1 tuổi — Gấu (Nguyễn Tùng Lâm)

Thiệp online gồm: phong bì mở ra, confetti, nhạc hộp nhạc Happy Birthday, đếm ngược đến tiệc, nút thêm vào lịch / chỉ đường, album ảnh. Toàn bộ là file tĩnh nên host ở đâu cũng được.

```
index.html            ← trang thiệp
images/               ← ảnh của Gấu + ảnh xem trước (og.jpg) + thiệp gốc
fonts/                ← font Baloo 2, Nunito, Dancing Script (giấy phép SIL OFL)
gau-sinh-nhat.ics     ← file lịch cho iPhone
```

## Host trên GitHub Pages (miễn phí, link không hết hạn)

1. Vào github.com → **New repository** → đặt tên `gau-1-tuoi` → chọn **Public** → Create.
2. Trong repo: **Add file → Upload files** → kéo thả *toàn bộ nội dung* của thư mục này (index.html, images, fonts, gau-sinh-nhat.ics, README.md) → **Commit changes**.
3. **Settings → Pages** → mục *Build and deployment*: Source = **Deploy from a branch**, Branch = **main**, thư mục **/(root)** → **Save**.
4. Đợi 1–2 phút, link sẽ là: `https://<username>.github.io/gau-1-tuoi/`

Hoặc bằng git:

```bash
cd gau-1-tuoi
git init && git add . && git commit -m "Thiep sinh nhat Gau 1 tuoi"
git branch -M main
git remote add origin https://github.com/<username>/gau-1-tuoi.git
git push -u origin main
```

### Để Zalo / Messenger hiện ảnh xem trước khi gửi link
Mở `index.html`, tìm dòng `og:image` và thay `TEN-GITHUB` bằng username GitHub của bạn, ví dụ:
`https://nguyentienanh.github.io/gau-1-tuoi/images/og.jpg`

## Link mời riêng cho từng khách
Thêm `?to=Tên khách` vào cuối link, ví dụ:
`https://<username>.github.io/gau-1-tuoi/?to=Ông bà nội`
→ phong bì ghi “Gấu có thư mời gửi **Ông bà nội**”, và tên hiện trên dòng “Trân trọng kính mời”.

Cách nhanh: mở `https://<username>.github.io/gau-1-tuoi/#tao-link`, gõ tên → bấm **Sao chép link**.

## Sửa nội dung
Ở cuối `index.html` có khối `CONFIG` (giờ tiệc, địa chỉ, câu mặc định khi không có tên khách, câu bong bóng khi chạm vào ảnh Gấu). Giờ kết thúc 13h00 chỉ dùng cho nút “Thêm vào lịch”.

## Lưu ý
- Repo Public → ai có link (hoặc tìm thấy repo) đều xem được ảnh của bé và địa chỉ tiệc.
- Nhạc chỉ phát sau khi khách chạm mở phong bì (trình duyệt chặn tự phát nhạc). Có nút ♪ ở góc để bật/tắt.
