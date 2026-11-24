# Rental One — Design System (proposal)

Status: **proposal only**, 24 November 2026, America/Chicago. Not owner-approved.  
This document codifies the brand as already written in `haydenclayne-ctrl/rental-one` (guidelines recorded 20 July 2026 from the founder’s brief, logo files replaced the same day) and as already implemented on the public site [rentaloneteam.com](https://rentaloneteam.com). It does not invent a new look. Do not treat this file as permission to restyle the brand or the site.

Machine-readable tokens: `tokens.json` and `tokens.css` in this folder. Inconsistencies and a prioritized consolidation list live in `audit.md`.

---

## 1. What this is, and what it is not

- **This company** is Rental One (RentalOne LLC) — a Cotton Co operating company, owned by High Cotton Capital. Positioning is **mission support, not equipment rental.** It supplies equipment, temporary infrastructure, labor, logistics, and FF&E from mobilization through completion, for commercial construction, industrial, manufacturing, general contractors, government, healthcare, education, and corporate facilities. The repo states “est. 1996”; that year was not independently verified in this pass and should not be treated as approved copy until confirmed.
- **Canonical brand source:** this GitHub repo (`brand-guidelines/`, `visual-identity/`, `CLAUDE.md`, owner-provided logos in `assets/logo/`). The live marketing site at [rentaloneteam.com](https://rentaloneteam.com) already implements those tokens in `css/styles.css` (the stylesheet itself cites `rental-one/visual-identity` as the source of truth). The website **codebase is not in this GitHub account**.
- **Endorsement:** “A Cotton Co Company,” in small letterspaced caps on corporate materials only — never locked into the logo, never inside its clear space, never a co-branded mark.
- **Not** High Cotton Capital corporate. Never import HCC Navy `#313E49`, HCC Gold `#CEA154`, Rajdhani, or the stag / CI badge.
- **Not** Cotton Co’s own black/gold identity. The parent relationship is endorsement type only.
- **Not** Blackhorn Global, Founders Ranch / High Cotton lifestyle, Roof Co Ventures, SE Roofing, Command, or Double Creek Ranch. Do not import those palettes, faces, or marks.
- **Not** the unrelated “Rental One” equipment company in Colleyville, Texas, acquired by Texas First Rentals in 2022, or RentalShare (named in older HCC notes as a marketplace). This system is only for Hayden’s Rental One / rentaloneteam.com (that “Hayden’s” wording is fine in this internal doc). Public pages, quote forms, cards, and signatures should not make Hayden the named contact — see Voice & copy.
- **Not** a request to restyle the brand. The logo is fixed artwork. The palette, type roles, chamfer, keyline, and plate are already decided.

---

## 2. Sources of truth

| Layer | Where | Status |
|---|---|---|
| Written brand | `haydenclayne-ctrl/rental-one` — start at `CLAUDE.md` and `README.md`, then `brand-guidelines/` and `visual-identity/` | Recorded 20 July 2026. This proposal extracts it. |
| Logo artwork | `assets/logo/r1-logo.png` (white on navy) and `r1-logo-2.png` (navy on light). The only approved artwork. | Shipping in the repo. `r1-logo-2.png` has a checkerboard baked into the pixels (no alpha). No SVG/EPS/AI. A standalone ONE-box file is specified but not in the repo. Concept-stage SVGs on Hayden’s Mac (`Documents/Rental One/output/brand-assets/`, coal/orange palette) are explicitly **do not use** and were not reviewed. |
| Live website | [rentaloneteam.com](https://rentaloneteam.com) — Home, Equipment, Services, Government, About, Request a Quote. CSS custom properties in `/css/styles.css` | Visually audited 24 November 2026 at 1440 and 390. No credentials used. Site source is not in this repo. |
| This proposal | `docs/design-system/` in `rental-one`, with copies under `/home/box/creative-dept/rental-one/design-system/` | Proposal only |

If the written guidelines and the live CSS disagree, the written guidelines win on brand facts (logo, palette, type roles, orange never on the logo, photography rules). The live CSS wins only as evidence of how the website currently implements those facts, including a few drifts called out in `audit.md`.

---

## 3. Brand direction

Rental One should feel like an **industrial operator** — strong, clean, modern, dependable, timeless. Think stamped equipment plates, staged yards, and contract-ready paperwork. It should never feel cheap, cartoonish, generic, playful, rustic, trend-driven, or busy.

**Default everywhere:** a navy field, a white logo, more white space than feels necessary. Navy dominates about 55% of any layout; white is the co-primary (~30%); Midnight about 10%; Steel Blue and Signal Orange each stay at or under 5%. Gold, cream, charcoal-warm, and other family palettes have no place here.

### Voice & copy

Voice: concise, confident, concrete. Lead with outcomes, short sentences, active voice, specifics over superlatives. No hype, no exclamation points, no buzzwords, no hedging, no humor at the trade’s expense. The brand never shouts.

**Elevator** (tightened from `messaging.md`; the “not just fill rental orders” construction is dropped):

> Rental One is a project support company. Equipment, temporary infrastructure, labor, logistics, and FF&E — one partner from mobilization to completion. Contractors and agencies call us to solve operational problems, not to place a rental order.

**Short boilerplate** (omit an unverified founding year until it is confirmed):

> Rental One provides equipment, temporary infrastructure, labor, logistics, and FF&E from mobilization through completion. A Cotton Co company.

**Tagline:** “One Source. Every Phase.” Campaign alternates, **one per composition, never stacked.** “Mobilize. Execute. Deliver.” is fine alone; do not stack it with other three-part lines (“Built to Keep Projects Moving.” / “Project Support, Delivered.”) in the same composition. The tagline sits outside the logo’s clear space, in display caps, at no more than 25% of logo width, and is never locked into the artwork.

**Public point of contact** is Pete Bell, not Hayden (per copy lead, pending Hayden confirmation). “Hayden’s Rental One” is fine in this internal design-system doc for disambiguation. Public pages, quote forms, cards, and signatures should not make Hayden the named contact.

If “jobsite campus” appears, prefer “Temporary offices and storage on an active jobsite,” or stay within the camp-rule limits already in this document.

Cotton Co’s `portfolio.md` still titles the sector “Equipment Rental.” That line should be retitled **Project support** (per copy lead, pending Hayden confirmation). That change belongs in the Cotton Co repo — do not edit `portfolio.md` from this PR, and do not visually mix Cotton Co black/gold into Rental One.

---

## 4. Color

Navy and white are the brand. Everything else supports them, quietly, in small doses. This palette supersedes the early concept palette (coal / field-white / orange `#FF5A1F`).

### 4.1 Primary

| Token | Hex | Print | Role |
|---|---|---|---|
| Rental One Navy | `#041E42` | PMS 282 C · CMYK 100/85/40/50 | The brand’s home. Measured from the owner-provided logo. Dominates every application. |
| Signal White | `#FFFFFF` | Paper | Co-primary, not an accent |
| Midnight | `#061024` | CMYK 100/85/45/70 (no Pantone; print from CMYK) | Deep grounds, dark environments, duotone shadows |

The logo PNG’s navy pixels cluster around `#021843` / `#011842` rather than a flat `#041E42`. Treat `#041E42` as the canonical token (as the repo already does). Do not “correct” the logo pixels, and do not introduce a second navy.

`visual-identity/applications.md` specifies business-card navy as **PMS 534**. That is a different ink from PMS 282 C. Until Hayden confirms, print navy is **282 C**. See `audit.md`.

### 4.2 Secondary and accent

| Token | Hex | Print | Role |
|---|---|---|---|
| Steel Blue | `#4F6DA8` | PMS 646 C · CMYK 75/55/10/5 | Charts, secondary UI, eyebrow labels, duotone highlights |
| Signal Orange | `#F26A21` | PMS 165 C · CMYK 0/70/95/0 | ≤5% of any layout. CTAs, safety cues, one rule or marker per composition. **Never touches the logo. Never a logo background.** |
| Concrete | `#C9CFD9` | Cool Gray 3 C · CMYK 8/5/0/15 | Dividers, secondary surfaces, spec tables |

### 4.3 Neutrals (navy-biased, never warm)

| Token | Hex | Role |
|---|---|---|
| Fog | `#F4F6FA` | Light page ground / section wash |
| Mist | `#D9DEE8` | Hero lead text on dark, cool mid light |
| Gunmetal | `#8B94A5` | Decorative mute only. **Fails AA** on white (3.05:1) and Fog (2.82:1). Never body or caption text below 18px, as the guidelines already say — and not at 18px on Fog either. |
| Iron | `#4A5262` | Muted body / lists on light (7.85:1 on white, 7.26:1 on Fog — AA/AAA) |
| Carbon | `#1C2027` | Body text on white |

True grayscale (`#FFF / #E6E6E6 / #B3B3B3 / #808080 / #4D4D4D / #000`) is for one-color print only, not for the website.

The live site also uses three undocumented hexes that should be folded into tokens or retired: eyebrow-on-dark `#9AB1D9` (a lightened steel, 7.61:1 on navy — AA), primary-hover `#FF7A31`, navy-hover `#0A2E5C`, and form-error `#C24A0E` (4.91:1 on white — AA).

### 4.4 Measured contrast (WCAG 2.x relative luminance)

- White on Navy 16.54:1, white on Midnight 18.96:1, Navy on white 16.54:1, Navy on Fog 15.29:1 — AAA.
- Carbon on white 16.34:1, Iron on white 7.85:1 — AAA. Use these for body and muted body on light.
- Steel Blue on white 5.14:1, on Fog 4.75:1 — AA at 16px+ (eyebrows at 12px on white are acceptable if treated as large/bold caps; prefer keeping them on white or Fog, not as 12px on a mid-tone).
- **Steel Blue on Navy 3.22:1, on Midnight 3.69:1 — fail AA for text.** The live site already avoids this by using `#9AB1D9` for eyebrows on dark. Promote that (or Concrete / Mist) as the official on-dark eyebrow, rather than Steel itself.
- **Signal Orange on white 3.06:1, on Fog 2.83:1 — fail AA and, on Fog, large-text AA.** Orange is for graphics and large display only, never body text, as already written. The primary button is navy type on orange (5.40:1 — AA). Keep it that way.
- Orange on Navy 5.40:1, on Midnight 6.19:1 — AA, fine for a large rule or a large display word on dark.
- **Gunmetal on white 3.05:1, on Fog 2.82:1 — fail AA.** Gunmetal on Midnight 6.21:1 and on Navy 5.42:1 — AA (footer mute on dark is fine).
- White on a 40–60% navy scrim over mid-value photography stays at or above ~4.6:1 in typical cases; always check a light photograph at the 40% end.

Proportion reminder: **Navy 55 · White 30 · Midnight 10 · Steel ≤5 · Orange ≤5.**

---

## 5. Typography

Three roles, three families. Never a fourth face in one composition.

| Role | Face | Weights | Use and rules |
|---|---|---|---|
| Display | **Industry** (Fort Foundry) | Bold, Black | Always ALL CAPS (the written H3 exception for mixed case should be closed — keep H3 in caps). Octagonal industrial forms that echo the logo without imitating it. Alternates: United Sans, Tungsten. Licensed (Adobe Fonts / MyFonts). Written rule: never below 18px, never for paragraphs. The live site’s buttons use Industry at **13px**, which contradicts that floor. |
| Text | **Archivo** (Google Fonts) | Regular–Bold | Body, UI, documents. Never letterspaced. Digital alternate: Roboto. Web-safe: Arial. |
| Data | **IBM Plex Mono** | Regular, Medium | Spec tables, equipment IDs, dates, part numbers, eyebrow labels. Web-safe: Consolas / Menlo. |

The live site loads Archivo (variable width 62–125 and weight 100–900) and IBM Plex Mono from Google Fonts. **Industry is named in the stack but is not embedded** — no Adobe Fonts / Typekit link, no `@font-face`. Display type currently falls back to Archivo at `font-stretch: 87%`, which approximates a condensed industrial face but is not Industry. Office and print work that use the licensed face will not match the website until a webfont license is in place.

### 5.1 Hierarchy (written)

| Level | Spec |
|---|---|
| Eyebrow | Plex Mono Medium · 12/16 · +22% tracking · caps · Steel Blue on light; a lighter steel (live: `#9AB1D9`) on dark |
| H1 | Industry Black · 44/48 · +1.5% · caps |
| H2 | Industry Bold · 28/32 · +2% · caps |
| H3 | Industry Bold · 19/24 · caps (proposal: close the “mixed case allowed” note) |
| Body | Archivo Regular · 16/26 · max ~65ch · Carbon |
| Lead | Archivo · 18 / ~1.66 · max 65ch (live site; not in the written table, useful) |
| Caption | Archivo Regular · 12.5/18 · Iron (not Gunmetal) |
| Button | Industry Bold · 13 · +10% · caps · min-height 48px (live). Reconcile with the 18px display floor — either raise the button to 18px or formally exempt UI labels from the floor. |

The live CSS uses fluid display sizes that overshoot the written caps: H1 `clamp(34px, 4.6vw, 58px)` (58 vs 44), H2 `clamp(28px, 3.4vw, 40px)` (40 vs 28), H3 `clamp(19px, 2vw, 23px)`. Phone H1 at 34px is a reasonable fluid floor. Recommendation: keep the fluid behaviour, but cap H1 at 44px and H2 at 32px unless Hayden prefers the larger live sizes.

---

## 6. Logo and mark

The logo is a framed industrial lockup: RENTAL in blocky octagonal capitals, the ONE box breaking the bottom keyline, the date split “19 / 96,” and the ®. It reads like a stamped equipment plate — permanent, load-rated, certified.

**The logo is fixed.** Never redraw, retype, auto-trace, restyle, recolor, rearrange, or substitute a typeset “Rental One.” The only approved artwork is the owner-provided files:

- `r1-logo.png` — white lockup on a Rental One Navy field, 1254×1254, RGB, no alpha. Default, the brand’s home state. Used (cropped / isolated as `r1-logo-white.png`) in the live header and footer.
- `r1-logo-2.png` — navy-and-white lockup intended for light surfaces, 1254×1254, RGB, **no alpha**. A light checkerboard (`#FEFEFE` / `#F0F0F0`) is baked into the pixels. Do not place this file on any real background. Request a transparent master rather than editing this file.

Approved versions (several have no file yet): white on navy (default); navy on white; one-color white; one-color black (fax, engraving, newsprint); **ONE box** as the secondary mark for avatars, favicons, hard-hat decals, and any use below the full-lockup minimum.

Clear space: 1X on all sides, where X is the cap height of “ONE” in the box. Minimum full lockup: print 1.25 in / 32 mm wide · digital 120 px wide · embroidery 2.5 in. Below that, use the ONE box (min 0.5 in / 48 px). The live header already scales the full lockup to 120 px at the 1020 px breakpoint — that is the floor, not a target to go under.

Backgrounds that are allowed: Navy, Midnight, white, black; photography with a 40–60% navy scrim behind the logo zone; high-contrast physical materials. Not allowed: mid-tones, gradients, patterns, busy photography without a scrim, any orange or accent-colored background.

Never stretch, condense, rotate, add effects or shadows or outlines, remove the keyline or dates, place the logo inside a containing shape, or animate it beyond a simple fade.

---

## 7. Spacing, layout, and shape

The written system is an 8-point grid, a 12-column page, 24 px gutters, and margins of at least 6% of page width. Hard column alignment; centered layouts only for covers and dividers. Minimum 30% empty space. One idea per spread, one focal point per layout. If a layout needs a third typeface, a second accent, or a fourth element to work, it doesn’t work.

The live site implements that as:

| Token | Value | Role |
|---|---|---|
| space 1–15 | 8 / 16 / 24 / 32 / 40 / 48 / 64 / 80 / 96 / 120 px | The 8 px scale |
| container | 1200 px | Main measure |
| page gutter | `max(24px, 6vw)`, 24 px from 1400 px up | Matches the ≥6% rule at typical widths |
| header | 96 px (80 px below 1020 px) | Sticky navy bar |
| chamfer | 18 px, small 12 px | 45° cut, one or two corners, never all four |
| keyline | 3 px solid navy (white on dark) | Frames feature content; elements may break it, like the ONE box |
| orange rule | 56×4 px | One per composition, never on the logo |
| button | padding 17/32/15, min-height 48 px, small chamfer on the primary | Capsule is not this brand — the chamfer is |
| tap | 48 px minimum on buttons | Live primary / ghost buttons |

There is no rounded-corner language and almost no drop shadow in the system. Elevation comes from the keyline, the plate, and the chamfer, not from soft UI shadows. Do not import Command’s card shadows or Founders Ranch radii.

**Graphic devices:** the Chamfer, the Keyline, and the Plate (mono-set data blocks styled like equipment ID plates, e.g. `UNIT R1-0448 · 20FT · CLIMATE`). Pattern: only a fine blueprint grid, Steel Blue at 8–12% opacity on navy, and only on large fields (trade-show walls, cover interiors). No hazard stripes, no textures, no gradients beyond navy→midnight.

---

## 8. Components (as the live site already draws them)

There is no component package in the GitHub repo. The live CSS is the de facto component layer. New work should match it, not invent a second set.

| Component | Behaviour |
|---|---|
| `.btn--primary` | Signal Orange fill, navy type, small chamfer on the top-right. Hover `#FF7A31` (undocumented). |
| `.btn--navy` | Navy fill, white type. Hover `#0A2E5C`. |
| `.btn--ghost` / `.btn--ghost-navy` | 2 px inset keyline, no chamfer, inverts on hover. |
| `.text-link` | Plex Mono, 13 px, caps, navy with a 2 px orange underline. |
| `.eyebrow` | Plex Mono, 12/16, +22% tracking, caps. Steel on light; `#9AB1D9` on dark. |
| `.plate` / `.plate--dark` | Mono, uppercase, 1 px concrete (or steel at 45%) frame. |
| `.keyline` | 3 px frame. |
| `.rule-orange` | The one allowed orange bar. |
| Cards (`.cap-card`, `.eq-card`) | Chamfered photo or icon block, display title, Archivo body, optional plate. |
| Forms | Fog or white shell, 16 px inputs (so iOS will not zoom), 12 px mono labels, error text `#C24A0E`. Quote page is a public form; this audit did not submit it. |
| Header | Navy, white lockup, mono nav (Equipment, Services, Government, About), orange “Request a Quote.” |
| Footer | Midnight or navy, endorsement line, gunmetal meta (AA on dark). |
| Icons | Geometric line icons, ~24 px grid, 2 px stroke, square terminals, 45° cuts where a radius would appear. One color only (navy on light, white on navy). No filled icons, no rounded “friendly” sets, no emoji. The live site’s inline SVGs follow this. |

Focus-visible on buttons is a 3 px Steel ring. `prefers-reduced-motion` is honoured (reveals and transitions collapse). A skip link is present.

---

## 9. Navigation and page structure

Live information architecture, navy header throughout:

| Path | Page |
|---|---|
| `/` | Home — hero, service lines, contract-ready band, Mobilize / Execute / Deliver, fleet cards, markets, close CTA |
| `/equipment` | Equipment & temporary infrastructure |
| `/services` | Labor, project support, FF&E & relocation |
| `/government` | Contract-ready / government work |
| `/about` | Positioning, endorsement, platform backing |
| `/quote` | Request a quote |

Website application of the brand, from `applications.md`: navy headers and heroes, white content sections, Signal Orange CTAs only. That is what the live site does. Stationery, fleet, PPE, apparel, and trade-show rules in that file remain the standard for non-web work.

---

## 10. Responsive behaviour

From the live CSS (the written guidelines do not publish breakpoints):

| Width | Behaviour |
|---|---|
| `< 520 px` | Check-grids collapse to one column |
| `< 560 px` | Footer becomes a single column |
| `< 640 px` | Card grids one column; form padding tightens |
| `< 800 px` | Form check-grids two columns, then one |
| `< 900 px` | Splits, stat bands, process steps, and the footer main stack |
| `< 1020 px` | Nav becomes a full-screen navy drawer (hamburger). Header 80 px. Logo 120 px wide (the digital minimum). Card and industry grids go to two columns, then one at 640. |
| `≥ 1400 px` | Container gutters lock at 24 px |

The 1440 and 390 passes on Home and About hold together: the chamfered orange CTA remains thumb-reachable, type does not overflow, the navy scrim keeps the hero headline at high contrast, and the 390 hero does clip the lower plate row slightly under the fold — a minor layout note, not a brand break.

---

## 11. Icons and imagery

Icons are the geometric line set described above. Do not introduce Lucide, filled icons, or another family’s marks.

### 11.1 Photography treatment (already written)

Documentary, not stock. Full color runs cool and slightly desaturated (−10 to −20%). Duotone for covers and dividers maps shadows to Midnight `#061024` and highlights to Steel Blue `#4F6DA8`. Text zones over photographs get a 40–60% navy scrim.

**Yes (general):** real crews and equipment on active sites; low-angle hero shots; dawn/dusk steel-blue light; order in the frame (staged yards, aligned fleets, clean sites); wide establishing shots paired with close texture.

**No (general):** stock handshakes; models pointing at clipboards; warm filters, HDR, or vignettes; cluttered, unsafe, or unbranded jobsites.

The live site currently uses Unsplash stills for every photograph. That already breaks the “documentary, not stock” rule. Subject-by-subject notes, including the camp rule, are in the next section and in `audit.md`. None of the live stills are Rental One’s own photography.

### 11.2 The camp rule — Rental One must never resemble the old workforce camps

Rental One provides temporary infrastructure and labor on other people’s projects. That work can include portable offices, modular facilities, and climate-controlled storage. It must **never** look like, or be mistaken for, the old oilfield and construction workforce camps — the Mentone example and places like it: rows of housing trailers on a dusty lot, a self-contained “man camp,” bunkhouses and mess halls as the subject, an isolated desert settlement of temporary living quarters.

The brand is mission support on a professional jobsite, not a place where a workforce lives. Photography, illustration, aerials, and copy (including “campus,” “village,” “camp,” and “housing”) must keep that line obvious.

**Do (in words, not pictures):**

- A small cluster of clean, current portable offices or climate-controlled containers sitting on an active commercial, industrial, healthcare, education, or government site, with the project visible in the frame — a building going up, a plant, a campus, a right-of-way — so the units read as jobsite infrastructure, not as a place to sleep.
- One or two modular offices, levelled and aligned, with safe access, power dressed in, and a crew clearly working, not loitering at a doorway.
- Staged equipment yards and aligned fleets on gravel or pavement, photographed in cool light, with order in the frame.
- Interior of a portable office or climate container set up as a workplace: desks, plans, PPE, charging, inventory — a job running, not a bunkroom.
- Wide shots that privilege the project and the work, with temporary facilities as a supporting element.

**Don’t (in words, not pictures):**

- Rows of weathered or identical housing trailers, “man camp” streets, bunkhouses, laundry lines, picnic tables between units, or any frame whose subject is where people live.
- Isolated desert or oilfield settlements of temporary housing, dusty unpaved camp loops, and aerials of trailer grids with no active project in view — the Mentone-class picture.
- Dense fields of shipping containers, photographed like a village or a settlement, used to stand in for “offices,” “modular facilities,” or a “jobsite campus.” A working seaport or a stacked container terminal is also the wrong metaphor for Rental One’s climate storage and jobsite offices.
- Mess halls, rec rooms, dorm interiors, or “home away from home” language and pictures.
- Copy that leans on “camp,” “crew village,” “workforce housing,” or an unscoped “campus” in a way that could be read as living quarters. If “jobsite campus” is used, it may only mean temporary workplace infrastructure on an active project, and the picture must make that unmistakable.

On the live site, **no photograph is a Mentone-style workforce camp.** The one image that gets too close to the rule, because of how it is used, is the dusk aerial of a dense container terminal (Unsplash `photo-1590496793929`), placed under “Offices & Climate Storage” with the line “a working jobsite campus, delivered,” and reused in a similar role on Equipment. Replace it with a clean modular office or climate container on an active commercial or government site. A seaport-and-container-ship still (Unsplash `photo-1578575437130`) has the same problem as a metaphor, even though it is clearly a port and not a camp.

---

## 12. Motion

The live site uses a modest rise-and-fade on scroll (24 px, 0.6 s, staggered). Header and drawer transitions are short (~0.2–0.25 s). Buttons shift color in 0.18 s. Logo animation, if any, is a simple fade only. `prefers-reduced-motion: reduce` disables the reveals and button transitions and turns off smooth scrolling. Keep that. Do not add a long logo intro or decorative motion.

---

## 13. Accessibility

Already in good shape on the live site: skip link, focus-visible rings, reduced-motion support, navy-on-orange buttons that meet AA, hero type on a navy scrim, 48 px button height, 16 px form inputs.

Still to fix, without changing the look of the brand:

- Do not use Gunmetal for text on white or Fog. Use Iron or Carbon.
- Do not use Steel Blue as 12 px text on Navy or Midnight; use the lighter on-dark eyebrow (`#9AB1D9` or Concrete / Mist).
- Do not use Signal Orange as text on white or Fog.
- Confirm every text-on-photograph pairing at the light end of the 40% scrim.
- When Industry is embedded, check that 13 px button caps still meet the size and contrast expectations, or raise them.

---

## 14. Tokens and engineering convention

- Written brand facts live in this repo’s markdown. Live implementation lives in [rentaloneteam.com](https://rentaloneteam.com)/css/styles.css, which is not in the repo.
- This proposal’s `tokens.css` / `tokens.json` use a `--r1-` prefix and extract both sources. Do not wire them into a production build until Hayden approves the system.
- New work uses these tokens, the three type roles, the chamfer / keyline / plate, and the photography rules including the camp rule. Do not add undocumented hexes, a fourth typeface, or another family’s components.
- Do not launch a restyle from this document. Consolidation only, tagged in `audit.md` as REFINEMENT or BRANDING.
