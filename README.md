# artwaresolutions.org

Marketing website for [Artware Solutions LLC](https://artwaresolutions.org), a company that builds software for entrepreneurs.

- **Artware CMS**: an art gallery management system
- **Checkmate Prep**: a chess game coach

It is a plain static site (HTML + CSS, no build step, no dependencies).

## Structure

| Path | Purpose |
| --- | --- |
| `index.html` | The single-page site (hero, products, about, contact) |
| `styles.css` | All styling; brand colors are CSS variables at the top |
| `404.html` | Page served by GitHub Pages for unknown URLs |
| `assets/logo.svg` | Official logo (vector, transparent background) |
| `assets/logo.png` | PNG logo, used for social sharing previews |
| `assets/favicon.png` | Favicon / touch icon |
| `.well-known/did.json`, `.well-known/did-configuration.json` | DID (`did:web:artwaresolutions.org`) documents |
| `CNAME` | Custom domain for GitHub Pages |
| `.nojekyll` | Tells GitHub Pages to serve the files as-is (no Jekyll) |

## Preview locally

```sh
python3 -m http.server 8000
```

Then open <http://localhost:8000>. Opening `index.html` directly in a browser also works.

## Deployment

The site is served by GitHub Pages straight from the root of the `main` branch (Settings → Pages → *Deploy from a branch*). Merging to `main` publishes it within a minute or two.

## Do not remove

- **`CNAME`**: removing it breaks the custom domain.
- **`.well-known/`**: these files back the site's DID identity and domain verification.
- **`.nojekyll`**: without it, GitHub Pages ignores dot-directories such as `.well-known`.

## Brand

- Blue `#21409A`, orange `#F5821F`, on a white background
- Tagline: *Solutions for the art world*
- The logo lettering is set in Handel Gothic and Bank Gothic. It is outlined in `assets/logo.svg`, so no font files are needed for the site.
- Contact: info@artwaresolutions.org
