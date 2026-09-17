<div align="center">

# Rhythmix

**Music with a new scale — a vibrant, dependency-free landing page for a music streaming service.**

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![Dependencies](https://img.shields.io/badge/dependencies-none-brightgreen?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square)

</div>

## Overview

Rhythmix is a lightweight, single-page marketing site for a music streaming
product. A full-bleed backdrop slowly cycles through hues behind frosted-glass
panels, while a warm orange-to-purple gradient drives the brand accent.

The entire site is one HTML file, one stylesheet, and a handful of images —
no frameworks, no build step, no third-party requests.

## Features

- **Zero dependencies** — inline SVG icons instead of icon CDN fonts; works fully offline
- **Responsive** — fluid gutters and type scales from phones to wide desktops
- **Accessible** — semantic landmarks, skip link, visible focus states, `prefers-reduced-motion` support
- **Fast** — a single stylesheet, one small SVG favicon, no render-blocking third-party CSS
- **Themeable** — all colors, fonts, and layout metrics live in CSS custom properties
- **Production-safe asset paths** — lowercase, case-exact references that survive Linux deploys

## Quick start

No build step is required. Clone the repo and open the page:

```bash
git clone https://github.com/vishnu-vemula/Music.git
cd Music
```

Then do either of the following:

- Open `index.html` directly in your browser, or
- Serve it locally (recommended, mirrors a real host):

```bash
python -m http.server 8080
# or
npx serve .
```

Visit `http://localhost:8080`.

## Project structure

```
.
├── index.html              Landing page markup
├── favicon.svg             Brand favicon (gradient music note)
├── assets/
│   ├── css/
│   │   └── styles.css      All styling, driven by design tokens
│   └── img/                Hero backdrops (see assets/img/README.md)
├── CONTRIBUTING.md         How to contribute
├── LICENSE                 MIT license
└── README.md               This file
```

## Customization

Everything visual is controlled from the `:root` block in
[`assets/css/styles.css`](assets/css/styles.css):

| Token              | Purpose                              | Default                            |
| ------------------ | ------------------------------------ | ---------------------------------- |
| `--color-brand`    | Primary brand color (headline)       | `#833ab4`                          |
| `--color-accent`   | Focus outlines / highlight           | `#fcb045`                          |
| `--gradient-brand` | Button gradient                      | orange → red → purple              |
| `--font-stack`     | Body font stack                      | `system-ui, …`                     |
| `--header-height`  | Header band height                   | `12rem`                            |
| `--page-gutter`    | Responsive side gutter               | `clamp(1.5rem, 8vw, 10rem)`        |
| `--hero-bg`        | Hero backdrop image                  | `url("../img/bg-money-1.jpg")`     |

To swap the backdrop, copy your image into `assets/img/` and point
`--hero-bg` at it — see [`assets/img/README.md`](assets/img/README.md) for the
bundled alternatives.

## Accessibility notes

- Skip-to-content link is the first focusable element
- Headings follow a single `<h1>` structure; the tagline is a `<p>`
- All interactive elements show a high-contrast `:focus-visible` outline
- The backdrop hue animation is disabled for users who prefer reduced motion
- Iconography is inline SVG marked `aria-hidden`; the logo carries an accessible name

## Browser support

Targets all evergreen browsers (Chrome, Edge, Firefox, Safari). Visual effects
use `backdrop-filter`, `svh` units, and CSS custom properties, each with
graceful fallbacks declared alongside.

## Contributing

Issues and pull requests are welcome — see [CONTRIBUTING.md](CONTRIBUTING.md).

## License

Released under the [MIT License](LICENSE).
