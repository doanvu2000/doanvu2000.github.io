# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static personal portfolio/landing page hosted on GitHub Pages (doanvu2000.github.io). No build system — pure HTML, CSS, and vanilla JavaScript served directly.

## Development

No build, lint, or test commands — open HTML files directly in a browser or use a local static server:

```bash
# Serve locally (Python)
python -m http.server 8080

# Or with Node (if installed)
npx serve .
```

## Architecture

- `index.html` — main landing page with social links, app shortcuts, Google search, and animated character
- `style.css` — all styling for `index.html`; uses CSS variables for dark theme
- `love.html` — standalone particle heart animation demo
- `fire/hpny2025.html` — fireworks animation using canvas + jQuery; self-contained in `fire/`

### Key patterns in index.html

- Editable text areas use `contenteditable` + `localStorage` to persist changes across page reloads
- No external JS framework — all interactivity is inline vanilla JS
- Google Fonts loaded via `<link>` (Noto Sans, Poppins)
- External CodePen script injected for additional animations
