# NF AI Workshop 2026

A two-day workshop bringing together NF researchers, clinicians, and AI experts to explore how agentic AI (Anthropic's Claude) can accelerate NF research. Participants attend a Discovery & Discussion Session with Anthropic's Head of Life Sciences Partnerships, then spend the afternoon building proof-of-concept AI projects with support from PhD-level technical assistants and field coaches. Projects are presented on the second day.

## Debugging / Local Development

This is a plain static HTML site — no build step required.

**Preview locally:**
```bash
# Python (built-in, any machine)
python3 -m http.server 8000
# then open http://localhost:8000/nf_conference2026/
```

**Common issues:**

| Problem | Likely cause | Fix |
|---|---|---|
| Styles not loading | Path to `css/style.css` is wrong | Check the `<link>` href is relative to the HTML file |
| Images not showing | Filename case mismatch or wrong path | Filenames are case-sensitive on Linux/GitHub Pages — verify `images/foo.jpg` matches exactly |
| Changes not appearing on GitHub Pages | CDN cache | Hard-refresh (`Ctrl+Shift+R`) or wait ~1 min after pushing |
| Layout broken on mobile | Missing viewport meta tag | Ensure `<meta name="viewport" content="width=device-width, initial-scale=1.0">` is in `<head>` |

**Browser DevTools** (F12) → Console tab shows JS errors; Network tab shows 404s for missing assets.

**Deployment:** Push to `main` — GitHub Pages serves the repo root automatically. No CI needed.
