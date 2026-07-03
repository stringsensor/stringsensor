# String Sense — site

Single-page site, no build step. `index.html` + `assets/logo.png` + `CNAME`.

## Deploy to GitHub Pages

1. Create a repo (e.g. `reptide/stringsense-site`), push these three files to the root of the `main` branch.
2. Repo → **Settings → Pages** → Source: `Deploy from a branch` → Branch: `main` / `root`.
3. Wait a minute, then check `https://reptide.github.io/stringsense-site/` loads.

## Point stringsense.kr at it (GoDaddy DNS)

In GoDaddy → your domain → **DNS**:

| Type | Name | Value |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | reptide.github.io |

These four A records are GitHub Pages' fixed IPs — same for every custom domain.

Back in GitHub → **Settings → Pages**, set the custom domain to `stringsense.kr` (this writes the `CNAME` file for you if you didn't already commit one — the one included here already has it) and once DNS propagates, tick **Enforce HTTPS**.

DNS propagation is usually 15 min–a few hours, occasionally up to 24-48h.

## Before you go live

- The waitlist form currently posts to a placeholder (`formsubmit.co/your-email@example.com`). Swap in your real address — [formsubmit.co](https://formsubmit.co) needs no backend, just replace the email and confirm via the activation email it sends on first submit. Or swap the whole `<form>` for a `mailto:` link if you'd rather skip that.
- `hello@stringsense.kr` and the GitHub link in the footer are placeholders — update to whatever you're actually using.
