# Deploying sonofahitch.com (GitHub Pages + GoDaddy domain)

This site is hosted **free** on GitHub Pages, and your **GoDaddy** domain points at it.
After the one-time setup below, publishing is just: edit → commit → push in GitHub Desktop.

---

## Step 1 — Put this folder on GitHub (GitHub Desktop)

1. Open **GitHub Desktop** → **File → Add Local Repository** → choose this `sonofahitch-website` folder.
   (If it says the folder isn't a repository, click **"create a repository"** when prompted.)
2. Give it a name like `sonofahitch-website`, then **Create Repository**.
3. Click **Publish repository** (top right). **Uncheck "Keep this code private"** so the repo is Public — free GitHub Pages requires a public repo. (A marketing site's files are public once live anyway; just never commit passwords or API keys.)
4. Make your first commit: enter a summary like "Initial site", click **Commit to main**, then **Push origin**.

## Step 2 — Turn on GitHub Pages

1. On github.com, open your new repo → **Settings → Pages**.
2. **Source:** *Deploy from a branch*. **Branch:** `main`, folder `/ (root)`. Click **Save**.
3. Wait ~1 minute. A green banner shows the temporary URL: `https://<your-username>.github.io/sonofahitch-website/`.
4. Under **Custom domain**, it should already read **sonofahitch.com** (the `CNAME` file sets this). If not, type `sonofahitch.com` and **Save**.

## Step 3 — Point your GoDaddy domain at GitHub

In GoDaddy: **My Products → Domains → sonofahitch.com → DNS / Manage DNS**.

Add/replace these records:

**A records** (apex domain → GitHub's servers). Add all four, Name = `@`:

| Type | Name | Value            |
|------|------|------------------|
| A    | @    | 185.199.108.153  |
| A    | @    | 185.199.109.153  |
| A    | @    | 185.199.110.153  |
| A    | @    | 185.199.111.153  |

**CNAME record** (for the www version):

| Type  | Name | Value                     |
|-------|------|---------------------------|
| CNAME | www  | <your-username>.github.io |

Notes:
- Delete any existing parked/forwarding A record on `@` that GoDaddy added by default, and remove any conflicting `www` CNAME, so only the records above remain.
- Replace `<your-username>` with your actual GitHub username.
- DNS changes can take anywhere from a few minutes to a few hours to take effect.

## Step 4 — Lock in HTTPS

1. Back in **Settings → Pages**, wait for GitHub to finish issuing the SSL certificate (it checks your DNS automatically).
2. When available, tick **Enforce HTTPS**. Your site is now live at **https://sonofahitch.com** with a padlock.

---

## Publishing future updates

1. Edit `index.html` (or any file) locally.
2. In **GitHub Desktop**: write a short summary → **Commit to main** → **Push origin**.
3. The live site updates automatically in about a minute. That's it.

## Quick troubleshooting

- **"Domain's DNS record could not be retrieved"** in Pages settings → DNS hasn't propagated yet; wait and click **Check again**.
- **Site shows a 404** → confirm Pages Source is `main` / `/ (root)` and that `index.html` is in the repo root.
- **HTTPS checkbox greyed out** → give it more time after the DNS is verified; the certificate can take up to ~24h the first time.
- **Old content still showing** → hard-refresh (Cmd-Shift-R); GitHub's CDN can cache briefly.
