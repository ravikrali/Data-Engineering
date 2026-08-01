# Data Engineering, Rebuilt by AI — R2 Digital

A single-page progressive web app presenting R2 Digital's point of view on how AI is
transforming data engineering, and what an AI-powered DE platform looks like inside an
AI-first enterprise data architecture.

**Live:** https://ravikrali.github.io/Data-Engineering/

## Contents

| Section | What it covers |
| --- | --- |
| 01 The Signal | What analyst research and vendor releases published Feb–Jul 2026 actually changed |
| 02 Executive Summary | Six inversions that redefine the discipline |
| 03 Gaps | Nine structural gaps in traditional data engineering |
| 04 Competencies | The nine branches of DE — how they are implemented, tools used, where AI lands |
| 05 Project Archetype Map | Which project types use which DE concepts, stacks and AI leverage |
| 06 From the Field | Anonymised composite of a delivered enterprise data platform, and what it tells us |
| 07 Where AI Attaches | The leverage map — pain points, agents, and the trust plane underneath |
| 08 Target Architecture | AI-powered DE platform + its place in the AI-first enterprise data architecture |
| 09 Redesign | Nine core DE concepts, traditional vs. AI-native, with operational impact |
| 10 Roadmap | Phased migration, workstreams, KPIs and failure modes |
| — | Free-consultation CTA, related posts, external references |

## Files

```
index.html              the entire app (HTML, CSS, JS, inline SVG diagrams)
hero.svg                hero illustration — standalone, animated, self-contained
hero.png                raster hero (1280x1040) for LinkedIn and slide decks
manifest.webmanifest    PWA manifest
sw.js                   service worker — network-first pages, cache-first assets
R2-favicon.svg          R2 orbital logomark — browser tab / PWA icon
icon-192.png            PWA icon
icon-512.png            PWA icon / maskable
og.png                  1200x630 social preview image
.nojekyll               tells GitHub Pages to serve files as-is
```

No build step, no dependencies, no bundler. Web fonts are loaded from Google Fonts;
everything else is self-contained.

## Branding

Built on the **R2 Digital design system v1.0** (`R2 Digital/brand/` — `tokens.css`,
`R2-Design-System.md`). The tokens are inlined at the top of `index.html` rather than
imported, so the page stays a single self-contained file.

- **Identity** — the orbital logomark (white ring, orange core, orbiting satellites),
  inlined as SVG in the nav and footer; `R2-favicon.svg` for the tab.
- **Colour** — ink `#002346` / accent `#A64312` (`#C04F15` on dark), with a cool neutral
  scale. Orange is treated as a signal, not a background: it carries the AI/agent plane,
  CTAs, links and the roadmap's climax phase. Supporting hues (steel, gold, crimson,
  desaturated "legacy" slate, success green) are used only to separate meaning in
  diagrams. Accent fills always take white text; links step one along the ramp
  (`#8A3810` light, `#D9713F` dark) to hold contrast.
- **Type** — Space Grotesk (display) + Inter (body) + the system mono stack for labels,
  on the design system's fluid 1.20 scale. The top menu runs at `1.14rem` and the nav
  logomark at 51px, so the horizontal menu needs ~1380px; below that it collapses into
  the drawer, which carries all eleven sections in full.
- **Themes** — ships light and dark, driven by `data-theme` on `<html>`. Dark is the
  default marketing look; light is the reading look. The choice persists in
  `localStorage` under `r2-theme` and falls back to the OS preference.

## Local preview

```bash
python -m http.server 8080
```

Then open <http://localhost:8080>. A real HTTP origin is needed for the service worker —
opening `index.html` from the filesystem will work but PWA install will not.

## Contact form

The consultation form posts to [FormSubmit](https://formsubmit.co) at
`https://formsubmit.co/ajax/contact@r2dw.com`. FormSubmit activates per recipient address,
not per site — this address was already activated for the AI-Native MDM post, so the form
should work immediately. If a submission ever fails, check `contact@r2dw.com` for a
one-time activation email and click the link in it.

## Related

- [The Enterprise AI Strategy](https://ravikrali.github.io/blogAIStrategy)
- [The AI Investment Guide](https://ravikrali.github.io/blogAIInvestmentGuide)
- [The AI-Native MDM Thesis](https://ravikrali.github.io/MDM-AI-Strategy)

---

© 2026 R2 Digital LLC · Written by Ravi Rali · contact@r2dw.com
