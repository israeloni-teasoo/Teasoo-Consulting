# Teasoo Consulting — Tree4Life page prototype

A self-contained, static HTML/CSS prototype that adds a **Tree4Life** project page to
the Teasoo Consulting website, plus the homepage **flagship** feature and a new
top-level **Projects** navigation menu.

> **Why a static prototype?** The live site (teasooconsulting.com) runs on
> **WordPress** (Astra theme + Elementor Pro). Its pages are built visually inside
> WordPress, not from files in a git repo — so code committed here does not
> auto-publish to the live site. This prototype faithfully reproduces the brand and
> the new page so it can be **reviewed, hosted as-is, or used as an exact build spec**
> for rebuilding the page in Elementor.

## What's here

| File | Purpose |
|------|---------|
| `index.html` | Homepage — existing look, **new Projects menu**, and the **Tree4Life flagship** section. |
| `tree4life.html` | The full **Tree4Life** project page (the new page). |
| `assets/css/style.css` | Shared stylesheet: Teasoo brand chrome + the forest-green project theme. |
| `assets/img/` | Optimised photos (from the 2024 Seplat Tree4Life deck) + Teasoo/Seplat logos. |

No build step, no dependencies, no external requests. **Open `index.html` in a browser**,
or serve the folder (`python3 -m http.server`) and visit `/`.

## Design decisions

- **Chrome matches the live site.** Palette taken from the live Elementor global kit
  (blue `#046bd2`, slate `#1e293b`/`#334155`, light bg `#F0F5FA`) with the red Teasoo
  logo. Header top-bar, sticky nav with dropdowns, and footer mirror the current site.
- **The new "Projects" menu** is a top-level dropdown; **Tree4Life** is its first item,
  flagged `FLAGSHIP`. The other existing case studies are listed as siblings.
- **The Tree4Life page** is modelled on the requested inspiration
  (treeaid.org/projects/tond-tenga): full-bleed hero → impact stats → about → why it
  matters → aims → goal quote → how it works → indigenous species → community &
  stories → 5-year roadmap → gallery → partners → CTA.
- **Forest-green content theme** is layered on the Tree4Life page only — thematically
  right for reforestation and consistent with the inspiration — while header/footer
  stay on-brand.

## Project facts used (source: 2024 Seplat Energy Tree4Life report)

- Launched 2022; Edo State forest reserve, Nigeria.
- Goal: **1,000,000 trees in 5 years**, rehabilitating **6,000 hectares**.
- 25-year MoU (renewable +25) → **~50 years** of carbon sequestration.
- Host communities: Obagie, Igieduma, Erua, Iruhie, Oke (1.6 km farming buffer,
  10% of seedlings shared as food trees, locally-trained plantation guards).
- Indigenous species incl. White/Black Afara, Opepe, Mahogany, Obeche, Okha, Odo,
  bamboo (10 identified with the Edo State Forestry Commission).
- Phased planting: 30k → 200k → 280k → 280k → 210k.
- Partners: Seplat Energy, Edo State Government / Forestry Commission,
  University of Benin (School of Life Sciences), Teasoo Consulting.

## Porting to WordPress / Elementor

1. Add a new page **Tree4Life** and set its permalink under a `/projects/` parent.
2. In **Appearance → Menus** (or the Elementor header template), add a **Projects**
   menu item and nest **Seplat Tree4Life Reforestation** beneath it.
3. Rebuild the sections with Elementor containers using this prototype as the visual
   reference. The stats band, alternating text/image rows, card grids, timeline and
   gallery all map to standard Elementor widgets.
4. Upload the images in `assets/img/` to the Media Library (or use higher-resolution
   originals from the project deck / Drive).
5. On the homepage, add the **flagship** section (single image container with overlay,
   heading, three stats and a button linking to the Tree4Life page).

## Media

Photos were selected and optimised from the *2024 Seplat Energy Tree4Life* presentation.
Additional field photos and summary videos are available in the project's Google Drive
folder and can be swapped in during the WordPress build.
