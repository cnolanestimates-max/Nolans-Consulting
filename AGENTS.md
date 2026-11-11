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
  (header state, mobile menu, scroll reveal, the hero answer-audit animation, the "How it works"
  step cycle, plan preselect, email-draft form, copy button).
- Fonts are self-hosted in `fonts/` (SIL Open Font License, licenses alongside):
  `geist-var.woff2` (all text) and `geist-mono-var.woff2` (labels, data and the console).
  `inter-var.woff2` is used only by the pages in `options/`. Fonts are subset to Latin, so a
  character outside basic Latin and common punctuation falls back to the system font.
- Logo: an inline SVG symbol (`#logo-mark`) plus the wordmark text. Same mark in `favicon.svg`,
  `favicon.ico`, `apple-touch-icon.png` and `logo.png` (512px, used in JSON-LD).
- `og-image.png` is the 1200x630 image shown when the site is shared.
- `index.html` is wrapped in `<!--email_off-->` and `<!--/email_off-->` comments. Cloudflare's
  Email Address Obfuscation is on for the domain and would otherwise swap the contact email for
  "[email protected]", which AI crawlers and visitors without JavaScript can't read. Keep both
  comments, and add them to any new page that shows the email address.
- `options/` holds spare home page designs the owner may switch to: `options/a/` ("The Editor",
  newspaper style) and `options/c/` ("The Launch", product-page style), plus a comparison page at
  `options/index.html` with screenshots in `options/shots/` and their fonts in `options/fonts/`.
  They are `noindex` and blocked in `robots.txt`. When offers or facts change, update them there
  too. The live design (option B, "The Signal") is `index.html`.
- `llms.txt` is a plain summary of the business for AI crawlers. Keep it in sync with the page.
- `404.html`, `robots.txt`, `sitemap.xml`, `_headers` (Cloudflare Pages caching, security headers
  and a Content-Security-Policy; inline scripts and styles are allowed, outside hosts are not,
  except Cloudflare Web Analytics).
- Hosting: Cloudflare Pages connected to this GitHub repo (see `README.md`). Once connected, every
  push to `main` goes live in about a minute. Use a branch and pull request for big changes so the
  owner can preview them.

## Page structure (keep this order)

1. Header: logo, links (ChatGPT Launch, How it works, Evidence, Pricing, FAQ), "Start a project",
   and a mobile menu.
2. Hero: "Your buyers ask AI. We measure the answer." with the answer-audit console, which types
   out a fictional AI answer (Larkfield Tea Co., labeled fictional) and then marks each finding.
   Quick facts below the buttons: $500 setup, about a week, monthly from $3k.
3. `#chatgpt-launch`: the $500 offer, what's included, who it's for, limits, disclaimer.
4. `#why`: three ways AI answers hurt a business.
5. `#loop` ("How it works"): the five monthly steps with the cycle diagram. Also carries the old
   `#services` and `#approach` anchors so older links still land here.
6. `#evidence`: sample monthly evidence log for the fictional tea company. Also carries the old
   `#sample-report` anchor.
7. `#pricing`: ChatGPT Launch, Focused GEO (featured), Full GEO, fine print.
8. `#principles`: working principles and the founder note.
9. `#faq`: questions mirrored in the FAQPage JSON-LD (keep the two in sync).
10. `#contact`: next steps and the email-draft form, then the footer.

## Design system (do not drift from it)

Option B, "The Signal": a dark, precise, software-product look. Chosen by the owner on 2026-11-11.

| Token | Value | Use |
|---|---|---|
| `--bg` / `--bg-2` | `#0A0B0D` / `#0E1013` | page background / inset panels |
| `--panel` / `--panel-2` | `#13161A` / `#191D22` | cards, console, active tabs |
| `--line` / `--line-2` | `#24282F` / `#323842` | rules, borders, hero grid |
| headings | `#FFFFFF` | h1 to h4 |
| `--text` | `#E8EAED` | main text |
| `--soft` | `#C5C9CF` | secondary text |
| `--muted` | `#9AA0A9` | labels and fine print |
| `--dim` | `#7D848E` | smallest labels only (lowest color that still passes AA on `--bg`) |
| `--accent` | `#D6F25A` | lime: second half of headings, primary buttons, focus rings, logo |
| `--accent-ink` | `#0A0B0D` | text on lime |
| ok / warn / bad | `#4FD69C` / `#FFB547` / `#FF6F6F` | audit statuses only |

- Type: Geist for text and headings (headings 600 to 620 weight, tight letter-spacing, the second
  half of most headings in lime or a dimmer grey). Geist Mono for labels, section numbers (01, 02),
  tags, data and the console. Section labels are a mono number plus a short uppercase tag.
- The visual idea is measurement: an AI answer being audited, evidence logs, numbered steps.
  Keep new sections in that language. Illustrations are built in HTML/CSS/SVG, not images.
- 8px button corners, 12 to 14px card corners, hairline borders instead of heavy shadows, a faint
  grid behind the hero, no stock photos, no emoji, no client logos.
- Motion: hero console typing and audit, step cycle in "How it works", fade-up on scroll. All of it
  is switched off for `prefers-reduced-motion`, which shows the finished state.
- Logo: the same mark as before, in lime with dark bars (`#logo-mark` in `index.html`,
  `favicon.svg`, `favicon.ico`, `apple-touch-icon.png`, `logo.png`).

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
