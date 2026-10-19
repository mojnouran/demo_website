# AIXAutonomy website

A static site. No build step, no framework. Files:

- `index.html` – the whole page (styles and script inside)
- `favicon.svg` – browser tab icon

## Change the placeholders

Find and replace in `index.html`:

| Find | Replace with |
|---|---|
| `rpirayeshs@gmail.com` | change when the company email exists |

## Deploy on Vercel

Option A, GitHub (easiest to update later)
1. Create a GitHub repo and upload `index.html` and `favicon.svg`.
2. On vercel.com, click Add New > Project, pick the repo, keep "Other" as the framework, click Deploy.
3. Every push to the repo redeploys the site.

Option B, command line
1. Install Node.js, then in this folder run `npx vercel`.
2. Answer the prompts. Run `npx vercel --prod` for the live URL.

Note: Vercel's free Hobby plan is for personal, non-commercial use. A company site should be on Pro, or use another host such as Cloudflare Pages or Netlify.

## Add your domain

In the Vercel project, open Settings > Domains, add your domain, and follow the DNS records it shows you.

## Company email

Vercel hosts the website only. Email needs a separate provider, connected through MX records on the same domain.

- Google Workspace Business Starter: about $7 per user per month (annual) or $8.40 monthly.
- Zoho Mail Forever Free: up to 5 users on one domain, 5 GB each, webmail and phone app only (no IMAP/POP).
- Cloudflare Email Routing: free forwarding from you@yourdomain to your Gmail. Receiving only, sending from the custom address needs extra setup.

Each provider gives you MX and TXT (SPF, DKIM) records. Add them where your domain's DNS lives (your registrar, or Vercel if you moved DNS there).
