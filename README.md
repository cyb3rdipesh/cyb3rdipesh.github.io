# dipeshtabdar.com.np — Portfolio Site

A static cybersecurity-themed portfolio, ready to deploy free on GitHub Pages
with the custom domain `dipeshtabdar.com.np`.

## 1. Edit your content

Placeholder text lives in `index.html` — search for "Placeholder" and swap in:

- Bio (About section)
- Real project links under `#projects`
- Real certifications under `#certifications`
- Social links (GitHub/LinkedIn/Twitter/TryHackMe/HackTheBox) in the hero and contact sections
- Your real email (replace `you@dipeshtabdar.com.np`)
- A real resume PDF at `assets/resume-placeholder.pdf` (or update the link/filename)

## 2. Push to GitHub

This folder is already a git repo with an initial commit. Create a new
**empty** repository on GitHub named exactly:

```
dipeshtabdar.github.io
```

(User-site repos on GitHub Pages must be named `<username>.github.io` — this
serves the site from the repo root at no cost, with no separate Pages config
needed for the default `github.io` subdomain.)

Do NOT initialize it with a README/license on GitHub's side (this repo
already has files). Then run:

```bash
git remote add origin https://github.com/dipeshtabdar/dipeshtabdar.github.io.git
git branch -M main
git push -u origin main
```

## 3. Enable GitHub Pages

Go to the repo → **Settings → Pages** → under "Build and deployment", set
**Source: Deploy from a branch**, branch `main`, folder `/ (root)`. Save.
Your site will be live within a minute or two at:

```
https://dipeshtabdar.github.io
```

## 4. Point your custom domain (dipeshtabdar.com.np)

The `CNAME` file in this repo already tells GitHub Pages to serve the site
for `dipeshtabdar.com.np`. You still need to point the domain's DNS at
GitHub. In your domain registrar's DNS panel, add:

**For the apex/root domain** (`dipeshtabdar.com.np`) — four A records:

| Type | Host | Value            |
|------|------|------------------|
| A    | @    | 185.199.108.153  |
| A    | @    | 185.199.109.153  |
| A    | @    | 185.199.110.153  |
| A    | @    | 185.199.111.153  |

**For `www`** (optional but recommended) — one CNAME record:

| Type  | Host | Value                     |
|-------|------|---------------------------|
| CNAME | www  | dipeshtabdar.github.io.   |

Then in the GitHub repo → **Settings → Pages → Custom domain**, enter
`dipeshtabdar.com.np` and save (GitHub will verify DNS — this can take a few
minutes up to ~24 hours to propagate). Once verified, tick **Enforce HTTPS**
so the site serves over `https://`.

> Note: `.com.np` domains are typically managed through Mercantile
> Communications or a reseller panel — look for a "DNS Management" or
> "Zone Editor" section for your domain to add the records above.

## 5. Local preview

Just open `index.html` in a browser, or serve it locally:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.
