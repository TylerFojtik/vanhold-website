# vanhold.com

The Vandercar website. It's a static site with no build step. Netlify serves this folder as-is, and every push to `main` goes live.

## What's here

| Path | What it is |
|---|---|
| `index.html` | The whole one-page site (styles and scripts inline) |
| `img/` | Photos and the logo |
| `ada-policy/`, `privacy-policy/` | Policy pages, kept at the same addresses as the old site |
| `404.html` | Shown for any address that doesn't exist |
| `page.css` | Shared styles for the policy and 404 pages |
| `_redirects` | Sends old Legend WebWorks addresses to sections of the new page |
| `favicon.png`, `apple-touch-icon.png` | Browser tab and home-screen icons |

## Making changes

Edit the files, commit and push to `main`. Netlify deploys in about a minute. To undo a bad change, open Netlify → Deploys, pick an earlier deploy and choose **Publish deploy**.

To preview locally:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000. The contact form only works on Netlify.

## Netlify settings

- **Build command:** none. **Publish directory:** repository root.
- **Forms:** form detection must be on. Submissions from the `contact` form email info@vanhold.com (Forms → Form notifications).
- **Domain:** primary domain `www.vanhold.com`; `vanhold.com` redirects to it.

## DNS (GoDaddy)

Only two records belong to the website:

| Type | Name | Value |
|---|---|---|
| A | `@` | Netlify's load balancer address (shown in Netlify's domain settings) |
| CNAME | `www` | `<site-name>.netlify.app` |

Every other record is for Microsoft 365 email, Teams or other services. Don't change those.
