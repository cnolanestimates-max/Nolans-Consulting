# Instructions for AI agents working on this site

This repo is the public website for **Nolan's Consulting Solutions** (https://nolansconsulting.com).
Any agent (Claude, Codex, Cursor, etc.) may edit it. Read this whole file before changing anything.

## What the business is

- Nolan's Consulting Solutions checks what AI search tools (ChatGPT, Google AI Mode) say about
  construction companies, marks up what is wrong or missing, and fixes it on the company's website.
- Target buyers: subcontractors and builders first; web/SEO agencies second (white-label).
- Founder: Cheyenne Nolan, 12+ years in construction administration and estimating, Texas.
- Main offer: **AI Search Check, $750 one time** (introductory price). Monthly work is quoted only
  after a check, based on what's left.
- Contact: nolansconsultingsolutions@gmail.com
- LinkedIn: https://www.linkedin.com/company/nolans-consulting-solutions/

If any of these facts change, update them **everywhere** they appear: visible page text, the
JSON-LD block in `<head>`, meta tags, `README.md`, and this file.

## How the site is built

- Plain static HTML. No framework, no build step, no package.json. Keep it that way unless the
  owner asks otherwise.
- `index.html` holds the whole home page: HTML, CSS (in `<style>`) and JS (in `<script>`).
- `fonts/` holds self-hosted fonts (Archivo variable, Architects Daughter; both SIL Open Font License).
- `og-image.png` is the 1200x630 image shown when the site is shared on LinkedIn, Facebook, etc.
- `404.html`, `robots.txt`, `sitemap.xml`, `_headers` (Cloudflare Pages headers).
- Hosting: Cloudflare Pages, connected to this GitHub repo. **Every push to `main` goes live
  automatically in about a minute.** Use a branch + pull request for big changes so the owner can
  preview them (Cloudflare gives each branch its own preview URL).

## Design system (do not drift from it)

| Token | Value | Use |
|---|---|---|
| `--vellum` | `#F3F4F1` | page background (drafting film) |
| `--sheet` | `#FFFFFF` | panels and tables |
| `--graphite` | `#1D2430` | text, buttons, heavy rules |
| `--pencil` | `#5F6873` | secondary text |
| `--rule` | `#C9CDC8` | thin lines |
| `--redline` | `#C81F27` | ONLY for corrections/markup (redline clouds, notes, the zeros in the test log) |

- Type: Archivo (headlines condensed, `font-stretch` ~72-80%, weight 800-850; body normal width).
  Architects Daughter is used **only** for handwritten redline notes.
- The visual idea is a construction drawing being redlined: revision clouds, delta triangles,
  a punch list, a drawing title block as the footer. Keep new sections in that language.
- Do not add: stock photos, gradients, emoji, generic SaaS card grids, ALL-CAPS labels,
  testimonial carousels.

## Writing rules

- Plain, specific language a contractor would use. Short sentences. No marketing jargon
  ("leverage", "unlock", "supercharge", "cutting-edge").
- Say "AI search" or name the tool. Use "GEO" sparingly; most buyers don't know the term.
- **Never invent proof.** No fake testimonials, client logos, case studies, review stars,
  "trusted by" claims or result percentages. Only publish results the owner has confirmed
  and has permission to share.
- **Never promise outcomes** (rankings, mentions, leads). The site promises work and reporting.
- Examples that aren't real must be labeled as examples (the hero uses "Your Company").

## Before you finish any change

1. Serve locally: `python3 -m http.server 8000` then open http://localhost:8000
2. Check at desktop width and at 390px wide (phone). No sideways scrolling.
3. Check the redline clouds in the hero still sit around the right sentences.
4. If you changed facts, check the JSON-LD block still matches the visible page.
5. Keep text contrast at WCAG AA or better.
6. Commit with a clear message describing what changed and why.

## Planned work (ask the owner before starting)

- Post the re-test results of the ten self-check questions in the "We checked ourselves first"
  section once they're run (keep misses as well as wins).
- Trade-specific pages (for example `/masonry/`, `/concrete/`) only once there is real content for them.
- A contact form (e.g. Cloudflare Pages Function or Formspree) if email-only becomes a problem.
