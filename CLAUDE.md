@AGENTS.md

# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static personal portfolio hosted on GitHub Pages (doanvu2000.github.io). No build system — pure HTML, CSS, and vanilla JavaScript served directly.

## Development

No build, lint, or test commands — open HTML files directly in a browser or use a local static server:

```bash
# Serve locally (Python)
python -m http.server 8080

# Or with Node (if installed)
npx serve .
```

## Architecture

- `index.html` — portfolio 1 file, style Apple (giống `F:\work\web\page\index.html`): Hero + stats, Giới thiệu (về tôi + kỹ năng), Kinh nghiệm, Dự án (app JLSoft + open source dạng app-row), Liên hệ; CSS inline, không Tailwind/three.js/gsap
- `style.css` — style cũ, `index.html` không còn dùng
- `love.html` — standalone particle heart animation (canvas, black background, pink gradient text)
- `fire/hpny2025.html` — fireworks animation using canvas + jQuery; self-contained in `fire/`
- `jlsoft/lovequote/` — product marketing pages (overview.html + marketing.html) for the LoveQuote app
- `jlsoft/jadio/` — product marketing pages for the Jadio Podcast app
- `https://jlsoft.jinvu.vn/` — JLSoft Together store landing page listing all apps (purple gradient, dark/light mode)

## JLSoft Product Sync Rule

Khi thêm sản phẩm JLSoft mới vào phần Projects của `index.html`, BẮT BUỘC cập nhật đồng thời `https://jlsoft.jinvu.vn/`:
- Thêm app card mới vào `.apps-grid` với: logo, tên, mô tả, feature tags, nút Play Store, nút Xem chi tiết
- Cập nhật hero stats (số ứng dụng, các số liệu nổi bật)
- Thêm thư mục `jlsoft/<appname>/` với `logo.png` và `marketing.html`

### Key patterns

- `index.html`: CSS token trên `:root` + `[data-theme="dark"]`, font SF / Google Sans; Poppins (love.html)
- Dark/light theme toggle stored in `localStorage` key `theme`; light is default
- No JS framework — all interactivity is inline vanilla JS
- `contenteditable` + `localStorage` persist user-edited text across reloads
