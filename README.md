# Gridicity Website

Static HTML/CSS website for [gridicity.co.uk](https://gridicity.co.uk).

**Deployed via:** Cloudflare Pages (connected to this repo; pushes to `main` auto-deploy).

## What this site is

An independent advisory for fleet electrification and EV charging: data-driven,
AI-assisted analysis and practical recommendations. It does **not** sell hardware,
software, or energy contracts, and there is no product/platform to integrate. The
page positions the business as a small, independent consultancy, not a SaaS product.

## Branches

| Branch | Status | Purpose |
|---|---|---|
| `main` | **Live** | Current site. Independent fleet electrification advisory. This is what Cloudflare Pages deploys. |
| `just_consulting` | Superseded | Earlier consulting-only draft (six services, TCO mockup, etc.). Kept for reference; **not** deployed. `main` replaces it. |

> The consulting rewrite lives on **`main`**. Earlier in development an advisory
> variant was drafted on `just_consulting`, but the finished, deployed version is
> `main` — edit there.

## Page structure (`index.html`)

Hero → ScottishPower testimonial → Services (Electrification planning · Infrastructure
and charging strategy · Charging analysis and optimisation) → free TCO Calculator
feature → How it works (4 steps) → Why Gridicity → About (founder) → Contact → Footer.

## Stack

Single `index.html` with embedded CSS. No build step, no framework. Served via any static host.

**Fonts:** Poppins (headings) · DM Sans (body) · JetBrains Mono (CTAs, tags, numbers)  
**Palette:** `#f5fbf7` bg · `#0e1c17` foreground · `#116c4a` primary green · white cards

## Local development

```bash
python3 -m http.server 3456
# open http://localhost:3456
```

## Deployment

Deployed with **Cloudflare Pages**, connected to this GitHub repo. It is a plain
static site, so the Cloudflare Pages project settings are:

- **Framework preset:** None
- **Build command:** *(none)*
- **Build output directory:** `/` (repo root)

Any push to `main` triggers an automatic Cloudflare deploy; Cloudflare serves the
files as-is with no build step. GitHub Pages is no longer used.

The `.nojekyll` file is a leftover from the previous GitHub Pages setup. It has no
effect on Cloudflare and can be removed if desired.

## Images

Most images are in `images/`, originally fetched from the live gridicity.co.uk
WordPress media library. Two were added for this site:

- `images/tco-calculator.png` — screenshot of the [Fleet TCO Calculator](https://xyy2secu.projects.saasbrella.co/), captured with headless Chrome. Static snapshot; re-capture if the tool's UI changes.
- `images/Scottish_Power_logo.svg` — ScottishPower logo used in the testimonial.

## Related

- [Fleet TCO Calculator](https://xyy2secu.projects.saasbrella.co/) — free EV-vs-fuel cost tool, linked from the site
- Design tokens documented in `design-system.md`
