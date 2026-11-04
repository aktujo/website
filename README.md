# aktujo – website

One static page for **aktujo**: no build step, no framework, no external resources, no cookies, no tracking.
A [falkOSS](https://falkoss.org) project.

| Path | What |
|---|---|
| `index.html`, `style.css`, `404.html` | the page (English) |
| `favicon.*`, `apple-touch-icon.png`, `icon-*.png`, `site.webmanifest`, `social.png` | head icons – **generated** by `brand/generate.py` in `aktujo/aktujo` (`brand/web/`), copied here |
| `assets/` | lockup and mark (from `brand/svg/`) |

Imprint and privacy policy are falkoss.org's – same operator, one place to keep them current.

Preview locally:

```sh
python3 -m http.server 8070
```

## Publishing

GitHub Pages via `.github/workflows/pages.yml` on every push to `main`. One-time setup: Repo → Settings → Pages →
Source: **GitHub Actions**.

The domain is **aktujo.org** (custom domain in the Pages settings, **Enforce HTTPS** once the certificate is there);
`canonical`, `og:url`, the absolute `og:image` and `Canonical:` in `.well-known/security.txt` point there, and
`404.html` uses root paths that resolve under it. aktujo.com and aktujo.eu redirect here (301, at the registrar);
aktujo.dev is the documentation (`aktujo/aktujo`), aktujo.app is kept for the apps (`aktujo/apps`).

## Licence

The site's code is **AGPL-3.0-or-later** (`LICENSE`); the brand's artwork (favicons, icons, `assets/`) is copied from
`aktujo/brand` under CC BY-ND 4.0, and the brand itself (name, logo, marks) is not covered by any licence.
