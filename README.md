# Son of a Hitch — Website

Marketing site for **Son of a Hitch**, a brand of rugged, characterful hitch caps for any standard trailer hitch receiver. Live at **[sonofahitch.com](https://sonofahitch.com)**.

This is a single-page static site — no build step, no dependencies to install. Just open `index.html`.

## Files

| File | Purpose |
|------|---------|
| `index.html` | The entire website (HTML, CSS, and JS inlined in one file). |
| `og-image.png` | 1200×630 social share image (used by Open Graph / Twitter cards). |
| `robots.txt` | Tells search engines they may crawl the site; points to the sitemap. |
| `sitemap.xml` | Lists the site's pages for search engines. |
| `CNAME` | Tells GitHub Pages to serve the site at `sonofahitch.com`. |
| `.nojekyll` | Disables GitHub's Jekyll processing so all files are served as-is. |
| `.gitignore` | Keeps OS junk and local scratch files out of the repo. |

## Editing

Everything lives in `index.html`. The brand palette is defined as CSS variables at the top of the `<style>` block (`--char`, `--blaze`, `--olive`, etc.) — change those hex values to restyle the whole site. Design collections live in the `#caps` section; the FAQ is in `#faq`.

## Publishing (GitHub Pages)

1. Commit and push changes with **GitHub Desktop**.
2. In the GitHub repo: **Settings → Pages**, set **Source = Deploy from a branch**, branch **`main`**, folder **`/ (root)`**.
3. Under **Custom domain**, confirm `sonofahitch.com` (the `CNAME` file sets this automatically), and enable **Enforce HTTPS** once the certificate is issued.
4. Point the domain at GitHub in **GoDaddy DNS** (see `DEPLOY.md` for exact records).

After the initial setup, publishing an update is just: edit → commit → push. The live site refreshes within about a minute.

## To-do before launch

- Wire the email signup form to a real service (Mailchimp / ConvertKit / Klaviyo).
- Replace the placeholder cap art in the four collections with real designs.
- Confirm the Instagram / TikTok handles in the footer.
