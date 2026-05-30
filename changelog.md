# Changelog

## Unreleased — ZelfCSS fork

### Breaking changes
- Removed deprecated colour variables: `$color-initial`, `$color-primary`, `$color-secondary`, `$color-tertiary`, `$color-quaternary`, `$color-quinary`
- Grid gutter changed from negative margin hack to CSS `gap` — layouts using manual negative margin compensation may need adjustment
- Link `text-decoration` is now `underline` by default (was `none`)
- Form focus state now shows a visible `outline` (previously `outline: 0` — a WCAG violation)

### Added
- `_Variables.sass` — full spacing scale (`$space-1` through `$space-8`), typography tokens, breakpoint tokens
- `_Color.sass` — semantic colour roles: `$color-text`, `$color-background`, `$color-border`, `$color-border-focus`, `$color-interactive`, `$color-interactive-hover`, `$color-interactive-text`
- Alert colours updated: `$color-success`, `$color-info`, `$color-warning`, `$color-danger` now use accessible-contrast values
- `_Utility.sass` — `.sr-only` / `.visually-hidden`, `.text-left/center/right`, `.d-none`, `.d-block`, `.d-flex`

### Changed
- Build tooling: `node-sass` replaced with Dart `sass`
- `package.json` identity updated to ZelfCSS
- `_Typography.sass` — heading `font-weight` now varies by level; added `text-wrap: pretty` (paragraphs) and `text-wrap: balance` (headings)
- `_Grid.sass` — `.row` now uses `gap: 2.4rem` instead of `margin-left: -1rem` / `width: calc(100% + 2rem)`
- `_Base.sass` — `font-family` now uses `$font-family-base` token; `color` uses `$color-text` token
- `_Image.sass` — retained Harry Roberts LQIP technique (unchanged)
- Output file renamed from `milligram.css` to `zelfcss.css`

---

## Milligram 1.4.1 (upstream baseline)

See [Milligram releases](https://github.com/milligram/milligram/releases) for upstream history prior to this fork.
