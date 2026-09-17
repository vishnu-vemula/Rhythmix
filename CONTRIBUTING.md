# Contributing to Rhythmix

Thanks for your interest in improving Rhythmix! This document covers everything
you need to start contributing.

## Getting set up

```bash
git clone https://github.com/vishnu-vemula/Music.git
cd Music
python -m http.server 8080   # or: npx serve .
```

Open `http://localhost:8080` and confirm the page renders before making changes.

There is no build step — the site is plain HTML and CSS.

## How to contribute

1. Fork the repository and create a branch from `main`:

   ```bash
   git checkout -b feature/my-change
   ```

2. Make your changes (see the guidelines below).
3. Test your changes in a browser — check mobile, desktop, and keyboard
   navigation (Tab / Shift+Tab).
4. Open a pull request describing **what** changed and **why**.

## Code guidelines

- **HTML** — 4-space indentation, semantic elements (`header`, `main`, `h1`),
  and alt/aria attributes on all non-text content.
- **CSS** — 4-space indentation, one selector per line blocks, custom
  properties in `:root` for any reusable value. No `!important`.
- **Assets** — images go in `assets/img/` following the `bg-<name>.<ext>`
  convention; optimize before committing.
- **No dependencies** — the project deliberately ships zero frameworks,
  fonts, or icon CDNs. Keep it that way; use inline SVG for icons.

## Accessibility checklist for PRs

- [ ] Keyboard reachable: every link/button is focusable with a visible outline
- [ ] Respects `prefers-reduced-motion` for any new animation
- [ ] Text contrast remains readable over the backdrop
- [ ] No heading-level skips

## Commit messages

Use short, imperative summaries, e.g. `Add reduced-motion fallback for hue animation`.

## Reporting issues

Open an issue with the browser, OS, and steps to reproduce. Screenshots help.
