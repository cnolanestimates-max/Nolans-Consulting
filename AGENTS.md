# Instructions for AI agents working on this site

This repo is the public website for **Nolan's Consulting** (https://nolansconsulting.com).
Any agent (Claude, Codex, Cursor, etc.) may edit it. Read this whole file before changing anything.

## What the business is

- Nolan's Consulting helps businesses get found and described accurately by ChatGPT, Google's AI
  and other AI assistants (generative engine optimization, GEO). We test the questions buyers ask,
  trace the sources behind the answers, improve the pages those answers rely on, and report every
  month on what changed.
- Name: always **Nolan's Consulting** in visible text (written with a curly apostrophe: Nolan’s).
  "Nolan's Consulting Solutions" appears only as `alternateName` in the JSON-LD, because the email
  address and LinkedIn page use it.
- Audience: US online stores (Shopify and similar) first, then online coaches, course sellers and
  other online-service businesses, then companies of any industry that want AI search visibility.
- **GEO only.** Never position the business around any other line of work the owner has had, never
  add trade-specific imagery, examples or audiences, and never link to old client portals or
  account pages.
- Founder: Cheyenne Nolan.
- Contact: nolansconsultingsolutions@gmail.com
- LinkedIn: https://www.linkedin.com/company/nolans-consulting-solutions/

### Offers (owner-set; never change without the owner's say-so)

- **ChatGPT Launch, US $500 one-time.** Delivered within 7 business days after the client completes
  verification. Includes: ChatGPT visibility audit; business profile claim and verification help in
  ChatGPT's Business Hub (the client completes verification; we guide them); business agent build
  if eligible; AI-readability check; launch report. **Upgrade credit:** the full $500 comes off the
  first month of Focused GEO if the client upgrades within 30 days. Outreach emails link to
  `/#chatgpt-launch`, so keep that anchor.
- **Focused GEO, US $3,000 per month:** one website and one priority offer; five buyer questions
  in two AI search experiences; month-one baseline and ranked fixes; up to three approved page
  updates per month; one revision round and documented retest; monthly evidence report and
  30-minute review.
- **Full GEO, US $8,000 per month:** one website and up to three offers; fifteen buyer questions
  in three AI search experiences; broader offer and buying-decision coverage; two expert interviews
  per month; up to eight approved page updates per month; one revision round and documented retest;
  two working sessions, monthly evidence report and next priorities.
- ChatGPT Launch has two PayPal checkout links on the site, both pointing to
  `https://www.paypal.com/ncp/payment/HYAVQ22SXRCX8` ($500 USD, one-time, quantity one).
  PayPal's shared legal seller is Cheyenne Nolan. Do not replace either account email.
- Focused GEO and Full GEO still use `#contact`: agree scope, renewal and cancellation terms
  in writing, then arrange payment through PayPal. Do not turn these into public automatic
  subscriptions without agreed terms. Keep the $500 upgrade credit when arranging the first bill.

### Facts about Businesses in ChatGPT (checked 2026-11-11)

- OpenAI introduced "Businesses in ChatGPT" in beta in November 2026. Businesses claim a profile in
  the Business Hub; once verified they can update details and see insights on mentions, website
  clicks and common topics.
- Business agents: only for eligible US ecommerce and online-service businesses. They answer
  questions and link to the business's site; they can't take payments or bookings.
- Nolan's is independent and not affiliated with OpenAI. Keep the disclaimer in the ChatGPT Launch
  section and the footer. Re-check these facts before adding new claims about the feature.

If any of these facts change, update them **everywhere** they appear: visible page text, the
JSON-LD block in `<head>` (business, offers and FAQ), meta tags, `llms.txt`, `README.md` and this
file.

## How the site is built

- Plain static HTML. No framework, no build step, no package.json. Keep it that way unless the
  owner asks otherwise.
- `index.html` holds the whole home page: HTML, CSS (in `<style>`) and a small inline script
  (header state, mobile menu, scroll reveal, plan preselect, email-draft form, copy button).
- Fonts are self-hosted in `fonts/` (SIL Open Font License, licenses alongside):
  `newsreader-var.woff2` and `newsreader-italic-var.woff2` (headings) and `inter-var.woff2` (text).
  They are subset to Latin, so a character outside basic Latin and common punctuation falls back
  to the system font.
