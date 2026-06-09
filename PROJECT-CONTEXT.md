# iVisa PR Tools & Pages — Project Context File
*Last updated: June 9, 2026 | For: Cowork (new session handoff)*

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

---

## Current pages

### 1. `umrah-visa-guide.html` — LIVE ✓
**Full Umrah visa guide for the 2026–2027 season.**

**H1:** "Your complete Umrah Visa guide 2026–2027"

**Page sections (in order):**
1. **Hero** — H1, subhead, nationality checker (dropdown → JS result card)
2. **What is Umrah** — Intro for new visitors
3. **Let iVisa handle it** — 3 circles with apply steps + animated floating photos (PHOTO A/B/C placeholders — need real images)
4. **Visa types — Compare your options** — Umrah visa vs Tourist eVisa comparison table
5. **Eligibility checker** — Step-by-step quiz (5 questions)
6. **Nationality guides** — Accordion per country: India, Pakistan, Bangladesh, Indonesia, Turkey, UK/EU/US, GCC
7. **Cost calculator** — Interactive pricing tool (some fields still TBD pending 2026/2027 fees)
8. **Timeline / Key dates** — Split calendar + key dates vertical timeline
9. **Processing times** — Table by nationality
10. **Apply with iVisa** — CTA band ("Ready to apply?" + "Get your visa →" button)
11. **FAQ** — Accordion (15 Q&As + JSON-LD schema)
12. **Footer** — Nav links + copyright

**Tech stack:** Vanilla HTML/CSS/JS, no frameworks. IntersectionObserver for scroll animations. CSS keyframe animations on hero circles.

---

## Brand & design standards

| Token | Value |
|---|---|
| `--hero` | `#004752` (dark teal — headings, hero bg) |
| `--cta` | `#48d878` (green — CTA buttons) |
| `--warning` | `#fbab1e` (amber — warnings, deadlines) |
| Font headings | Manrope (Google Fonts) |
| Font body | Roboto (Google Fonts) |
| Logo | `/assets/ivisa-logo.svg` (transparent bg, in header) |
| CTA button text | "Get your visa →" or "Apply with iVisa" or "Start My Application" |

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
| Umrah is for Muslims only | Yes — tourist eVisa holders can enter Makkah outside Hajj blackout |
| Non-Muslims and Makkah | Non-Muslims cannot enter Makkah or Madinah at all — this must be stated clearly |

**Nationality-specific rules:**
- **India / Bangladesh / Pakistan:** Cannot self-apply on Nusuk — must use licensed travel agent (MOIA-registered). iVisa works with approved agents.
- **Pakistan / India:** VOA available with valid US, UK, or Schengen visa (note: airlines may still require pre-issued visa, boarding not guaranteed)
- **Bangladesh:** No VOA available
- **Indonesia:** Eligible for Saudi tourist eVisa directly (on eligible country list). Umrah visa goes through PPIU licensed operator.
- **Turkey / UK / EU / US / GCC / Malaysia:** Can apply directly on Nusuk

---

## Completed changes (history)

All commits are on `main`. Key changes made across sessions:

- Removed emoji flags from `<select>` dropdown (Windows doesn't render them) — kept emoji in JS result display only
- Moved "Visa types compare" section to below "Let iVisa handle it" section
- Removed Hajj blackout callout box
- Added CSS scroll animations (IntersectionObserver + keyframe `circleIn`, `floatBob1`, `ctaGlow`, `dotPulse`)
- Fixed logo background (transparent, uses `mix-blend-mode`)
- Simplified CTA band to just "Ready to apply?" + "Get your visa →"
- Fixed comparison table Umrah vs tourist eVisa Makkah availability wording (was contradictory)
- Added Non-Muslim / Makkah section: hero checker caveat, non-Muslim FAQ, comparison table note
- Cleaned up FAQs (deleted several redundant ones)
- Fixed "Can I visit other cities on Umrah visa?" — answer is YES via Nusuk Masar (not restricted)
- Added non-Umrah tourist visa options to Pakistan, Bangladesh, India nationality cards
- Clarified Apr 7 departure deadline = Umrah visa only, not tourist eVisa
- Added travel window / application window boxes to timeline section
- Updated H1 to "Your complete Umrah Visa guide 2026–2027"
- **Audit fixes (June 9, 2026):**
  - JSON-LD Hajj blackout dates: "Apr 3–18" → "March 15–May 31, 2026"
  - Women's mahram year: "2025" → "2021"
  - JSON-LD + FAQ + comparison table: removed "restricts to Makkah/Madinah" language, added other cities via Nusuk Masar
  - Footer nav: `#timeline` → `#processing-times`
  - JS: `nationality-select` → `country-select`
  - Calendar March 2027: added "Ramadan until ~18 Mar" note
  - Ramadan dates aligned to Feb 17–Mar 18 across all sections

---

## Pending / open tasks

| Priority | Task |
|---|---|
| 🔴 High | Add real photos to the 3 apply circles (PHOTO A/B/C placeholders in "Let iVisa handle it" section) |
| 🔴 High | Set up DNS: dev team adds CNAME `umrah → cname.vercel-dns.com` in iVisa's DNS settings |
| 🟡 Medium | Update all "TBD" cost/fee fields once 2026/2027 official fees are confirmed |
| 🟡 Medium | Replace IMAGE 1 and IMAGE 2 placeholder divs with real photos before full launch |
| 🟢 Low | Build `guides.ivisa.com` hub page (links to all PR tools) |
| 🟢 Low | Additional pages in the initiative (new individual briefs from Paula) |

---

## File structure

```
/Users/Paulaivisa/Desktop/PR tools and pages/
├── umrah-visa-guide.html     ← Main deliverable (3,400+ lines)
├── vercel.json               ← URL routing config
├── README.md                 ← GitHub readme
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
