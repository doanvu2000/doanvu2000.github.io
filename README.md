# doanvu2000.github.io

Personal portfolio site of **Doan Vũ** — Mobile Developer (Android · Java/Kotlin). Hosted on GitHub Pages.

🔗 Live: https://doanvu2000.github.io

## Stack

- Pure HTML / CSS / vanilla JavaScript — no build step
- Tailwind CSS via CDN
- Google Fonts: Noto Sans, JetBrains Mono, Poppins
- Dark / light theme toggle (persisted in `localStorage`)

## Pages

| Path | Description |
|------|-------------|
| `index.html` | Portfolio — About, Skills, Experience, Achievements, Projects, Community, Hobbies, Contact. Progress bar + particle / cursor canvas effects. |
| `love.html` | Standalone particle heart animation (canvas, black background, pink gradient text). |
| `jlsoft/lovequote/marketing.html` | Landing page for **Love Quote Story** Android app. |
| `jlsoft/lovequote/overview.html` | Technical overview of Love Quote Story. |
| `jlsoft/jadio/marketing.html` | Landing page for **Jadio Podcast** Android app. |

## JLSoft Products

- **Love Quote Story**
  - 🌐 Landing: https://doanvu2000.github.io/jlsoft/lovequote/marketing.html
  - 📱 Google Play: https://play.google.com/store/apps/details?id=com.jlsoft.lovequotestory
- **Jadio Podcast**
  - 🌐 Landing: https://doanvu2000.github.io/jlsoft/jadio/marketing.html
  - 📱 Google Play: https://play.google.com/store/apps/details?id=com.jlsoft.radio

## Local development

No build, lint, or test commands. Serve as static files:

```bash
# Python
python -m http.server 8080

# Or Node
npx serve .
```

Then open http://localhost:8080.

## License

Personal portfolio — content © Doan Vũ. Third-party assets retain their original licenses.
