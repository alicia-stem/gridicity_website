# Gridicity Website

Static HTML/CSS website for [gridicity.co.uk](https://gridicity.co.uk).

## Branches

| Branch | Purpose |
|---|---|
| `main` | Full product site — advisory services plus AI/software product offerings |
| `just_consulting` | Consulting-only variant — pure fleet electrification advisory, no product references |

## Stack

Single `index.html` with embedded CSS. No build step, no framework. Served via any static host.

**Fonts:** Poppins (headings) · DM Sans (body) · JetBrains Mono (CTAs, tags, numbers)  
**Palette:** `#f5fbf7` bg · `#0e1c17` foreground · `#116c4a` primary green · white cards

## Local development

```bash
python3 -m http.server 3456
# open http://localhost:3456
```

## Images

All images are in `images/`. Originals fetched from the live gridicity.co.uk WordPress media library.

## Related

- [Fleet TCO Calculator](https://xyy2secu.projects.saasbrella.co/) — linked from the consulting variant
- Design tokens documented in `design-system.md`
