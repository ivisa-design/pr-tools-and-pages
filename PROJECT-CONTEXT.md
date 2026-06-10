# iVisa PR Tools & Pages — Project Context File
*Last updated: June 10, 2026 | For: Cowork (new session handoff)*

---

## What this project is

A set of standalone HTML pages built for iVisa to:
- Rank in top 10 for high-intent visa keywords
- Be cited by AI models (ChatGPT, Claude, Perplexity)
- Generate organic traffic (5,000+ sessions/month per page)
- Drive qualified leads (500+/month across all pages)
- Earn PR coverage in travel and immigration media

**Paula** is Brand & Creative Manager at iVisa. She reviews all work and pushes to GitHub herself from her Mac Terminal (the sandbox can't push due to filesystem permissions on the mounted drive).

---

## Infrastructure

| What | Detail |
|---|---|
| GitHub repo | `https://github.com/ivisa-design/pr-tools-and-pages` (branch: `main`) |
| Live URL | `https://pr-tools-and-pages.vercel.app` |
| Target domain | `umrah.ivisa.com` (CNAME pending — iVisa dev team adds `umrah → cname.vercel-dns.com`) |
| Deployment | Auto-deploys from GitHub main via Vercel |
| Local folder | `/Users/Paulaivisa/Desktop/PR tools and pages/` |
| `vercel.json` | Routes `/` and `/umrah-visa-guide` → `umrah-visa-guide.html` |

### How to push changes (Paula runs in Terminal)
```bash
cd "/Users/Paulaivisa/Desktop/PR tools and pages"
# If git is blocked by a lock file:
rm -f .git/index.lock
# Then:
git add -A && git commit -m "Your message" && git push origin main
```

> **Note on deployment:** If live site doesn't reflect changes, first confirm the commit is on GitHub, then hard-refresh browser (`Cmd+Shift+R`) or test in an incognito window. Vercel auto-deploys within ~30 seconds of a push.

---

## Current pages

### 1. `umrah-visa-guide.html` — LIVE ✓
**Full Umrah visa guide for the 2026–2027 season.**

**H1:** "Your complete Umrah Visa guide" + "2026–2027" (Anton font, uppercase, on next line)

**Page sections (in order):**
1. **Hero** — H1 (Manrope + Anton for date), subhead (16px, line-height 1.4, max-width 880px, manual `<br>` for balanced 2 lines), nationality checker (dropdown → JS result card), eligibility box (glass card, reduced vertical padding), 4 nav-link CTAs below checker
2. **What is Umrah** — Intro for new visitors
3. **Let iVisa handle it** — 3 circles with apply steps + animated floating photos (PHOTO A/B/C placeholders — need real images). Logo removed from this section.
4. **Start your Umrah journey** — Tab navigator: "Understand visa types" + "Am I eligible?" (cost tab removed). "Apply for my visa" CTA below section.
5. **Visa types — Compare your options** — Two stacked cards (Umrah + Tourist eVisa) on left + teal gradient image card (mosque icon) on right. No stats in image card.
6. **Documents & key dates** — Dark teal gradient background. Two glass boxes side by side: left = required documents bullet list, right = key dates mini-boxes + warning note. Image placeholder removed.
7. **Nationality guides** — Accordion per country: India, Pakistan, Bangladesh, Indonesia, Turkey, UK/EU/US, GCC. Collapsible category cards above (Umrah only / Either visa / Not Muslim).
8. **Cost calculator** — Interactive pricing tool (some fields still TBD pending 2026/2027 fees)
9. **Timeline / Key dates** — Split calendar + key dates vertical timeline
10. **Processing times** — Table by nationality
11. **Apply with iVisa** — CTA band ("Ready to apply?" + "Get your visa →" button). Logo removed from this section. Footer is black.
12. **FAQ** — Accordion (15 Q&As + JSON-LD schema)
13. **Footer** — Black background (`#000`). `ivisa-logo.png` (base64 embedded). Nav links + copyright.

**Tech stack:** Vanilla HTML/CSS/JS, no frameworks. IntersectionObserver for scroll animations. CSS keyframe animations on hero circles.

---

## Brand & design standards

| Token | Value |
|---|---|
| `--hero` | `#004752` (dark teal — headings, hero bg) |
| `--cta` | `#48d878` (green — CTA buttons) |
| `--warning` | `#fbab1e` (amber — warnings, deadlines) |
| `--footer` | `#000000` (black — footer background) |
| Font headings | Manrope 800 (Google Fonts) |
| Font body | Roboto 400/500 (Google Fonts) |
| Font H1 date | **Anton** (Google Fonts) — replaces Oswald. Used for "2026–2027" in H1 only. Impact-style, all-caps. |
| CTA button style | Manrope 800, 15px, `padding: 13px 28px`, `border-radius: 50px`, `color: #000`, `background: var(--cta)`. `min-width: 168px` on nav-link CTAs. |
| CTA button texts | "Get your visa →" / "Apply with iVisa" / "Apply for my visa" / "Apply now" / "Check now" |

### Logo files (CRITICAL — do not change)
| File | Use | Filter |
|---|---|---|
| `Assets/logo-positive.png` | Header (white bg) | None |
| `Assets/ ivisa-logo.png` *(note: leading space in filename)* | Footer (black bg) | None |

Both logos are **base64-embedded** directly in the HTML (not path-referenced). Width-based sizing: `120px` header, `160px` footer. Both are 2000×2000px square canvas — content occupies centre portion, so width-based sizing is critical.

**Tone:** Professional, approachable, transparent. Non-salesy. Standard case (not ALL CAPS). Contractions are fine. No fluff.

**Never say:** "100% approval guaranteed" — use "99% approval rate"

---

## Key content facts (Umrah 2026–2027 season)

These are verified and must stay consistent across ALL sections of the page:

| Fact | Value |
|---|---|
| Season opens | June 1, 2026 |
| Travel window (Umrah visa) | Jun 1, 2026 → Mar 23, 2027 |
| Application window (Umrah visa) | Jun 1, 2026 → Mar 9, 2027 |
| Last visa issuance | March 9, 2027 |
| Last entry date | March 23, 2027 |
| Mandatory departure deadline | **April 7, 2027 — Umrah visa holders ONLY** |
| Ramadan 2027 | ~Feb 17 – Mar 18, 2027 |
| Hajj blackout 2026 | ~March 15 – May 31, 2026 |
| Women's mahram policy | No mahram required for women 18+ since **2021** |
| Tourist eVisa Apr 7 rule | **Does NOT apply** — tourist eVisa holders have no seasonal departure deadline |
| Other cities on Umrah visa | **Allowed** after completing Umrah, via **Nusuk Masar** program |
| Umrah is for Muslims only | Yes — tourist eVisa holders (Muslim) can also enter Makkah outside Hajj blackout |
| Non-Muslims and Makkah | Non-Muslims **cannot** enter Makkah or Madinah at all — stated clearly on page |
| Health insurance | **Included** in Umrah visa fee (mandatory). Tourist eVisa does **not** include it. |

**Nationality-specific rules:**
- **India / Bangladesh / Pakistan:** Cannot self-apply on Nusuk — must use licensed travel agent (MOIA-registered). iVisa works with approved agents.
- **Pakistan / India:** VOA available with valid US, UK, or Schengen visa (note: airlines may still require pre-issued visa, boarding not guaranteed)
- **Bangladesh:** No VOA available
- **Indonesia:** Eligible for Saudi tourist eVisa directly (on eligible country list). Umrah visa goes through PPIU licensed operator.
- **Turkey / UK / EU / US / GCC / Malaysia:** Can apply directly on Nusuk

---

## Completed changes (history)

All commits are on `main`. Changes in chronological order:

**Early sessions:**
- Removed emoji flags from `<select>` dropdown (Windows doesn't render them) — kept emoji in JS result display only
- Moved "Visa types compare" section to below "Let iVisa handle it" section
- Removed Hajj blackout callout box
- Added CSS scroll animations (IntersectionObserver + keyframe `circleIn`, `floatBob1`, `ctaGlow`, `dotPulse`)
- Fixed logo background (transparent)
- Simplified CTA band to "Ready to apply?" + "Get your visa →"
- Fixed comparison table wording (Makkah availability, contradictions removed)
- Added Non-Muslim / Makkah section: hero checker caveat, non-Muslim FAQ, comparison table note
- Cleaned up FAQs (deleted redundant ones)
- Fixed "Can I visit other cities on Umrah visa?" — YES via Nusuk Masar
- Added non-Umrah tourist visa options to Pakistan, Bangladesh, India nationality cards
- Clarified Apr 7 departure deadline = Umrah visa only, not tourist eVisa
- Added travel window / application window boxes to timeline section
- Updated H1 to "Your complete Umrah Visa guide 2026–2027"

**Audit fixes (June 9, 2026):**
- JSON-LD Hajj blackout dates: "Apr 3–18" → "March 15–May 31, 2026"
- Women's mahram year: "2025" → "2021"
- JSON-LD + FAQ + comparison table: removed "restricts to Makkah/Madinah" language, added other cities via Nusuk Masar
- Footer nav: `#timeline` → `#processing-times`
- JS: `nationality-select` → `country-select`
- Calendar March 2027: added "Ramadan until ~18 Mar" note
- Ramadan dates aligned to Feb 17–Mar 18 across all sections

**Design & UX overhaul (June 10, 2026):**
- **Logos:** Switched to base64 embedding to avoid path issues. `logo-positive.png` in header (no filter), `ivisa-logo.png` in footer (no filter). Width-based sizing (120px/160px). Logo removed from "Let iVisa handle it" and apply sections.
- **Footer:** Background changed to black (`#000`). "Unlock the world" tagline placed below logo.
- **CTA pills:** All CTAs across entire page unified — Manrope 800, 15px, `padding: 13px 28px`, `border-radius: 50px`, `#000` text. Includes nav "Apply now", eligibility "Check now", hero nav-link buttons, CTA band, apply section. Fixed `.nav-links a.btn-cta` specificity override so "Apply now" inherits correct font weight.
- **Hero nav-link buttons:** Shortened labels: Requirements / Calculate cost / Check timelines / Visa types. `min-width: 168px` for equal widths.
- **H1 font:** "2026–2027" date changed from Oswald → **Anton** (Google Fonts). `margin-top: 0.2em` for spacing from line above.
- **H2 subhead:** `font-size: 16px`, `line-height: 1.4`, `max-width: 880px`. Manual `<br>` after "season." for balanced 2-line layout.
- **Eligibility checker box:** Vertical padding reduced from `40px` → `26px`. Title bottom margin `24px` → `18px`.
- **Comparison section (visa cards):**
  - Removed "Non-Muslims for general travel only" from Tourist eVisa badge → now just "All Muslims can apply"
  - Balanced both cards to 6 bullets of similar length
  - New layout: two stacked cards on left + tall featured image card on right (teal→green gradient, mosque emoji, Makkah label)
  - Stats (2M+/99%/24/7) removed from image card — clean gradient fill only
- **Documents & key dates section:**
  - Section background: dark teal gradient (`linear-gradient(135deg, #003d47, #005263, #004752)`)
  - Two glass boxes (glassmorphism: `backdrop-filter: blur(16px)`, `rgba(255,255,255,0.10)` bg)
  - Left glass box: required documents as bullet list with green checkmarks
  - Right glass box: 3 key date mini-boxes (glass style, Apr 7 in red-tinted glass) + amber-bordered warning note
  - Image placeholder A removed entirely
- **Navigator section ("Start your Umrah journey"):**
  - Removed "How much will it cost?" tab button and its panel
  - Added "Apply for my visa" CTA centered below the section (no divider line)
- **Required documents:** Previous icon-card grid replaced by clean bullet list inside glass box (see above)

---

## Pending / open tasks

| Priority | Task |
|---|---|
| 🔴 High | Add real photos to the 3 apply circles (PHOTO A/B/C placeholders in "Let iVisa handle it" section) |
| 🔴 High | Set up DNS: dev team adds CNAME `umrah → cname.vercel-dns.com` in iVisa's DNS settings |
| 🟡 Medium | Update all "TBD" cost/fee fields once 2026/2027 official fees are confirmed |
| 🟡 Medium | Replace IMAGE 1 placeholder in comparison/table section with real Grand Mosque photo (1200×500px WebP) |
| 🟡 Medium | Replace visa-card-image gradient placeholder with real Makkah photo (600×700px WebP) |
| 🟢 Low | Build `guides.ivisa.com` hub page (links to all PR tools) |
| 🟢 Low | Additional pages in the initiative (new individual briefs from Paula) |

---

## File structure

```
/Users/Paulaivisa/Desktop/PR tools and pages/
├── umrah-visa-guide.html     ← Main deliverable (~3,600+ lines)
├── vercel.json               ← URL routing config
├── README.md                 ← GitHub readme
├── Assets/
│   ├── logo-positive.png     ← Header logo (white bg, base64 embedded in HTML)
│   └──  ivisa-logo.png       ← Footer logo (dark bg, note: leading space in filename, base64 embedded)
└── .git/                     ← Git repo (remote: github.com/ivisa-design/pr-tools-and-pages)
```

---

## Project instructions (inherited by all pages)

From the project brief — all pages in this initiative must:
- Be standalone HTML files (no frameworks, no external deps except YouTube embeds)
- Be Vercel-ready (static, no SSR)
- Use iVisa brand colors and Manrope/Roboto fonts
- Include FAQ JSON-LD schema in `<head>` for LLM indexing
- Include Organization schema with `author: iVisa`
- Have minimum 5 internal links to ivisa.com pages
- Include `<!-- COOKIE CONSENT BANNER TO BE ADDED BY IVISA DEV TEAM -->` placeholder
- Be mobile-first responsive (380px / 768px / 1200px)
- Target Lighthouse 85+ desktop / 75+ mobile
- NOT use jQuery, React, Vue, or Angular

---

## iVisa key stats to use in copy

- 2,000+ visa applications processed monthly
- 99% approval rate
- Serving 100+ countries
- 24/7 customer support

---

## External references

- Official Umrah platform: https://www.nusuk.sa
- iVisa main site: https://ivisa.com
- iVisa Saudi Umrah visa page: https://ivisa.com/saudi-arabia-umrah-visa
- iVisa blog: https://ivisa.com/blog
