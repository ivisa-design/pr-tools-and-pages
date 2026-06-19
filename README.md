# iVisa Umrah Guide

A standalone SEO and PR content page for [iVisa](https://ivisa.com) targeting the 2026–2027 Umrah season.

## Contents

### `umrah-visa-guide.html`

A fully self-contained HTML guide page covering Umrah visa eligibility, types, costs, and nationality-specific rules.

**Live URL:** `https://umrah.ivisa.com`
**Preview URL:** `https://umrah-ivisa.vercel.app`
**Deployment:** Auto-deploys from `main` via Vercel (project: `umrah-guide`)

**What's inside:**

- Structured data (JSON-LD) — `Organization`, `BreadcrumbList`, `WebPage`, and `FAQPage` schemas for Google rich results and AI citation
- Nationality eligibility checker (dropdown → JS result card)
- Comparison of the Umrah eVisa vs. Saudi tourist eVisa
- Nationality-specific accordion guides (India, Pakistan, Bangladesh, Indonesia, Turkey, UK, EU, GCC, and more)
- Processing times, costs, key dates, and a 12-month travel calendar
- 19-question FAQ
- Downloadable print guide (`umrah-visa-guide-print.html`)
- iVisa CTA funnel with UTMs (pending implementation)

**Tech:**

- Pure HTML/CSS/JS — no build step, no dependencies
- Google Fonts: Manrope + Roboto
- All images base64-embedded (except hero, served from `Assets/`)
- Cookie consent banner placeholder (to be wired up by dev team)
- Responsive, mobile-first layout (380px / 768px / 1200px)

### `umrah-visa-guide-print.html`

Clean PDF/print version of the full guide. Opened via the "Download full guide" button in the main guide.

## Deployment

- **Vercel project:** `umrah-guide` (`vercel.com/ivisa-design/umrah-guide`)
- **GitHub repo:** `ivisa-design/pr-tools-and-pages`
- **DNS:** CNAME `umrah → cname.vercel-dns.com` on Cloudflare (pending — iVisa dev team)

## Notes

- Hajj blackout 2026: approximately March 15 – May 31. No Umrah visas issued during this window.
- Date stamp must be updated on every commit. See `PROJECT-CONTEXT.md` for exact locations.
- All factual claims must be sourced. See content integrity rules in `PROJECT-CONTEXT.md`.
