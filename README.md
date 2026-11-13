# vanhold.com

The Vandercar website. It's a static site with no build step. GitHub Pages serves this repository as-is, and every push to `main` goes live within a minute or two.

## What's here

| Path | What it is |
|---|---|
| `index.html` | The whole one-page site (styles and scripts inline) |
| `img/` | Photos and the logo |
| `ada-policy/`, `privacy-policy/` | Policy pages, kept at the same addresses as the old site |
| `home/`, `our-company/`, `our-projects/`, `contact/` | Tiny pages that forward the old Legend WebWorks addresses to the right section. Old project pages open that project (for example `/#row-on-merchant`). |
| `404.html` | Shown for any address that doesn't exist; also forwards unknown old-site addresses |
| `page.css` | Shared styles for the policy and 404 pages |
| `CNAME` | Tells GitHub Pages the site's domain (`www.vanhold.com`). Don't delete it. |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are |
| `favicon.png`, `apple-touch-icon.png` | Browser tab and home-screen icons |

## Making changes

Edit the files, commit and push to `main`. To undo a bad change, revert the commit and push again.

To preview locally:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Contact form

Submissions go through [Web3Forms](https://web3forms.com), which emails them to info@vanhold.com. The form's access key is in `index.html`. It's meant to be public; it only lets people send messages to that inbox.

## GitHub Pages settings

Settings → Pages: deploy from the `main` branch, root folder. Custom domain `www.vanhold.com`, with **Enforce HTTPS** on.

## DNS (GoDaddy)

Only these records belong to the website:

| Type | Name | Value |
|---|---|---|
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| CNAME | `www` | `tylerfojtik.github.io` |

Every other record is for Microsoft 365 email, Teams or other services. Don't change those.
