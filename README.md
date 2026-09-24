# snagly_terms

Marketing site and privacy policy for [Snagly](https://play.google.com/store/apps/details?id=com.snagly.snagly), the UK new-build snagging app. Static HTML/CSS, no build step, deployed to GitHub Pages via `.github/workflows/deploy.yml` on every push to `main`.

## Structure

- `index.html` — landing page
- `privacy/index.html` — privacy policy, served at `/privacy/`
- `assets/css/style.css` — shared stylesheet
- `assets/img/` — screenshots (WebP, 2x) and icons
- `robots.txt`, `sitemap.xml` — SEO
- `CNAME` — custom domain (`snagly.house`); remove this file if the domain isn't set up yet, and GitHub Pages will fall back to the default `*.github.io` URL

Built from the design handoff in the main Snagly repo's `website/` folder (`WEBSITE.md`, `Snagly Website.dc.html`, `Snagly Privacy Policy.dc.html`) — see that folder for the source of truth on copy and visual spec.

## Local preview

Any static file server works, e.g.:

```
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Deployment

Push to `main`. GitHub Actions builds and deploys automatically via GitHub Pages. Enable Pages under **Settings → Pages → Source: GitHub Actions** on first setup.
