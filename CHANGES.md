# Homepage redesign — April 2026

Landing-page overhaul: new information architecture, serif-headed typography,
featured-research hero for the H₃S vertex-correction paper, and a curated top-10
publications list. Sub-pages (Publications, CV, Talks, Teaching, Research) are
untouched and keep their existing layout.

## Files touched

| File | Change | Why |
|---|---|---|
| `_pages/about.md` | Rewritten as the landing page with a custom HTML structure: header (name, role, email, Scholar/ORCID/GitHub/GitLab), About (≤120 words), Featured research (npj H₃S paper + figure + plain-language summary + DOI), four Research themes, ten Selected publications, CV download, Contact. | Implements the new IA; previous content was a dense markdown bulleted page with a sidebar profile. |
| `_layouts/home.html` (new) | Minimal full-width wrapper that inherits `default` but skips the author-profile sidebar. | Lets the home page diverge from the Minimal-Mistakes sidebar layout without affecting other pages. |
| `_sass/layout/_home.scss` (new) | All home-page styling, scoped under `main.home`. Design targets: body 16px, headings 20/24/30px on modular scale, Source Serif 4 headings + Inter body + IBM Plex Mono code, 780px column, line-height 1.65, ≥2rem section rhythm, `#111` on `#fafafa` with `#2c5282` single accent. Includes `[data-theme="dark"]` override. | Encapsulates the redesign without touching the existing Minimal-Mistakes partials that other pages depend on. |
| `assets/css/main.scss` | Added `"layout/home"` to the import list. | Compiles the new partial into `main.css`. |
| `_includes/head/custom.html` | Added Google Fonts preconnect + link for Inter, Source Serif 4, and IBM Plex Mono. | Serves the typefaces required by the spec. |
| `_data/navigation.yml` | Masthead is now `About · Research · Publications · CV · Contact`. Previous `Talks` and `Teaching` entries commented out. | Matches the spec IA. Pages themselves are preserved at `/talks/` and `/teaching/` for future reinstatement. |
| `images/featured/h3s-vertex-correction.png` (new) | Hero figure for the featured research card. Copied from `/Volumes/Research/Shashi-Academics/Proposals/figures/Toc_vertex.png` (902×915, PNG, ~191 kB). | The figure originally referenced in the research statement; caption: "Effect of vertex corrections in H₃S and Pb computed from DFT." |
| `CHANGES.md` (this file, new) | Changelog. |

## What was deliberately NOT touched

- `CV.tex` (per scope) — CV is served from `files/Shashi_CV.pdf`.
- Any PDF/TeX under `/Volumes/Research/Shashi-Academics/IOP-B/`.
- `_layouts/single.html`, `_layouts/default.html`, `_sass/theme/*`, `_sass/layout/*` other than the new `_home.scss` — existing sub-pages keep their current look.
- `_publications/`, `_talks/`, `_teaching/`, `_portfolio/` content. `Publications` subpage still lists all 29 items; the home page shows a curated 10.
- `_config.yml`, Gemfile, CI, and hosting configuration.

## Design targets vs. implementation

| Target | Implementation |
|---|---|
| Body 15–16px | `font-size: 16px` (drops to 15px on ≤480px) |
| Headings on modular scale 20/24/30 | `h3 20 / h2 24 / h1 30`, section labels 13px uppercase |
| Code 14px mono | `code` → IBM Plex Mono 14px |
| Content column 720–820px | `max-width: 780px` on `.home__wrap` |
| Line-height 1.6–1.7 | Body 1.65, About 1.7, section rhythm 2.5rem top/bottom |
| Serif headings + sans body | Source Serif 4 + Inter |
| Neutral palette `#111` on `#fafafa` + single accent | `#111` on `#fafafa`, accent `#2c5282` |
| Nav: About · Research · Publications · CV · Contact | Matches |
| External links `target="_blank" rel="noopener"` | Applied to every external link on the home page |

## Known divergences from the spec

- **Hero figure is near-square (902×915)**, not landscape, so it sits in a narrower right column (~320 px) next to the paper summary rather than as a full-width banner. At 1440 px the featured card still fits above the fold.
- **Role line says UMD, not Binghamton.** The user confirmed the Mar 2026 UMD position is now current; this supersedes the Phase-4 header text.
- **Publications are curated, not a strict Scholar top-10 cite count.** Per the user's direction the list highlights current research (superconductivity / electron-phonon / topology) plus two high-impact energy-materials papers. A citation-ordered list is still available at `/publications/`.
- **Dark mode** is supported via `[data-theme="dark"]` but the palette is a muted slate-navy, not the strict `#111` on `#fafafa` pair.

## How to run locally

Ruby 3.2 is required (Minimum for the pinned `github-pages` gem):

```
docker compose up   # or: bundle install && bundle exec jekyll serve
```

Site serves at <http://localhost:4000>. No build verification was performed in this working directory because the local Ruby is 2.6 — please run the build once before merging.
