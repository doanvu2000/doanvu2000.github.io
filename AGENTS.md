# doanvu2000.github.io

Portfolio cá nhân của Doan Vũ (Android, iOS native, Flutter, game Unity sang Flutter, web, desktop) trên GitHub Pages, kèm landing page các app JLSoft Together. Site tĩnh, đang chạy live tại https://doanvu2000.github.io.

| | |
|---|---|
| Loại | Web tĩnh (HTML / CSS / vanilla JS, không build) |
| Chạy | `python -m http.server 8080` hoặc `npx serve .` rồi mở http://localhost:8080 |
| Test | chưa rõ (không có lint / test) |
| Deploy | GitHub Pages từ nhánh `master` — chủ nhân tự push |

## Thư mục chính

- `index.html`: portfolio 1 file, style Apple, CSS inline (Hero, Giới thiệu, Kinh nghiệm, Dự án, Liên hệ)
- `love.html`: animation trái tim bằng canvas
- `fire/`: pháo hoa `hpny2025.html` (canvas + jQuery)
- `jlsoft/<app>/`: `logo.png` + `marketing.html` (+ `overview.html`) cho từng app — `lovequote`, `jadio`, `ledbanner`
- `img/`: avatar, icon mạng xã hội
- `style.css`: style cũ, `index.html` không còn dùng

## Quy ước riêng project

- Thêm sản phẩm JLSoft vào phần Dự án của `index.html` → BẮT BUỘC cập nhật cả https://jlsoft.jinvu.vn/ (app card, hero stats) và thêm `jlsoft/<appname>/` có `logo.png` + `marketing.html`.
- `index.html` theo style `F:\work\web\page\index.html`: token màu trên `:root` + `[data-theme="dark"]`, theme lưu `localStorage` key `theme`, mặc định sáng.
- Nội dung ngắn gọn, ít liệt kê, hạn chế phải scroll.
- `app-ads.txt` ở root dành cho AdMob — không xoá.

## Tài liệu

- Plan và tiến độ: `.planning/`
- Bug đã gặp: `bug_pool/signatures.tsv`
