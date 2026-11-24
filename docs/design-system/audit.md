# Rental One — design audit

24 November 2026, America/Chicago. Proposal companion to `DESIGN_SYSTEM.md`.  
Scope: `haydenclayne-ctrl/rental-one` at `main` (`5d1bf47`, last push 20 July 2026), a read-only look at Cotton Co and High Cotton Capital for endorsement and naming context only, and a visual pass of the public site [rentaloneteam.com](https://rentaloneteam.com) at 1440×900 and 390×844. No app or site code was changed. No credentials were used. No form was submitted. Login screenshots and local copies of the public stills sit under `/home/box/creative-dept/rental-one/design-system/screenshots/` (not in the PR).

Tags: **REFINEMENT** (implementation cleanup that preserves the look) or **BRANDING** (needs Hayden, or a check against master artwork / a license).

---

## How the audit was done

- Read the Design Library entry, listed `haydenclayne-ctrl` repos, and cloned `rental-one`, plus `cotton-co` and `high-cotton-capital` for context. No other Rental One repo exists on this account. `caldwell-solutions` is named in the library but is no longer resolvable.
- Read every file in the brand repo, measured both logo PNGs, and computed contrast for the official palette.
- Screenshotted Home, About, Equipment, Services, Government, and Quote on the live site; extracted `/css/styles.css` custom properties, type, breakpoints, and every `<img>`.
- Judged each live photograph, in words, against the written photography rules and against the camp rule (Rental One must never resemble the old workforce camps, for example Mentone).

---

## Repos and properties

| Source | What it is |
|---|---|
| [haydenclayne-ctrl/rental-one](https://github.com/haydenclayne-ctrl/rental-one) (public) | The brand repo. Guidelines + two logo PNGs. No website code, no token files (until this proposal), no vectors. |
| [rentaloneteam.com](https://rentaloneteam.com) | The live marketing site. Implements the written tokens closely. Source is not in this GitHub account. |
| cotton-co, high-cotton-capital | Parent context and endorsement only. Cotton Co’s `portfolio.md` still describes Rental One as “Equipment Rental,” which lags the “mission support / project support” position. Retitle that sector line to **Project support** (per copy lead, pending Hayden confirmation) in the Cotton Co repo — not in this one, and not on `main`. |

---

## Current state (summary)

The written brand is unusually complete for a repo with no website inside it: a locked logo, a full palette with Pantone and proportion, three type roles, chamfer / keyline / plate, application rules, and a clear voice. The live site already looks like that system — navy header and heroes, white content, chamfered orange CTAs, Archivo body, Plex Mono eyebrows, 8 px spacing, 1200 px measure, 40–60% navy scrims.

The gaps are production assets and adoption details, not a missing direction. There are no vector or transparent logo masters. Industry is not actually loaded on the web. Every photograph is Unsplash stock, and a few of those stills are the wrong subject. The camp rule is not yet written into the brand repo; this proposal adds it. No live still is a Mentone-style workforce camp, but one container-terminal aerial is used in a way that gets too close.

---

## Inconsistencies

### Logo and assets

1. **`r1-logo-2.png` is not a usable light-ground master.** The checkerboard is baked into the RGB pixels; there is no alpha channel. It cannot be placed on Fog, photography, or any real field without the checks showing.
2. **No vector, no transparent white lockup, no ONE-box file in the repo.** The guidelines specify one-color versions and a secondary ONE-box mark. The live header uses a cropped white lockup (`/assets/r1-logo-white.png`) that is not in the GitHub repo. Concept-stage SVGs were deliberately removed on 20 July 2026 (“drop reproductions”) and must stay dropped. The README still says `assets/logo/` holds “vector reproductions.”
3. **Pixel navy vs token navy.** Canonical token `#041E42` is correct per the repo notes. The navy field in `r1-logo.png` clusters around `#021843` / `#011842` (export / compression). Do not fork a second navy.
4. **Business cards specify PMS 534** in `applications.md`, while the brand navy is PMS 282 C. Those are different inks.

### Color and type

5. **Live site adds four hexes not in the written palette:** `#9AB1D9` (eyebrows on dark — a good, AA-safe idea), `#FF7A31` and `#0A2E5C` (button hovers), `#C24A0E` (form errors).
6. **Gunmetal fails AA on light grounds** (3.05:1 on white, 2.82:1 on Fog). The written rule already forbids it below 18 px; it also fails large-text AA on Fog. The live footer uses it on dark, which is fine (5.42:1 on navy).
7. **Steel Blue on navy/midnight fails AA** (3.22 / 3.69). The live site already works around this with `#9AB1D9`.
8. **Signal Orange on white/Fog fails AA.** Already restricted to graphics and large type; the primary button correctly uses navy on orange (5.40:1).
9. **Industry is not embedded.** The live stack names it, then loads only Archivo (variable width) and IBM Plex Mono from Google Fonts. Display is Archivo at `font-stretch: 87%`. Print and web will not match.
10. **Display size conflicts.** Written: Industry never below 18 px; buttons are specified at 13 px. Written H1/H2 are 44/28; the live CSS caps them at 58/40. Written H3 “mixed case allowed” fights “display is always ALL CAPS.”

### Components, layout, engineering

11. **The website is not in the repo.** Tokens on the live site can already drift from the markdown, and there is no shared package to keep them together.
12. **Cotton Co / HCC copy is stale.** Cotton Co still headlines Rental One as “Equipment Rental.” Retitle it **Project support** (per copy lead, pending Hayden confirmation) in Cotton Co `portfolio.md` — do not edit that file from this PR or on `main`. Older HCC notes also list a “RentalShare” marketplace; that is out of scope here and must not be visually mixed in.
13. **Copy cleanup (from the 24 November copy-lead review).** Tighten the elevator to “Contractors and agencies call us to solve operational problems, not to place a rental order.” Keep “Mobilize. Execute. Deliver.” as a standalone campaign line; do not stack it with other three-part lines. The public POC is Pete Bell, not Hayden (per copy lead, pending Hayden confirmation). Do not treat “est. 1996” as approved copy until it is confirmed.
13. Shadows and radii are correctly mostly absent. Do not “improve” the UI with another product’s card shadows.

### Imagery (including the camp rule)

Every live photograph is an Unsplash stock still. That already violates “Documentary, not stock.” Subject-by-subject:

| Live use | Unsplash id | Camp rule | Other issues |
|---|---|---|---|
| Home / Government hero: cranes over a high-rise | `photo-1591955506264` | Does not violate. Active urban project, low-angle, navy scrim. | Stock; source still is black-and-white (the scrim saves it on the page). |
| Home / Government: two supervisors pointing | `photo-1626885930974` | Does not violate. | Stock “people pointing at a site”; warm sun; **Delawie** (another firm) on the hard hat; Uline vest. Close to the written “models pointing” ban. Government alt text calls it a “federal project,” which the picture does not establish. |
| Home “temp power” / About hero / About crew | `photo-1504307651254` | Does not violate. | Stock. Home alt says “temporary power distribution”; the frame is rebar and a concrete deck, not temp power. Somewhat cluttered. |
| Home / Equipment: “telehandler” | `photo-1616401784845` | Does not violate. | Indoor retail/wholesale reach truck and boxed consumer goods — not construction material handling. |
| Home / Equipment: “Offices & Climate Storage,” “jobsite campus” | `photo-1590496793929` | **Too close, because of use.** A dusk aerial of a dense container terminal, used to stand in for jobsite offices and a “campus.” Not Mentone and not housing, but a container field as “campus” is the wrong metaphor and can start to read as a settlement. Replace. | Stock; seaport, not a Rental One yard. |
| About / Equipment: “technician servicing equipment / a generator” | `photo-1517524206127` | Does not violate. | A man in a t-shirt, no PPE, working on a small engine / buggy in a corrugated workshop. Rustic, which the personality rules forbid. It is not a generator and not heavy equipment. |
| About / Services / Equipment: crew on a slab | `photo-1541888946425` | Does not violate. Active institutional jobsite, PPE on. | Stock; warm daylight. |
| Equipment hero: excavators and haul trucks | `photo-1523848309072` | Does not violate. | Open-pit mine / quarry, not the commercial, government, or healthcare work the site sells. |
| Equipment: “modular structures” | `photo-1508450859948` | Does not violate. | A concrete building shell with shoring — not portable offices or modular facilities. Misleading alt. |
| Equipment / Services: port cranes and ships | `photo-1578575437130` | Does not violate as a picture of a port, but is the **wrong metaphor** for jobsite logistics or climate storage (same family of problem as the container aerial). | SSA Terminals, container ship “NORTHERN JUSTICE.” |
| Services: crew at height | `photo-1516216628859` | Does not violate. | Stock; **MIDAS** work shirts; bright, warm sky. |
| Services: high-bay warehouse | `photo-1553413077` | Does not violate. | Generic boxed inventory, a trash can in the aisle; not a Rental One warehouse. |

**Camp-rule verdict:** no live photograph depicts a Mentone-style workforce camp (housing trailers, bunkhouses, isolated desert man-camps, living quarters as the subject). The container-terminal aerial — and, as a metaphor, the container-ship still — should be retired from offices / storage / “jobsite campus” use. The camp rule itself is not yet in `visual-identity/visual-style.md`; this proposal writes it.

---

## Prioritized recommendations

Work these in order. None of them restyle the brand.

### 1. Replace the Unsplash set, and apply the camp rule — REFINEMENT (photography), with a BRANDING decision on commissioning real work

Retire stock. In the meantime, remove or replace, first:

- The container-terminal aerial and the container-ship still, wherever they stand in for offices, climate storage, logistics, or a “jobsite campus.”
- The motorcycle-workshop “generator” still.
- The retail reach-truck still as construction material handling.
- The mine/quarry hero as a commercial/government equipment picture.
- The Delawie and MIDAS stills (other companies’ marks).
- The pointing-supervisors still, or at least stop using it as “federal.”

Write the camp rule into `visual-identity/visual-style.md` once this proposal is approved (do not edit it in this PR). Commission documentary photography of Rental One’s actual equipment, modular offices, and crews on real commercial and government sites. Do not shoot, license, or publish workforce-housing or man-camp imagery.

### 2. Issue real logo masters — BRANDING

Request, from the original artwork, and add only those owner-provided files: a transparent white lockup, a transparent navy lockup (to replace `r1-logo-2.png`), one-color black and white, SVG/EPS/AI if they exist, and a standalone ONE-box mark at the sizes the guidelines already specify. Do not auto-trace or redraw. Fix the README line that still promises vectors in the folder. Keep the concept-stage coal/orange SVGs out of the system.

### 3. Embed Industry, or formally adopt the live Archivo condensed stand-in — BRANDING

Until a webfont license for Industry is on the site, display type is not the brand face. Either embed Industry (Adobe Fonts / a licensed fileset) or, if Hayden prefers not to license it for the web yet, document Archivo at 87% width as a temporary shipping substitute — the way Command documented Avenir Next — and keep Industry for print. Do not add a fourth family.

### 4. Close the written-vs-live token gaps — REFINEMENT

Promote or replace the live-only hexes (`steel-on-dark`, button hovers, form error). Cap live H1/H2 at the written 44/28 unless Hayden signs off on the larger sizes. Reconcile the 13 px button with the 18 px Industry floor. Drop the H3 mixed-case exception. Use Iron, not Gunmetal, for mute on light. Confirm print navy as PMS 282 C and correct the PMS 534 typo. Pull the live `:root` tokens and this file into one shared source once the website has a repo.

### 5. Put the website and the brand repo in a declared relationship — BRANDING

Decide where the rentaloneteam.com source lives, whether it should be added to this account, and who updates tokens when the guidelines change. Until then, treat this proposal plus `visual-identity/` as the brief, and the live CSS as the implementation that must be checked against it.

### 6. Align parent-company and public copy — REFINEMENT (copy), in the Cotton Co / HCC repos where noted, not on this `main`

Update Cotton Co’s portfolio line to **Project support** (per copy lead, pending Hayden confirmation). Do not visually mix Cotton Co black/gold or HCC marks into Rental One. On Rental One itself: use the tightened elevator; keep “Mobilize. Execute. Deliver.” unstacked; list Pete Bell as the public POC on public pages, quote forms, cards, and signatures (per copy lead, pending Hayden confirmation). Do not publish an unverified founding year as approved copy.

---

## Out of scope / do not do

- Do not redraw the logo or revive the concept-stage coal/orange artwork.
- Do not import High Cotton Capital, Cotton Co black/gold, Blackhorn, Founders Ranch, Roof Co, or Command colour, type, or components (no gold rules, no Rajdhani, no cream grounds, no soft card shadows).
- Do not publish imagery or copy that makes Rental One look like a workforce camp.
- Do not merge this proposal to `main`, deploy it, or launch Cursor cloud agents from it. Documentation only.
- Do not treat the unrelated Colleyville “Rental One” / Texas First Rentals company, or RentalShare, as this brand.

---

## Screenshot notes

- **Home, 1440 and 390:** navy header, white lockup, mono nav, chamfered orange “Request a Quote,” hero on a navy-scrimmed crane photograph, Industry-style caps (currently condensed Archivo), mist-colored lead, orange + ghost CTAs, plate row. Phone holds the type and the primary CTA; the lower plates sit under the fold.
- **About, Equipment, Services, Government, Quote:** the same chrome. Quote is a public form on Fog; it was not submitted.
