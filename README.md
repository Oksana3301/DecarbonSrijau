# DecarbonHub

Unified product prototype for **DecarbonHub** — a carbon accounting & compliance platform for Indonesia. Exported from Claude Design and rebranded from the original "Srijau" working name to DecarbonHub.

## What's here

The **Unified** entry point composes three surfaces behind a floating product switcher:

| Surface | File | Description |
|---------|------|-------------|
| Landing | `DecarbonHub Landing.dc.html` | Marketing page — hero, "untuk siapa", cara kerja, kredibilitas, FAQ |
| Aplikasi | `DecarbonHub App.dc.html` | Product app — organisation onboarding & carbon calculation flow |
| Pemerintah & Donor | `DecarbonHub Dashboard Pemerintah.dc.html` | Government/donor aggregate reporting dashboard |
| **Unified** | `DecarbonHub Unified.dc.html` | Shell that imports the three above + the switcher |

`support.js` is the Claude Design runtime (`dc-runtime`) that renders the `.dc.html`
components. It loads React from a CDN and resolves `<dc-import>` by fetching sibling
`.dc.html` files, so the pages must be served over HTTP (not opened as `file://`).

## Preview locally

```bash
node server.js
# then open http://localhost:5599/  (defaults to the Unified view)
```

Any static file server rooted at this folder works equally well.

## Design tokens

- **Type:** Fraunces (display) + Plus Jakarta Sans (text)
- **Surface:** `#F3EFE3`  · **Ink:** `#17241A`  · **Accent yellow:** `#F4C518`  · **Link blue:** `#2C86D8`
- **Art:** Nusantara riso-print illustrations in `assets/`
