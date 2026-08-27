# Teasoo Consulting — website prototype

A self-contained, static HTML/CSS prototype of the Teasoo Consulting website, including
the homepage, a **Products** menu (ESG Horizon), and a top-level **Projects** menu with
project pages — led by the **Tree4Life** reforestation flagship and the **Unilever**
stakeholder-management case study.

> **Why a static prototype?** The live site (teasooconsulting.com) runs on
> **WordPress** (Astra theme + Elementor Pro). Its pages are built visually inside
> WordPress, not from files in a git repo — so code committed here does not
> auto-publish to the live site. This prototype faithfully reproduces the brand and
> the new pages so they can be **reviewed, hosted as-is, or used as an exact build spec**
> for rebuilding in Elementor.

## What's here

| File | Purpose |
|------|---------|
| `index.html` | Homepage — existing look, **Projects** and **Products** menus, and the **Tree4Life flagship** section. |
| `tree4life.html` | The **Tree4Life** reforestation project page. |
| `unilever.html` | The **Unilever** stakeholder-management project page. |
| `products.html`, `esg-horizon.html` | Products overview + the ESG Horizon flagship. |
| `assets/css/style.css` | Shared stylesheet: Teasoo brand chrome + the forest-green project theme. |
| `assets/img/` | Optimised photos + Teasoo/ESG Horizon logos. |

No build step, no dependencies, no external requests. **Open `index.html` in a browser**,
or serve the folder (`python3 -m http.server`) and visit `/`.

## Content & branding rules (applied)

- **No public financial figures** anywhere — the one exception is a quantified cost
  *saving* Teasoo delivered (e.g. "saved ₦300M in operational cost").
- **No third-party sponsor branding.** Project pages present the work as Teasoo's own
  (e.g. **Tree4Life**), name other partners only where appropriate, and do **not** brand
  pages with a client/sponsor's name, logo, or photos without their approval. Other
  companies may be mentioned; the energy sponsor is not named.
- **Outcomes, not method.** Project pages publish results, impact and Teasoo capability —
  not internal strategy, selection process, or methodology that competitors could copy.
- **Global positioning.** Pages are written to sit alongside leading global firms and
  aligned to recognised international standards.

## Tree4Life page (current structure)

Full-bleed hero → outcome stats → why it matters → Teasoo capability
("from strategy to a standing forest") → impact outcomes → global-standard alignment
(UN Decade on Ecosystem Restoration, Bonn Challenge / AFR100) → community outcomes →
gallery → delivered-by (Teasoo) & partners → CTA. Forest-green content theme on the
project page only; header/footer stay on-brand.

## Porting to WordPress / Elementor

1. Add each project as a page under a `/projects/` parent and nest it under a **Projects**
   menu item in the Elementor header template.
2. Rebuild sections with Elementor containers using this prototype as the visual
   reference (stat bands, alternating text/image rows, card grids, gallery).
3. Upload the images in `assets/img/` to the Media Library, or swap in higher-resolution
   originals and approved stock/field media during the build.
4. On the homepage, add the **flagship** section (image container with overlay, heading,
   three stats and a button linking to the project page).
