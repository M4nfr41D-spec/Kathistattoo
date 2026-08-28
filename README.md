# KATTOO — v30 FINAL DEPLOY CANDIDATE

Prepared for `kattoo.online`.

## Runtime structure
- `index.html` — main KATTOO site
- `galerie.html` — tattoo portfolio
- `beyond-ink.html` — separate art portfolio
- `artworks.html` — backward-compatible redirect to Beyond Ink
- `assets/` — all visual/runtime assets
- `assets/gallery-manifest.json` — authoritative tattoo gallery curation
- `assets/artworks-manifest.json` — authoritative Beyond Ink curation
- `assets/artworks-data.js` — generated browser-safe mirror for local/static rendering
- `ASSET_MAPPING.json` — source/provenance and assignment mapping
- `CNAME` — `kattoo.online`

## Tattoo gallery
- 85 unique cards
- `Tattoo (1).zip`: 25/25 source images accounted for (6 new motifs, 19 duplicate/composite mappings)
- Color & Comic: 24
- Black & Grey: 35
- Fine Line: 21
- Confirmed Cover-up: 5
- New wing project is one motif with two views (`SW10A.webp`, `SW10B.webp`) to avoid a duplicate card.
- Cover-up status is never inferred automatically.

## Beyond Ink
- 32 unique artworks
- 6 paintings / 18 selected drawings / 8 sketches & studies
- 3 exact duplicate uploads were excluded
- Wide atelier artwork is the Hero visual
- Secondary artist visual is used lower on the page
- Real drawing-process photo is used in “Im Entstehen”

## Contact
Primary route: WhatsApp to Kathi at `+43 676 5174291`.
Core CTA: **„Schreib mir direkt auf WhatsApp“**.

## Deployment
This package is complete as a deploy candidate. Upload the contents of this folder to the GitHub Pages repository root.
