# PR Tools and Pages

A collection of SEO-optimized landing pages and content tools for [iVisa](https://ivisa.com).

## Contents

### `umrah-visa-guide.html`

A fully self-contained HTML guide page targeting the 2026–2027 Umrah season.

**Live URL (when published):** `https://ivisa.com/saudi-arabia-umrah-visa/guide`

**What's inside:**

- Structured data (JSON-LD) — `Organization`, `BreadcrumbList`, `WebPage`, and `FAQPage` schemas for Google rich results
- 15-question FAQ covering eligibility, visa types, costs, processing times, and nationality-specific rules
- Comparison of the dedicated Umrah visa vs. Saudi tourist eVisa
- Nationality routing (US/UK/EU/GCC/Malaysia → Nusuk direct; India/Pakistan/Bangladesh → licensed agent via iVisa)
- Vaccine, mahram, and Hajj blackout season guidance
- iVisa CTA funnel throughout

**Tech:**

- Pure HTML/CSS — no build step, no dependencies
- Google Fonts: Manrope + Roboto
- Cookie consent banner placeholder (to be wired up by the dev team)
- Responsive, mobile-first layout

## Usage

Open any `.html` file directly in a browser for local preview, or deploy to the iVisa web server at the canonical URL defined in each file's JSON-LD.

## Notes

- Hajj blackout period 2026: approximately March 15 – May 31. Visa applications during this window are refused by Saudi authorities.
- Pages are updated seasonally. Check `dateModified` in the `WebPage` JSON-LD block for the last update date.
