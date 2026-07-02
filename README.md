# usableagain.com

Static public website for the iOS/iPadOS app **Usable Again**. Plain HTML + one shared CSS file — no framework, no build step, no JS.

## Pages

| URL | File |
|---|---|
| `/usable-again` | `usable-again/index.html` |
| `/usable-again/privacy` | `usable-again/privacy/index.html` |
| `/usable-again/terms` | `usable-again/terms/index.html` |
| `/usable-again/support` | `usable-again/support/index.html` |

The site root (`/`) redirects to `/usable-again/`.

## Before publishing

- Replace `[Effective Date]` in `usable-again/privacy/index.html` and `usable-again/terms/index.html` with the real effective date.

## Deploy (GitHub Pages + Cloudflare DNS)

1. Push this folder as the root of a GitHub repository.
2. Repo → Settings → Pages → Source: **Deploy from a branch**, branch `main`, folder `/ (root)`.
3. In the Pages settings, set the custom domain to `usableagain.com` (the `CNAME` file in this repo keeps it set).
4. In Cloudflare DNS for usableagain.com, add the four GitHub Pages `A` records for the apex (185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153) and a `www` CNAME to `<your-github-username>.github.io` if you want `www` too.
5. Wait for the Pages certificate, then enable **Enforce HTTPS**.

Preview locally with `python3 -m http.server` from this folder, then open `http://localhost:8000/usable-again/` (root-relative asset paths require a local server, not `file://`).

## App Store Connect URLs

- Privacy Policy URL: `https://usableagain.com/usable-again/privacy`
- Support URL: `https://usableagain.com/usable-again/support`
- Marketing URL (optional): `https://usableagain.com/usable-again`
