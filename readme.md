# ZelfCSS

A minimalist CSS framework, forked and extended from [Milligram](https://milligram.io/).

ZelfCSS keeps the minimal philosophy — no utility soup, no component bloat — but modernises the things Milligram never updated: design tokens, accessibility, build tooling, and sensible defaults.

## What's different from Milligram

- **Design tokens** — proper spacing scale, semantic colour roles, and typography tokens in `_Variables.sass` and `_Color.sass`
- **Accessibility** — WCAG 2.2 AA compliant focus states on all interactive elements; links are underlined by default
- **Typography** — heading weights vary by level (h1/h2 bold, h3/h4 semi-bold, h5/h6 medium); `text-wrap: pretty` on body text; `text-wrap: balance` on headings
- **Grid** — CSS `gap` replaces the old negative margin gutter hack
- **Utility** — `.sr-only` / `.visually-hidden` for accessible hidden content; text alignment and display helpers
- **Build tooling** — Dart Sass (replaces the deprecated `node-sass`)

## Installation

**npm**
```
npm install zelfcss
```

**CDN** (coming soon)

**Direct download** — grab `dist/zelfcss.css` or `dist/zelfcss.min.css` from this repo.

## Usage

```html
<link rel="stylesheet" href="zelfcss.min.css">
```

ZelfCSS styles standard HTML elements directly — no class names needed for typography, forms, tables, or lists. Use the grid and utility classes where needed.

## Browser support

Modern browsers. No IE support.

## Contributing

See [contributing](.github/contributing.md).

## License

Based on [Milligram](https://milligram.io/) by [CJ Patoilo](https://twitter.com/cjpatoilo), extended by [X.R. Galdur](https://github.com/rvh-zelf). Licensed under the [MIT License](license).
