# Site Platform

Shared rendering and validation layer for Apricot Personal Labo product sites.

This directory is a migration-stage host. Product repositories keep their current `docs/` GitHub Pages sites unchanged while a parallel `site/` source tree is introduced.

## Responsibility boundary

- Product repository: product facts, manuals, privacy text, links, translations, screenshots/assets.
- Site platform: HTML layout, shared navigation/footer, design tokens, accessibility baseline, rendering/validation.
- Reusable workflow: preview build and artifact generation.
- Existing `docs/`: production source until an explicit cutover.

The initial contract uses `site/site.json` plus Markdown so the preview builder has no third-party runtime dependencies. A later renderer (for example Astro) may replace the implementation without changing the product-side ownership model.
