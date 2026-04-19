# Site redesign — April 2026

## Pass 4 (2026-04-19, late evening)

Header layout and research-highlight carousel, per user feedback.

### Files touched (pass 4)

| File | Change |
|---|---|
| `_pages/about.md` | (1) Header order flipped: portrait now sits in the **left corner** next to the name/role/links block (was right-aligned, centred big). (2) Three research highlights (topology, IFE, energy) wrapped in a **horizontal slider** with prev/next arrow buttons and keyboard-accessible scroll-snap. Inline ~10-line JS wires up the arrows; the track is also fully swipeable/scrollable without JS (CSS scroll-snap). |
| `_sass/layout/_home.scss` | (1) `.home__header--with-photo` now a 110 px / 1fr grid (was 1fr / 160 px) — portrait ~30 % smaller, same column on mobile collapses to 86 px. (2) New `.slider*` component (track with `scroll-snap-type: x mandatory`, custom thin scrollbar, circular prev/next buttons positioned absolutely, hidden below 520 px). (3) `.highlights__card` now lives inside the slider with `scroll-snap-align: start`, fixed 260 px card width. (4) `.highlights__figure img max-height: 120 px` (was 180 px) — all thumbnails are smaller. (5) Dark-mode overrides added for the slider components. |
| `images/featured/energy-materials.png` | Resized via `sips -Z 650` — 1311×925 → 650×459, **1.3 MB → 335 kB** (74 % file-size reduction, ≥50 % dimension reduction). |
| `images/featured/ife-light-matter.png` | Resized via `sips -Z 900` — 947 kB → 478 kB for web optimization (still large enough to render cleanly on Retina). |

### Behaviour

- **Mobile / narrow:** arrow buttons hide, cards become 82 % viewport width; user swipes horizontally.
- **Desktop:** arrow buttons appear on the sides; click advances ~85 % of the track width. Cards snap into place.
- **No JS path:** the track is still scrollable with trackpad / shift-wheel; only the arrow-button shortcut requires the 10-line script.
- **Reduced motion:** `scroll-behavior: smooth` is the only animation; browsers respect `prefers-reduced-motion` natively when set.

### Still open / notes

- I did **not** add a fourth carousel slide for the Spin-IFE PRB 2023 paper — the current three are Topology / IFE (PRB 2025) / Energy per your previous message. If you want the Spin-IFE paper to be its own slide (with the dM/dI-vs-ℏω figure from your CV page), send me the figure PNG and I'll add it.
- `devcmgroup.nfshost.com` doesn't actually have a carousel — I checked. Its research layout is a static grid of clickable thumbnails. The slider here is a custom build that inherits the same minimal aesthetic (thin rule, neutral palette, serif titles), but the *motion* is our own choice since the reference didn't demo it.

---

## Pass 3 (2026-04-19, evening)

Targeted follow-ups driven by user feedback: expand Featured Research, refresh
contact/socials, and extend the home aesthetic to the Publications page.

### Files touched (pass 3)

| File | Change |
|---|---|
| `_pages/about.md` | (1) Header now has a circular portrait (1235×1235 photo, 160 px on screen) next to the name block. (2) Email updated everywhere to `shashi13@umd.edu`. (3) GitHub link removed (GitLab only). (4) Featured research now contains the H₃S hero **plus three new highlight cards** — Transport in topological materials, Inverse Faraday effect, Energy materials by design — each with a figure, venue, summary, and DOI. |
| `_pages/research.md` | (1) Overview rewritten in first person ("I study …" instead of "My group …"). (2) "Beyond-Migdal superconductivity" project renamed to **Superconductivity** and rewritten as two paragraphs to separate hydrides (non-adiabatic / vertex / anharmonic) from conventional Migdal-regime materials (Na-intercalated graphite). (3) EPW tile reworded: vertex corrections + **Berry curvature implementation** (replaces "topological point detection") + two-level MPI parallelization **for superconductivity**. (4) New **WannierBerri** tile: IFE implementation. (5) Collaborations updated: UMD (Murphy + Dev), Tohoku (Mori), IIT Madras (Nanda + Roy), new "Other collaborators" line with Akashi, Das, Rambabu. |
| `_pages/cv.md` | Email → `shashi13@umd.edu`, GitHub link removed (GitLab only). |
| `_pages/publications.html` | Rewritten: now uses `layout: home` (no sidebar), splits entries into **Journal articles** and **Conference proceedings** lists styled with the `.pubs` typography. Profile sidebar is gone — profile portrait appears only on the About page. |
| `_config.yml` | `author.email` → `shashi13@umd.edu`; `author.github` cleared (GitLab remains). |
| `_sass/layout/_home.scss` | New components: `.home__header--with-photo` + `.home__portrait` (circular avatar, grid that stacks on mobile), `.highlights*` (3-column figure/title/venue/summary/DOI cards) with dark-mode overrides. |
| `files/Shashi_CV.pdf` | Replaced with the latest CV from `/Volumes/Research/Shashi-Academics/CV.pdf` (132 KB). The About page no longer links the PDF — the `/cv/` page is the canonical CV — but the file is refreshed for anyone with a bookmarked URL. |
| `images/profile.png` | Refreshed from `/Volumes/Research/Shashi-Academics/IOP-B/Shashi-photo.png` (1235×1235, 363 KB). Now only consumed by the About header. |
| `images/featured/topological-transport.png` (new) | Rendered from `Proposals/figures/Toc_taas.pdf` via `sips`. |
| `images/featured/ife-light-matter.png` (new) | From `Proposals/figures/Ultrafast-res.png` (972×641). Stand-in until a dedicated IFE-curve figure is supplied; UCR group–style IFE plot is not yet available as a standalone asset. |
| `images/featured/energy-materials.png` (new) | From `Proposals/figures/energy-sch.png` (1311×925). |

