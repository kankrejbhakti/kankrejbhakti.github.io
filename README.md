# Bhakti Kankrej — CV site

A single-page CV built as one `index.html`, with the portrait, social card, and downloadable PDF in `assets/`, plus the SEO files.

## Publish on GitHub Pages

1. Create a repository (for example `bkt-cv`) and push these files to `main`.
2. In the repository: **Settings → Pages → Build and deployment**
   - Source: **Deploy from a branch**
   - Branch: `main`, folder: `/ (root)`
3. Your URL will be one of:
   - `https://<username>.github.io/bkt-cv/` for a project site
   - `https://<username>.github.io/` if the repository is named `<username>.github.io`

## Replace before publishing

### 1. The site URL

Search for `YOUR-USERNAME` in:

- `index.html` — canonical, Open Graph, Twitter Card, and JSON-LD
- `robots.txt` — `Sitemap:`
- `sitemap.xml` — `<loc>`
- `README.md` — the examples above

If your repository is not called `bkt-cv`, also replace `bkt-cv` in those URLs and in the file names references above.

### 2. The CV download

The three “Download CV” links (header, hero, footer) point at `assets/bhakti-kankrej-cv.pdf`. To update the CV, replace that file and keep the filename — no HTML changes needed. The `download` attribute saves it as `Bhakti-Kankrej-CV.pdf`.

`CV -2026.pdf` in the project root is the untouched source file; it is not linked from the page.

## SEO checklist

- [ ] Absolute URL set in the canonical, `og:url`, `og:image`, Twitter, and JSON-LD tags
- [ ] `sitemap.xml` submitted in Google Search Console
- [ ] Page verified in Search Console (HTML tag or DNS)
- [ ] Structured data tested: <https://search.google.com/test/rich-results>
- [ ] Social card previewed: <https://www.opengraph.xyz/>
- [ ] If using a custom domain, add a `CNAME` file and update the absolute URLs

### Project-site note

GitHub project sites live at `https://<username>.github.io/<repo>/`. Google reads `robots.txt` only from the domain root, so `/bkt-cv/robots.txt` is not authoritative. The page-level `meta robots` and canonical still work; submit the sitemap directly in Search Console. With a custom domain or a `<username>.github.io` user site, the root `robots.txt` is used normally.

## Print

The page includes an A4 print stylesheet. Cmd/Ctrl+P prints a clean, text-first CV with the contact details on the first page. The figures, including the drawings section, are hidden in print.

## Files

- `index.html` — the page
- `assets/bhakti-kankrej-cv.pdf` — the downloadable CV
- `assets/portrait.jpg` — 860×1075 portrait, cropped from the source CV
- `assets/og-image.png` — 1200×630 social preview
- `assets/plan-typical.jpg` — typical floor plate drawing (Fig. 03)
- `assets/unit-2bhk.jpg` — 2 BHK unit plan (Fig. 04)
- `assets/unit-2-5bhk.jpg` — 2.5 BHK unit plan (Fig. 05)
- `assets/unit-3bhk.jpg` — 3 BHK unit plan (Fig. 06)
- `robots.txt`
- `sitemap.xml`
- `.nojekyll` — keeps GitHub Pages from running Jekyll
- `CV -2026.pdf` — source CV PDF (not linked from the page)
