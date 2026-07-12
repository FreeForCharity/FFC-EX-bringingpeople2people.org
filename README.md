# FFC-EX-bringingpeople2people.org

Bringing People 2 People — FFC-supported charity. Static placeholder site (GitHub Pages).

Part of the FFC Wave-1 WordPress-to-Pages program ([FFC-Cloudflare-Automation#702](https://github.com/FreeForCharity/FFC-Cloudflare-Automation/issues/702)).

## Why a placeholder (no capture)

At migration time `bringingpeople2people.org` had **no website to capture**: the apex was a
Cloudflare-level **HTTP 301 redirect to the organization's Facebook page**
(`facebook.com/BRINGINGPEOPLE2PEOPL`), and `www.bringingpeople2people.org` did not resolve. There
was no HTML site, WordPress install, or origin content behind the domain.

Rather than clone a redirect, this repo ships a minimal, fully self-contained **"Website coming
soon"** placeholder (single `index.html`, all CSS inline, zero external assets) that:

- names the organization,
- links visitors to the org's active Facebook presence, and
- carries the FFC standard attribution footer.

## Hosting
- GitHub Pages, default URL: <https://freeforcharity.github.io/FFC-EX-bringingpeople2people.org/>
- Deploys from `.github/workflows/static.yml` on push to `main`. No custom domain / DNS at this stage.

## CI
- `static.yml` — deploys to Pages on push to `main`.
- `check-assets.yml` — fails if any asset loads from an external host (trivially green: no external assets).
- `linkcheck.yml` — lychee link check.

---
Supported by [Free For Charity](https://freeforcharity.org).
