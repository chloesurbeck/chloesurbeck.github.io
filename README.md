# Chloe Surbeck (Phuong Lan Tanaka) — Unified Portfolio & Website

This repository hosts the unified personal, quantitative risk / data science, and visual arts website for **Chloe Surbeck (Phuong Lan Tanaka)**.

- **GitHub Pages URL**: <https://chloesurbeck.github.io>
- **Custom Domain**: <https://phuonglantanaka.com>
- **GitHub Repository**: <https://github.com/chloesurbeck/chloesurbeck.github.io>

---

## Site Architecture

1. **Home (`index.qmd`)**: Combined landing and biography page featuring pronouns (`she/her`), micro-biography, academic & industry snapshot (UBC MDS, Temple University Economics), photos, and social/contact links.
2. **Risk & Validation (`risk-validation.qmd`)**: UBC MDS 6-Block composite portfolio featuring unified 3-act validation papers (Quant Build, MRM Audit, Governance Synthesis) paired with links to GitHub repositories and interactive risk applications.
3. **Arts & Draft (`arts-and-drafts.qmd`)**: Visual arts, collage, illustration, and rough animation portfolio (2020–2025) migrated from `phuonglantanaka.com/portfolio`.
4. **Metric Monday *(Reserved / Not Yet Active)***: Commented out in `_quarto.yml` for future ongoing tracking & media essays.

---

## Local Build & Preview

```powershell
# Render full site into docs/
quarto render

# Live preview locally
quarto preview
```

---

## Linking `phuonglantanaka.com` to GitHub Pages (When Ready)

1. In your domain registrar (GoDaddy) DNS settings for `phuonglantanaka.com`:
   - Add four `A` records for `@` pointing to GitHub Pages IPs:
     - `185.199.108.153`
     - `185.199.109.153`
     - `185.199.110.153`
     - `185.199.111.153`
   - Add a `CNAME` record for `www` pointing to `chloesurbeck.github.io`.
2. In GitHub (`Settings -> Pages -> Custom domain`), enter `phuonglantanaka.com` and enable **Enforce HTTPS**.
