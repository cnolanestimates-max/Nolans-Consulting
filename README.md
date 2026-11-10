# nolansconsulting.com

The website for Nolan's Consulting Solutions. Plain HTML, no build step. Any AI agent with access
to this repo can edit it. The rules for agents are in `AGENTS.md`.

## Put it live on Cloudflare Pages (one-time, about 15 minutes)

1. Make a free account at https://dash.cloudflare.com/sign-up (or log in).
2. Left menu: **Workers & Pages** > **Create** > **Pages** tab > **Connect to Git**.
3. Connect your GitHub account and pick the repo **Nolans-Consulting**.
4. Build settings: Framework preset **None**. Build command: leave **empty**.
   Build output directory: `/` (just a slash). Click **Save and Deploy**.
5. You'll get a free address like `nolans-consulting.pages.dev`. Open it and check the site.
6. Point your domain at it: in the Pages project go to **Custom domains** > **Set up a custom domain**
   and type `nolansconsulting.com`. Cloudflare walks you through it.
   - If your domain isn't on Cloudflare yet, it will ask you to add it. That means changing the
     "nameservers" where you bought the domain to the two Cloudflare gives you. Before you switch,
     write down any existing DNS records (especially email records) so nothing breaks.
   - Add `www.nolansconsulting.com` too, so both addresses work.

After this, every change pushed to the `main` branch goes live on its own.

## Edit it yourself

Open `index.html` on GitHub, click the pencil icon, change the text, click **Commit changes**.
It's live about a minute later.

## Optional: a nicer email address

Cloudflare Email Routing (free) can forward `hello@nolansconsulting.com` to your Gmail.
Dashboard > your domain > **Email** > **Email Routing**.

## Files

- `index.html` - the home page (all text, styles and scripts)
- `fonts/` - the self-hosted font (Bricolage Grotesque)
- `og-image.png` - preview image for LinkedIn/Facebook shares
- `404.html` - page shown for broken links
- `robots.txt`, `sitemap.xml` - help search engines find the site
- `_headers` - caching and security headers for Cloudflare Pages