- Logo: an inline SVG symbol (`#logo-mark`) plus the wordmark text. Same mark in `favicon.svg`,
  `favicon.ico`, `apple-touch-icon.png` and `logo.png` (512px, used in JSON-LD).
- `og-image.png` is the 1200x630 image shown when the site is shared.
- `llms.txt` is a plain summary of the business for AI crawlers. Keep it in sync with the page.
- `404.html`, `robots.txt`, `sitemap.xml`, `_headers` (Cloudflare Pages caching, security headers
  and a Content-Security-Policy; inline scripts and styles are allowed, outside hosts are not,
  except Cloudflare Web Analytics).
- Hosting: Cloudflare Pages connected to this GitHub repo (see `README.md`). Once connected, every
  push to `main` goes live in about a minute. Use a branch and pull request for big changes so the
  owner can preview them.

## Page structure (keep this order)

1. Header: logo, links (ChatGPT Launch, Services, Approach, Pricing, FAQ), "Start a project".
2. Hero: "What does AI tell your buyers about you?" with the audited AI answer illustration
   (fictional Larkfield Tea Co., labeled fictional).
3. Strip of AI assistants we test.
4. `#chatgpt-launch` (dark): the $500 offer, five included parts, who it's for, limits, disclaimer.
5. `#why`: three ways AI answers hurt a business.
6. `#services`: Audit, Fix, Measure.
7. `#approach`: the five monthly steps and the sign-off note.
8. `#sample-report`: one finding for the fictional tea company.
9. `#pricing`: ChatGPT Launch, Focused GEO (featured), Full GEO, fine print.
10. `#principles`: four principles and the founder card.
11. `#faq`: questions mirrored in the FAQPage JSON-LD (keep the two in sync).
12. `#contact` (dark): next steps and the email-draft form, then the footer.

## Design system (do not drift from it)

| Token | Value | Use |
|---|---|---|
| `--paper` | `#F7F5F0` | page background (warm ivory) |
| `--paper-2` | `#EFEBE3` | alternate section background |
| `--card` | `#FFFFFF` | cards and panels |
| `--ink` | `#0C1A2E` | headings, primary buttons |
| `--text` | `#2E3A4D` | body text |
| `--muted` | `#5A6577` | secondary text (AA on paper and white) |
| `--line` / `--line-strong` | `#E2DDD3` / `#CFC8BB` | rules and borders |
| `--night` | `#0A1628` | dark sections (ChatGPT Launch, contact, footer, featured plan) |
| `--accent` | `#2347C8` | eyebrows, italic heading emphasis, links, focus rings |
| `--accent-night` | `#9CB1FF` | accent on dark sections |
| ok / warn / bad | `#17795A` / `#9A5B0B` / `#B4321F` | audit statuses only |

- Type: Newsreader for headings (weight 400 to 500, an italic accent phrase in most section titles),
  Inter for everything else. Small uppercase eyebrow labels with a short rule before them.
- The visual idea is an audited AI answer: highlights, numbered findings, sources, evidence.
  Keep new sections in that language. Illustrations are built in HTML/CSS, not images.
- Pill buttons, 16 to 22px card corners, soft shadows, no stock photos, no emoji, no client logos.
- Motion is subtle (fade-up on scroll, hero highlight sweep) and switched off for
  `prefers-reduced-motion`.

## Writing rules

- Plain, specific language. Short sentences. No hype ("leverage", "unlock", "supercharge").
- **Never invent proof.** No fake testimonials, client logos, case studies, review stars or
  result percentages. Only publish results the owner has confirmed and has permission to share.
- **Never promise outcomes** (rankings, citations, leads, traffic, revenue). The site promises work,
  evidence and reporting.
- Fictional examples must be labeled as fictional.

## Before you finish any change

1. Serve locally: `python3 -m http.server 8000` then open http://localhost:8000 (root-relative
   paths like `/fonts/...` need a server, not a file:// URL).
2. Check at desktop width and at 390px wide (phone). No sideways scrolling. Open the mobile menu.
3. Open http://localhost:8000/#chatgpt-launch directly and check it lands on the offer.
4. If you changed facts, check the JSON-LD and `llms.txt` still match the visible page.
5. Keep text contrast at WCAG AA or better.
6. Commit with a clear message describing what changed and why.
