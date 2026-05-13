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

- `index.html` — full portfolio with sections: About, Skills, Experience, Achievements, Projects, Community, Hobbies, Contact; progress bar + cursor canvas effects
- `style.css` — supplemental styling for `index.html`; primary styling via Tailwind CSS CDN
- `love.html` — standalone particle heart animation (canvas, black background, pink gradient text)
- `fire/hpny2025.html` — fireworks animation using canvas + jQuery; self-contained in `fire/`
- `jlsoft/lovequote/` — product marketing pages (overview.html + marketing.html) for the LoveQuote app
- `jlsoft/jadio/` — product marketing pages for the Jadio Podcast app
- `jlsoft/index.html` — JLSoft Together store landing page listing all apps (purple gradient, dark/light mode)

## JLSoft Product Sync Rule

Khi thêm sản phẩm JLSoft mới vào phần Projects của `index.html`, BẮT BUỘC cập nhật đồng thời `jlsoft/index.html`:
- Thêm app card mới vào `.apps-grid` với: logo, tên, mô tả, feature tags, nút Play Store, nút Xem chi tiết
- Cập nhật hero stats (số ứng dụng, các số liệu nổi bật)
- Thêm thư mục `jlsoft/<appname>/` với `logo.png` và `marketing.html`

### Key patterns

- Tailwind CSS loaded via CDN — no PostCSS/build step; utility classes used directly in HTML
- Google Fonts: Noto Sans, JetBrains Mono (index.html), Poppins (love.html)
- Dark/light theme toggle stored in `localStorage`; dark is default
- No JS framework — all interactivity is inline vanilla JS
- `contenteditable` + `localStorage` persist user-edited text across reloads