### Known divergences / follow-ups

- The IFE highlight uses `Ultrafast-res.png` as a stand-in. If you want the
  specific dM<sub>IFE</sub>/dI-vs-ℏω plot from the PRB 2023 paper (the figure
  shown in the attached CV page), send me the raw PNG and I'll swap it in.
- Publications page: the Liquid split by `category` assumes the frontmatter
  correctly tags `conferences`. Today only `2017-05-lifepo4-md.md` is flagged,
  so the Conference Proceedings section has exactly one entry.
- `author.github` is now blank in `_config.yml`. The Minimal-Mistakes sidebar
  on any page still using `author_profile: true` (there are no such pages on
  the new site) would silently drop the icon rather than link somewhere wrong.

---

## Pass 2 (2026-04-19, later)

Extends the home aesthetic to the Research and CV pages, updates current
position to University of Maryland, and reconciles `_publications/` against
the canonical CV.

### Files touched (pass 2)

| File | Change |
|---|---|
| `_config.yml` | `bio`, `location`, `employer` → UMD College Park. |
| `_pages/cv.md` | Rewritten with `layout: home`. New UMD position (Assistant Research Scientist, ECE, Mar 2026–Present) added at the top; Binghamton moved to Apr 2023–Mar 2026. "Download PDF" link removed (content is now the canonical CV). Reorganized into tighter CV sections: Education · Appointments · Interests · Funding · Honours · Service · Teaching · Invited Talks · Contributed Presentations · Skills · Memberships · Publications (link). |
| `_pages/research.md` | Rewritten with `layout: home`. Four current-project cards (Beyond-Migdal, Topological transport, Light-matter, Energy materials), Code development tiles (EPW, EPWpy), and an updated Collaborations list including UMD. |
| `_sass/layout/_home.scss` | New component classes: `.cv-entry*`, `.cv-list`, `.projects*`. Dark-mode overrides added. Section `h2` labels remain 13px uppercase (design preserved). |
| `_publications/2026-01-taas-family-transport.md` (new) | PRB 113, 045202 (2026), TaAs family, Mishra*/Liu*/Tiwari/Giustino/Margine. |
| `_publications/2026-02-tio2-gas-sensing.md` (new) | *Mater. Sci. Eng. B* 326, 119210 (2026), Dey*/Mishra*/Hazra/Kabiraj/Roy. |
| `_publications/2025-03-h3s-d3s-nonadiabatic.md` | Updated from arXiv preprint to published version in *Ann. Phys.* 538, e00553 (2026). |
| `_publications/2025-01-vertex-corrections-h3s.md` | arXiv link → npj DOI `10.1038/s41524-025-01818-9`; venue short now includes *npj Comput. Mater.* **11**, 342. |
| `_publications/2021-06-graphdiyne-battery.md` | DOI corrected: `10.1021/acsaem.1c01462` → `10.1021/acsaem.1c01164`. |
| `_publications/2022-03-graphyne-battery.md` | DOI corrected: `10.1039/D2NA00238H` → `10.1039/D2NA00058J`. |
| `_publications/2025-01-weyl-transport-taas.md` | **Deleted** — duplicate arXiv stub of the published single-TaAs paper already captured in `2025-09-taas-carrier-transport.md`. |

### Still not touched

- Minimal-Mistakes partials, `_layouts/single.html`, `_layouts/default.html`.
- `_pages/publications.html` — still uses the archive layout; the home aesthetic is not applied there (it renders every `_publications/` entry automatically, which now totals 28 after the above fixes).
- `_pages/talks.html`, `_pages/teaching.html`.
- CV source (`CV.tex`) and IOP-B PDFs.

---

## Pass 1 (2026-04-19, committed as `abb5ed3`)

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
