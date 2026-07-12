# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

This is a personal GitHub Pages static site deployed at `utf-8s.github.io`. There is no build step, bundler, or framework — it's plain HTML/CSS served directly.

## Pages

- **`index.html`** — Main personal homepage. Bilingual (Chinese/English), with a welcome hero, "About me" contact section (QQ, WeChat, GitHub, Email), header nav, and footer.
- **`pfstupage.html`** — Redirect/jump page for the "PFstu" studio, linking to old (`pfstu.github.io`) and new (`pfstu.netlify.app`) studio sites. Shares the same header/footer pattern as the main page but has its own stylesheet.

## CSS design system

- **`css/style.css`** — Styles for the main page. Uses CSS custom properties defined in `:root` for theming (colors, background image, blur amount). Header and footer use a semi-transparent `--UI-color` background. The `.about` section uses flexbox cards. Main layout is centered flex column.
- **`css/pfstupagestyle.css`** — Separate stylesheet for the PFstu page. Duplicates the header/footer styles from `style.css` rather than sharing them. The main page's `:root` variables (like `--purple-text-color`, `--main-p-size`) are not redefined here.

## Viewing the site

No server or build tool is required. Open any HTML file directly in a browser, or serve with any static file server:

```bash
python -m http.server 8080
# or
npx serve .
```

## Font

The custom font `Ubuntu-Regular.ttf` lives in `fonts/`. It's loaded via `@font-face` in `style.css` and applied globally through the universal `*` selector. The PFstu page does not load this font.

## Repository

GitHub Pages serves directly from the `master` branch root. Pushing to `master` deploys the site.
