# Personal Website — Yiyuan (Ian) Chen

Single-page personal/résumé site (modern dark theme), built as static HTML/CSS/JS — no build step, deploys directly to GitHub Pages.

## Structure
```
index.html        # all content (single page)
css/styles.css    # dark theme
js/main.js         # scroll reveal + active-nav
assets/resume.pdf  # downloadable résumé (converted from source docx)
```

## Local preview
```bash
cd personal-website
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy (GitHub Pages)
Push to a GitHub repo, then enable Pages:
- **User site:** repo named `<username>.github.io`, served from `main` branch root.
- **Project site:** any repo name, Settings → Pages → Deploy from `main` / root.

## Update résumé content
Edit `index.html` directly. To refresh the PDF from a new Word doc:
```bash
libreoffice --headless --convert-to pdf --outdir assets "<new.docx>"
mv assets/<new>.pdf assets/resume.pdf
```
