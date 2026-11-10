# Instructions for AI agents working on this site

This repo is the public website for **Nolan's Consulting Solutions** (https://nolansconsulting.com).
Any agent (Claude, Codex, Cursor, etc.) may edit it. Read this whole file before changing anything.

## What the business is

- Nolan's Consulting Solutions helps companies get noticed and described accurately in AI search
  (generative engine optimization, GEO). We test the questions a company's buyers ask ChatGPT and
  Google's AI, trace the sources behind the answers, improve the pages those answers rely on, and
  report monthly on changes and retest results.
- Buyers: companies of any industry that want more visibility in AI search.
- **This business has nothing to do with construction or estimating.** Never add construction
  imagery, wording, examples, audiences or links (including any link to an estimating-client page).
- Founder and service owner: Cheyenne Nolan.
- Plans (owner-set; never change without the owner's say-so):
  - **Focused GEO, US $3,000 per month:** one website and one priority offer; five buyer questions
    in two AI search experiences; month-one baseline and ranked fixes; up to three approved page
    updates per month; one revision round and documented retest; monthly evidence report and
    30-minute review.
  - **Full GEO, US $8,000 per month:** one website and up to three offers; fifteen buyer questions
    in three AI search experiences; broader offer and buying-decision coverage; two expert interviews
    per month; up to eight approved page updates per month; one revision round and documented retest;
    two working sessions, monthly evidence report and next priorities.
  - Prices are shown quietly at the bottom of each plan, not in headlines or buttons. The owner is
    fine keeping pricing in the background.
- Contact: nolansconsultingsolutions@gmail.com
- LinkedIn: https://www.linkedin.com/company/nolans-consulting-solutions/

If any of these facts change, update them **everywhere** they appear: visible page text, the
JSON-LD block in `<head>`, meta tags, `README.md`, and this file.

## How the site is built

- Plain static HTML. No framework, no build step, no package.json. Keep it that way unless the
  owner asks otherwise.
- `index.html` holds the whole home page: HTML, CSS (in `<style>`) and a one-line script.
- `fonts/bricolage-grotesque.woff2` is the only font (Bricolage Grotesque, SIL Open Font License).
- `og-image.png` is the 1200x630 image shown when the site is shared on LinkedIn, Facebook, etc.
- `404.html`, `robots.txt`, `sitemap.xml`, `_headers` (Cloudflare Pages headers).
- Hosting: Cloudflare Pages, connected to this GitHub repo. **Every push to `main` goes live
  automatically in about a minute.** Use a branch + pull request for big changes so the owner can
  preview them (Cloudflare gives each branch its own preview URL).

## Page structure (keep this order)

1. Hero: "What does AI search say about your business?" with the fictional tea-company sample finding.
2. Problems AI search causes for a business.
3. How the work runs each month (5 steps).
4. Services: Focused GEO and Full GEO.
5. Sample audit (fictional tea company, clearly labeled fictional).
6. Contact: "Which buyer question matters to you?" with the prefilled email draft.

## Design system (do not drift from it)

| Token | Value | Use |
|---|---|---|
| `--paper` | `#F5F6F8` | page background |
| `--card` | `#FFFFFF` | panels |
| `--ink` | `#15213B` | text, buttons, the dark sample-audit band |
| `--muted` | `#566073` | secondary text |
| `--line` | `#D6DAE1` | thin rules |
| `--mark` | `#F7E35A` | highlighter, used ONLY to mark the part of an AI answer that matters |
| `--cite` | `#2C52DB` | citation numbers and focus outlines |

- The visual idea is an AI answer with citations and a highlighter: where a business gets noticed,
  or where an answer falls short. Keep new sections in that language.
- Rounded pill buttons, 18px card corners, no gradients, no stock photos, no emoji, no ALL-CAPS labels.

## Writing rules

- Plain, specific language. Short sentences. No hype ("leverage", "unlock", "supercharge").
- **Never invent proof.** No fake testimonials, client logos, case studies, review stars or
  result percentages. Only publish results the owner has confirmed and has permission to share.
- **Never promise outcomes** (rankings, citations, leads, revenue). The site promises work,
  evidence and reporting.
- Fictional examples must be labeled as fictional.

## Before you finish any change

1. Serve locally: `python3 -m http.server 8000` then open http://localhost:8000
2. Check at desktop width and at 390px wide (phone). No sideways scrolling.
3. If you changed facts, check the JSON-LD block still matches the visible page.
4. Keep text contrast at WCAG AA or better.
5. Commit with a clear message describing what changed and why.
