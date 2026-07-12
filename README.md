# atonughosh.com

Personal website of **Atonu Ghosh** — IoT, Edge & LPWAN systems researcher (PhD, IIT Kharagpur; Research Intern, Samsung R&D Institute India).

A single-page, fully static site — no build step, no framework. It deploys as-is to GitHub Pages.

## Structure

```
.
├── index.html                 # the whole page
├── assets/
│   ├── css/style.css          # design system + components + responsive + dark mode
│   ├── js/main.js             # theme toggle, mobile nav, scroll-spy, reveals, tabs
│   ├── fonts/                 # self-hosted woff2 (Space Grotesk, Inter, JetBrains Mono)
│   ├── img/                   # profile photo + PWA icons
│   └── og/atonu-cover.jpg     # social share card (1200×630)
├── Atonu_Ghosh_CV.pdf         # full CV (linked from the page)
├── Atonu_Ghosh_Resume.pdf     # 1-page résumé
├── favicon.svg / favicon.ico  # signal-node mark
├── apple-touch-icon.png
├── site.webmanifest           # PWA / installable
├── robots.txt · sitemap.xml
└── CNAME                       # atonughosh.com
```

## Design notes

- **Identity:** an "instrument / oscilloscope" system — cool paper (light) and deep teal-black (dark), a phosphor-teal accent, and a functional amber used only for status (granted / in production).
- **Type:** Space Grotesk (display) · Inter (body) · JetBrains Mono (labels & data). Fonts are self-hosted, so there's no third-party request and no render-blocking dependency.
- **Signature:** LoRa signal-propagation rings emanating from the profile "node" — a nod to long-range, low-power radio, which is the substance of the research.
- **Accessibility:** keyboard skip-link, visible focus rings, `prefers-reduced-motion` respected, semantic landmarks, ARIA on the nav, tabs, and toggle.

## Editing

Everything is plain HTML/CSS/JS.

- **Content** lives directly in `index.html` (sections are commented and labelled).
- **Colors, spacing, type** are CSS custom properties at the top of `assets/css/style.css` (`:root` for light, `[data-theme="dark"]` for dark).
- **Publications & patents** are simple `<li class="pub-item">` entries inside the tabbed panels — add or edit in place and update the tab counts.

## Deploy (GitHub Pages)

1. Push to the `atonughosh.github.io` repository (`main` branch).
2. Settings → Pages → Source: **Deploy from a branch** → `main` / root.
3. The `CNAME` file keeps the custom domain `atonughosh.com`.

No install, no CI, no build — GitHub Pages serves the files directly.
