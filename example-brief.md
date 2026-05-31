# ZelfCSS `example.html` — Content Brief

**Version:** 2026.05.31  
**Author:** Content Creator Skill  
**Purpose:** Define every section, heading, body copy, and demo content needed to build a comprehensive `example.html` showcase for the ZelfCSS framework. A developer should be able to build the page from this brief alone without ambiguity.

---

## Page Overview

| Property | Value |
|---|---|
| Page title | `ZelfCSS — Kitchen Sink` |
| Meta description | `Every feature of ZelfCSS demonstrated in one page — typography, grid, forms, buttons, tables, lists, code, alerts, and utilities.` |
| Stylesheet | `dist/zelfcss.min.css` |
| Wrapper | All demo content sits inside `.wrapper` for max-width and padding |
| Navigation | Sticky top nav bar (see §1) linking to each section via `id` anchors |

---

## Section Order

1. Navigation (sticky top)
2. Hero / Introduction
3. Typography
4. Colour Tokens
5. Buttons
6. Links
7. Grid — Flexbox (`.row` / `.column`)
8. Grid — CSS Grid (`.grid`, `.grid-2/.3/.4`, `.grid-auto`)
9. Forms
10. Tables
11. Lists
12. Code
13. Blockquote
14. Images
15. Alerts
16. Divider
17. Utility Classes
18. Spacing Tokens
19. Footer

---

## Section 1 — Sticky Top Navigation

**Element:** `<header>` with `position: sticky; top: 0` (demo-only CSS).  
**Purpose:** Let a developer jump to any section without scrolling. The nav doubles as a visual demo of ZelfCSS link styles.

### Logo / Brand area (left)
- Logo text: `ZelfCSS`
- Subtitle inline: `Kitchen Sink`

### Nav links (right, horizontal)
Links target each section `id` listed below. Use `.button.button-clear` on the "GitHub" link to show a button variant in context.

| Link label | Target `id` |
|---|---|
| Typography | `#typography` |
| Colour | `#colour` |
| Buttons | `#buttons` |
| Links | `#links` |
| Flex Grid | `#flex-grid` |
| CSS Grid | `#css-grid` |
| Forms | `#forms` |
| Tables | `#tables` |
| Lists | `#lists` |
| Code | `#code` |
| Blockquote | `#blockquote` |
| Images | `#images` |
| Alerts | `#alerts` |
| Utilities | `#utilities` |
| GitHub | external link, `.button.button-clear` style |

**Demo-only CSS note:** The sticky nav header needs a `background-color: $color-background` and `border-bottom: 1px solid $color-border` to separate it visually from page content. These are demo overrides — not framework styles.

---

## Section 2 — Hero / Introduction

**Heading (h1):** `Everything ZelfCSS can do, on one page.`  
**Body copy:**
> ZelfCSS is a minimalist CSS framework forked and modernised from Milligram. It styles standard HTML elements directly — no utility soup, no component bloat. This page demonstrates every feature the framework provides, from typography and forms to grid layouts and alert states.

**Sub-copy (smaller, muted):**
> Version 2026.05.31 · MIT Licence · Based on [Milligram](https://milligram.io/) by CJ Patoilo

**Implementation notes:**
- The hero sits inside `.wrapper` with generous top/bottom padding (demo-only).
- No image required — the copy carries the section.

---

## Section 3 — Typography

**Section `id`:** `typography`  
**Section heading (h2):** `Typography`  
**Purpose sentence:** Demonstrate all six heading levels, body text behaviour (`text-wrap: pretty`), bold/strong, and the heading scale produced by ZelfCSS tokens.

### Sub-section: Heading scale

Show all six headings one after another with a meaningful label beside each (use a `<small>` or a `<span class="text-muted">` aside — demo-only CSS):

| Element | Heading text to use |
|---|---|
| `<h1>` | `The quick brown fox jumps over the lazy dog` |
| `<h2>` | `The quick brown fox jumps over the lazy dog` |
| `<h3>` | `The quick brown fox jumps over the lazy dog` |
| `<h4>` | `The quick brown fox jumps over the lazy dog` |
| `<h5>` | `The quick brown fox jumps over the lazy dog` |
| `<h6>` | `The quick brown fox jumps over the lazy dog` |

Beside each heading, show its size and weight in muted text:
- h1: 4.6rem / 700
- h2: 3.6rem / 700
- h3: 2.8rem / 600
- h4: 2.2rem / 600
- h5: 1.8rem / 500
- h6: 1.6rem / 500

### Sub-section: Body text

**Heading (h3):** `Body Text`

Show a real paragraph (not lorem ipsum) demonstrating `text-wrap: pretty` (no orphaned words at line breaks):

> Good typography is invisible. When a reader moves through a well-set page, they absorb the meaning without noticing the craft. ZelfCSS inherits this principle from the web's own defaults and sharpens them — sensible line heights, a balanced heading scale, and `text-wrap: pretty` to prevent the single dangling word that makes a paragraph look unfinished.

Show a second, shorter paragraph:

> System fonts are used by default: fast, familiar, and honest. No external font load, no Flash of Invisible Text, no render-blocking stylesheet.

### Sub-section: Bold and strong

**Heading (h3):** `Bold & Strong`

Show an inline sentence:

> Semantically, `<strong>` and `<b>` both render as **bold** in ZelfCSS. Use `<strong>` when the bold carries emphasis in meaning; use `<b>` for stylistic weight without semantic emphasis.

---

## Section 4 — Colour Tokens

**Section `id`:** `colour`  
**Section heading (h2):** `Colour Tokens`  
**Purpose sentence:** Visualise the full colour palette — neutral scale, semantic roles, interactive states, and alert colours.

### Sub-section: Neutral scale

**Heading (h3):** `Neutral Scale`

Display swatches in a `.row` of `.column` blocks. Each swatch is a coloured box (demo CSS: `height: 6rem; border-radius: 4px;`) with the token name and hex beneath.

| Token | Hex value | Label |
|---|---|---|
| `$color-dark` | `#09090b` | Dark |
| `$color-grey-darkest` | `#27272a` | Grey — Darkest |
| `$color-grey-dark` | `#52525b` | Grey — Dark |
| `$color-grey` | `#a1a1a9` | Grey |
| `$color-grey-light` | `#e5e7eb` | Grey — Light |
| `$color-grey-lightest` | `#f4f5f6` | Grey — Lightest |
| `$color-light` | `#fafafa` | Light |

### Sub-section: Semantic roles

**Heading (h3):** `Semantic Colour Roles`

Table (2 columns: Token | Role):

| Token | Role / Usage |
|---|---|
| `$color-text` | Default body text |
| `$color-text-muted` | Secondary / supporting text |
| `$color-background` | Page background |
| `$color-border` | Borders on inputs, dividers |
| `$color-border-focus` | Focus ring on inputs |
| `$color-interactive` | Links, primary buttons, code border |
| `$color-interactive-hover` | Hover state for interactive elements |
| `$color-interactive-text` | Text on interactive backgrounds |

### Sub-section: Interactive & alert

**Heading (h3):** `Interactive & Alert Colours`

Swatches row (same format as neutral scale):

| Token | Hex | Label |
|---|---|---|
| `$color-interactive` | `#2563eb` | Interactive |
| `$color-interactive-hover` | `#1d4ed8` | Interactive — Hover |
| `$color-success` | `#16a34a` | Success |
| `$color-info` | `#2563eb` | Info |
| `$color-warning` | `#d97706` | Warning |
| `$color-danger` | `#dc2626` | Danger |

---

## Section 5 — Buttons

**Section `id`:** `buttons`  
**Section heading (h2):** `Buttons`  
**Purpose sentence:** Show all button variants — solid, outline, clear — as native `<button>` elements, `<a>` tags with `.button`, and input types, including disabled states.

### Sub-section: Solid (default)

**Heading (h3):** `Solid (Default)`  
**Copy:** `The default button uses the interactive colour token. Works on `<button>`, `<a>`, `<input type="submit">`, and `<input type="button">`.`

**Buttons to show (in one row, wrapped):**

```html
<button>Button</button>
<a class="button" href="#">Link Button</a>
<input type="submit" value="Submit Input">
<input type="button" value="Button Input">
<input type="reset" value="Reset Input">
<button disabled>Disabled</button>
```

### Sub-section: Outline

**Heading (h3):** `Outline`  
**Copy:** `.button-outline` gives a transparent background with a coloured border and text. On hover, the border darkens.

```html
<button class="button-outline">Outline</button>
<a class="button button-outline" href="#">Outline Link</a>
<button class="button-outline" disabled>Disabled</button>
```

### Sub-section: Clear

**Heading (h3):** `Clear`  
**Copy:** `.button-clear` removes the background and border entirely. Text only, coloured by the interactive token. Use for low-emphasis actions.

```html
<button class="button-clear">Clear</button>
<a class="button button-clear" href="#">Clear Link</a>
<button class="button-clear" disabled>Disabled</button>
```

---

## Section 6 — Links

**Section `id`:** `links`  
**Section heading (h2):** `Links`  
**Purpose sentence:** Demonstrate ZelfCSS link defaults — underlined, interactive-coloured, with a hover state that increases underline thickness.

**Body copy:**

> Links are underlined by default with a 1px text-decoration-thickness and a 0.2em underline offset. On hover and focus, the underline thickens to 2px and the colour shifts to `$color-interactive-hover`. Focus-visible adds a 2px outline for keyboard navigation.

**Demo links to show:**

```html
<p>
  Inline link: <a href="#">Read the full documentation</a> for installation and usage details.
</p>
<p>
  Another example: <a href="#">View on GitHub</a> · <a href="#">Download CSS</a> · <a href="#">Report an issue</a>
</p>
```

---

## Section 7 — Grid: Flexbox

**Section `id`:** `flex-grid`  
**Section heading (h2):** `Flexbox Grid`  
**Purpose sentence:** Demonstrate the `.row` / `.column` flexbox grid system — equal columns, fixed-percentage columns, offsets, and vertical alignment helpers.

**Intro copy:**

> The flexbox grid uses `.row` as the flex container and `.column` as the flex child. By default, columns share space equally. Explicit widths (`.column-50`, `.column-33`, etc.) and offsets (`.column-offset-25`, etc.) are available. On mobile (below 640px), columns stack vertically. Gaps use the `$space-5` token (24px).

### Sub-section: Equal columns

**Heading (h3):** `Equal Columns`  
Show a `.row` with 2, 3, and 4 equal `.column` children. Each column box has a light background (demo CSS) and centred text showing how many columns are in the row.

2-column example content in boxes:
- Box 1: `One of two`
- Box 2: `Two of two`

3-column example content:
- `One of three` / `Two of three` / `Three of three`

4-column example content:
- `One` / `Two` / `Three` / `Four`

### Sub-section: Explicit widths

**Heading (h3):** `Explicit Column Widths`  
Show a `.row` with explicit size classes. Use meaningful content (not just labels):

```
.column-25  → "Sidebar"
.column-75  → "Main content area — wider column paired with a sidebar"
```

Second example:

```
.column-33  → "Feature A"
.column-33  → "Feature B"
.column-34  → "Feature C"
```

### Sub-section: Offsets

**Heading (h3):** `Column Offsets`  
Show a `.row` where a column is pushed right using an offset:

```
[gap]  .column-offset-25  .column-50  → "Centred with a 25% left offset"
```

### Sub-section: Vertical alignment

**Heading (h3):** `Vertical Alignment`  
Use `.row-top`, `.row-center`, `.row-bottom` on separate `.row` elements. Each row contains two columns — one short, one tall (demo CSS to force different heights) — so the alignment is visible.

Label each row: `row-top`, `row-center`, `row-bottom`.

### Sub-section: Wrapper

**Heading (h3):** `Wrapper`  
**Copy:** `.wrapper` is the main page container. It centres content, sets a `max-width` of `1440px`, and applies `$space-5` horizontal padding. All demo sections on this page use `.wrapper`.

---

## Section 8 — Grid: CSS Grid

**Section `id`:** `css-grid`  
**Section heading (h2):** `CSS Grid`  
**Purpose sentence:** Demonstrate the `.grid`, `.grid-2`, `.grid-3`, `.grid-4`, and `.grid-auto` helper classes for CSS Grid layouts.

**Intro copy:**

> ZelfCSS provides lightweight CSS Grid helpers via `.grid` variants. Use `.grid-2`, `.grid-3`, or `.grid-4` for fixed column counts, or `.grid-auto` for auto-fill responsive columns.

### Sub-section: `.grid-2`

**Heading (h3):** `Two-Column Grid (.grid-2)`  
Show 4 boxes in a `.grid.grid-2`. Label boxes: `Item 1` through `Item 4`.

### Sub-section: `.grid-3`

**Heading (h3):** `Three-Column Grid (.grid-3)`  
Show 6 boxes in a `.grid.grid-3`. Label boxes: `Item 1` through `Item 6`.

### Sub-section: `.grid-4`

**Heading (h3):** `Four-Column Grid (.grid-4)`  
Show 8 boxes in a `.grid.grid-4`. Label boxes: `Item 1` through `Item 8`.

### Sub-section: `.grid-auto`

**Heading (h3):** `Auto-Fill Grid (.grid-auto)`  
**Copy:** `.grid-auto` uses `auto-fill` with a minimum column width, so columns reflow responsively without breakpoint classes.  
Show 6 boxes. Label: `Auto 1` through `Auto 6`.

**Demo-only CSS for grid boxes:** `background: #f4f5f6; padding: 2.4rem; border-radius: 4px; text-align: center;`

---

## Section 9 — Forms

**Section `id`:** `forms`  
**Section heading (h2):** `Forms`  
**Purpose sentence:** Demonstrate every form element ZelfCSS supports using a realistic contact/registration form scenario.

**Intro copy:**

> All form elements are full-width by default. Labels and legends use bold weight. Inputs, selects, and textareas share a consistent border, focus ring, and height. Fieldsets strip their native border and padding.

### Demo scenario: Conference registration form

Use a realistic CPD event registration form. This gives every input type a natural context.

**Form heading (h3):** `CPD Event Registration`

**Form structure and field-by-field content:**

#### Personal details fieldset

```
<fieldset>
  <legend>Personal Details</legend>

  Text input
    label: "Full name"
    placeholder: "Dr Jane Dlamini"
    type="text"

  Email input
    label: "Email address"
    placeholder: "jane.dlamini@hospital.co.za"
    type="email"

  Tel input
    label: "Contact number"
    placeholder: "+27 11 000 0000"
    type="tel"

  Password input
    label: "Create a password"
    placeholder: "Minimum 8 characters"
    type="password"

  Number input
    label: "Years in practice"
    placeholder: "e.g. 12"
    type="number"
    min="0" max="60"

  Date input
    label: "Date of birth"
    type="date"

  URL input
    label: "LinkedIn profile (optional)"
    placeholder: "https://www.linkedin.com/in/yourprofile"
    type="url"
</fieldset>
```

#### Event preferences fieldset

```
<fieldset>
  <legend>Event Preferences</legend>

  Select (single)
    label: "CPD category"
    options: "— Select a category —", "Clinical", "Ethical", "Management"

  Select (multiple)
    label: "Topics of interest (select all that apply)"
    options: "Cardiology", "Oncology", "Neurology", "Paediatrics", "General Practice", "Mental Health"
    multiple

  Textarea
    label: "Dietary requirements or accessibility needs"
    placeholder: "Please let us know if you have any special requirements."
    rows: 4

  Colour input
    label: "Preferred name badge colour"
    type="color"
    value="#2563eb"
</fieldset>
```

#### Attendance details fieldset

```
<fieldset>
  <legend>Attendance</legend>

  Radio group
    legend: "Attendance format"
    Options:
      radio value="in-person" label="In person (Sandton Convention Centre)"
      radio value="virtual"   label="Virtual (Zoom link sent on registration)"
      radio value="hybrid"    label="Hybrid (attend in person, recording access for 30 days)"

  Checkbox group
    legend: "Session preferences"
    Options:
      checkbox value="morning"    label="Morning session (08:00–12:00)"
      checkbox value="afternoon"  label="Afternoon session (13:00–17:00)"
      checkbox value="workshop"   label="Hands-on workshop (additional R500 — limited seats)"

  Single checkbox (agreement)
    type="checkbox"
    label (inline): "I confirm I am a registered HPCSA practitioner and consent to my attendance being recorded for CPD purposes."

  Search input
    label: "Search for a colleague to share your registration with"
    type="search"
    placeholder: "Search by name or HPCSA number"

  Month input
    label: "Month of HPCSA registration renewal"
    type="month"

  Week input
    label: "Preferred contact week"
    type="week"
</fieldset>
```

#### Submit area

```
<input type="submit" value="Register for CPD Event">
<input type="reset" value="Clear form">
```

---

## Section 10 — Tables

**Section `id`:** `tables`  
**Section heading (h2):** `Tables`  
**Purpose sentence:** Demonstrate ZelfCSS table styling — full-width, left-aligned, with bottom borders on cells, and horizontal scroll on small screens.

**Intro copy:**

> Tables are full-width by default, with bottom borders on every cell for legibility. On screens below 640px, the table scrolls horizontally to preserve column widths. First and last columns lose their left/right padding to stay flush with the wrapper.

**Demo scenario:** Webinar attendance report

Use a realistic dataset from a fictional CPD webinar to give the table meaningful content.

**Table heading (h3):** `CPD Attendance Report — Cardiology Update 2026`

| Registrant | HPCSA Number | Speciality | Attended | Duration Watched | CPD Awarded |
|---|---|---|---|---|---|
| Dr J. Dlamini | MP 0234567 | Cardiology | Yes | 58 min / 75 min | ✓ 1 Clinical |
| Dr A. Nkosi | MP 0198432 | General Practice | Yes | 48 min / 75 min | ✗ Below 75% |
| Dr P. van Wyk | MP 0312890 | Internal Medicine | Yes | 75 min / 75 min | ✓ 1 Clinical |
| Dr C. Pretorius | MP 0401234 | Cardiology | No | 0 min / 75 min | ✗ Did not attend |
| Dr S. Maharaj | MP 0287643 | Neurology | Yes | 62 min / 75 min | ✓ 1 Clinical |
| Dr L. Botha | MP 0356721 | Paediatrics | Yes | 70 min / 75 min | ✓ 1 Clinical |

**Table `<th>` content:**
`Registrant | HPCSA Number | Speciality | Attended | Duration Watched | CPD Awarded`

Add a `<caption>` element:
> "Attendance data exported from WebinarJam. CPD awarded to registrants who watched ≥75% of the session."

---

## Section 11 — Lists

**Section `id`:** `lists`  
**Section heading (h2):** `Lists`  
**Purpose sentence:** Demonstrate unordered lists, ordered lists, and nested lists with meaningful content.

### Sub-section: Unordered list

**Heading (h3):** `Unordered List`  
**Copy:** `Displayed with \`circle\` bullets inside the content flow.`

**List content — ZelfCSS design principles:**

- Styles standard HTML elements directly — no class names needed for most elements
- Accessibility-first: WCAG 2.2 AA compliant focus states throughout
- Semantic colour tokens — change one token, update the whole framework
- Uses `text-wrap: pretty` on paragraphs to prevent orphaned words
- Uses `text-wrap: balance` on headings for even line breaks
- CSS `gap` for gutters — no negative-margin hacks

### Sub-section: Ordered list

**Heading (h3):** `Ordered List`  
**Copy:** `Decimal, inside. Useful for step-by-step instructions.`

**List content — installing ZelfCSS:**

1. Install via npm: `npm install zelfcss`
2. Link the stylesheet in your `<head>`: `<link rel="stylesheet" href="dist/zelfcss.min.css">`
3. Write standard HTML — ZelfCSS styles it directly
4. Add `.wrapper` to centre your content
5. Use `.row` and `.column` for flexbox layouts
6. Use `.grid-2`, `.grid-3`, or `.grid-4` for CSS Grid layouts

### Sub-section: Nested list

**Heading (h3):** `Nested List`  
**Copy:** `Nested lists reduce font size to 90% and indent 30px.`

**List content:**

- Grid system
  - Flexbox grid (`.row` / `.column`)
    - Equal columns
    - Explicit percentage widths
    - Column offsets
    - Vertical alignment helpers
  - CSS Grid (`.grid`, `.grid-2`, `.grid-3`, `.grid-4`, `.grid-auto`)
- Typography
  - Headings (h1–h6)
  - Body text with `text-wrap: pretty`
  - Bold and strong

---

## Section 12 — Code

**Section `id`:** `code`  
**Section heading (h2):** `Code`  
**Purpose sentence:** Demonstrate inline `<code>` and block `<pre><code>` styling — light background, monospace, and the blue left-border on code blocks.

**Intro copy:**

> Inline code has a light grey background, rounded corners, and a slight size reduction. Block code (`<pre><code>`) adds a left border in the interactive colour and allows horizontal scrolling for long lines.

### Sub-section: Inline code

**Heading (h3):** `Inline Code`

Show inline `<code>` within sentences:

> Use the `.wrapper` class to centre content. Set `max-width: 144rem` and `padding: 0 $space-5` for consistent horizontal spacing. The `$space-5` token equals `2.4rem` (24px).

### Sub-section: Code block

**Heading (h3):** `Code Block`

Show a real HTML snippet as a `<pre><code>` block — use actual ZelfCSS markup so it's useful, not decorative:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>My ZelfCSS Page</title>
    <link rel="stylesheet" href="dist/zelfcss.min.css">
  </head>
  <body>
    <div class="wrapper">
      <h1>Hello, ZelfCSS</h1>
      <p>A minimalist CSS framework that gets out of your way.</p>

      <div class="row">
        <div class="column">One</div>
        <div class="column">Two</div>
        <div class="column">Three</div>
      </div>
    </div>
  </body>
</html>
```

Show a second block — SCSS variable override example:

```scss
// Override ZelfCSS tokens before import
$color-interactive: #e11d48;        // rose — replace default blue
$color-interactive-hover: #be123c;
$font-family-base: 'Inter', system-ui, sans-serif;

@import 'zelfcss/src/milligram';
```

---

## Section 13 — Blockquote

**Section `id`:** `blockquote`  
**Section heading (h2):** `Blockquote`  
**Purpose sentence:** Demonstrate the `<blockquote>` element — a 3px left border in the border colour, with flushed margins and padded content.

**Intro copy:** `Blockquotes use a coloured left border and internal padding. The last child element inside has its bottom margin removed.`

**First blockquote:**

> Good design is as little design as possible. Less, but better — because it concentrates on the essential aspects, and the products are not burdened with non-essentials. Back to purity, back to simplicity.
>
> — Dieter Rams

**Second blockquote (nested paragraph + citation):**

> The Web is not a platform. It is a medium. The difference matters: a platform constrains what you can build; a medium amplifies what you already know how to make.
>
> Write standard HTML. Style it once. Ship it everywhere.

---

## Section 14 — Images

**Section `id`:** `images`  
**Section heading (h2):** `Images`  
**Purpose sentence:** Demonstrate responsive images and the LQIP (Low-Quality Image Placeholder) technique built into ZelfCSS's `_Image.sass`.

**Intro copy:**

> ZelfCSS makes all images responsive (`max-width: 100%; height: auto`) and uses the LQIP technique from Harry Roberts (CSS Wizardry). A blurred, low-quality version of the image is set as a `background-image` inline style. When the full image loads, it covers the placeholder seamlessly — no layout shift, no blank loading state.

**Heading (h3):** `Responsive Image (no LQIP)`

Show a standard responsive image. Use a placeholder service for the demo:

```html
<img
  src="https://placehold.co/800x400"
  alt="An 800×400 placeholder image demonstrating responsive scaling within the wrapper"
  width="800"
  height="400"
>
```

**Heading (h3):** `LQIP Technique`

**Copy:**

> Set `background-image` to a tiny base64-encoded or low-resolution version of the image inline on the `<img>` element. ZelfCSS handles `background-size: cover` and `background-repeat: no-repeat` automatically. The `shape-margin: 0.75rem` property is also applied for float-based image shapes.

Show a code example of the LQIP pattern:

```html
<img
  src="high-res-photo.jpg"
  style="background-image: url('data:image/jpeg;base64,/9j/4AAQ...')"
  alt="Photo of the Sandton Convention Centre conference hall"
  width="1200"
  height="600"
  loading="lazy"
>
```

---

## Section 15 — Alerts

**Section `id`:** `alerts`  
**Section heading (h2):** `Alerts`  
**Purpose sentence:** Show all five alert variants — default (grey), success, info, warning, and danger — with realistic content.

**Intro copy:**

> Alerts use a 10% tint of the semantic colour for both background and border, with the full colour applied to text. The `.alert` base class handles layout and spacing; modifier classes apply the colour variant.

**Alert content to use:**

```html
<!-- Default / neutral -->
<div class="alert">
  <strong>Note:</strong> Your registration details have been saved as a draft. 
  Complete payment to confirm your CPD event booking.
</div>

<!-- Success -->
<div class="alert alert-success">
  <strong>Registration confirmed.</strong> You are registered for the Cardiology Update 2026 
  webinar. A confirmation email has been sent to jane.dlamini@hospital.co.za.
</div>

<!-- Info -->
<div class="alert alert-info">
  <strong>CPD processing in progress.</strong> HPCSA submission for the February 2026 webinar 
  series is scheduled for 14 March 2026. You will receive a confirmation once submitted.
</div>

<!-- Warning -->
<div class="alert alert-warning">
  <strong>Attendance below threshold.</strong> You watched 48 of 75 minutes of the session 
  (64%). A minimum of 75% attendance is required to earn the CPD point for this webinar.
</div>

<!-- Danger -->
<div class="alert alert-danger">
  <strong>HPCSA number not found.</strong> The number MP 0000000 does not match any record in 
  the HPCSA register. Please check the number and try again, or contact support.
</div>
```

---

## Section 16 — Divider

**Section `id`:** `divider` (covered within the page naturally — no dedicated nav link needed; can be shown within any section or between sections as a real example)

**Purpose sentence:** Show the `<hr>` element as a visual section separator.

**Placement:** Show an `<hr>` between two paragraphs in a sub-section of its own.

**Heading (h3):** `Horizontal Rule`  
**Copy above the `<hr>`:**
> ZelfCSS strips the native `<hr>` border and replaces it with a clean 1px top border using `$color-grey-lightest`. The margin is `3.0rem` top and bottom.

```html
<hr>
```

**Copy below the `<hr>`:**
> The rule above uses no class names — just a standard `<hr>` element. It works as a content divider anywhere in the flow.

---

## Section 17 — Utility Classes

**Section `id`:** `utilities`  
**Section heading (h2):** `Utility Classes`  
**Purpose sentence:** Demonstrate all utility classes — screen-reader only, text alignment, display helpers, and float helpers.

**Intro copy:**

> ZelfCSS ships a minimal utility layer. No utility soup — just the essential toggles a minimalist framework actually needs.

### Sub-section: Screen reader only

**Heading (h3):** `Visually Hidden (`.sr-only` / `.visually-hidden`)`

**Copy:**

> `.sr-only` and `.visually-hidden` are aliases. Both hide content visually while keeping it accessible to screen readers — useful for icon-only buttons, skip-navigation links, and supplementary context labels.

Show a button where the label is `.sr-only`:

```html
<button>
  <!-- SVG icon here -->
  <span class="sr-only">Close dialog</span>
</button>
```

Add a note: "Inspect the element above — the 'Close dialog' text is in the DOM but invisible. Screen readers will announce it."

### Sub-section: Text alignment

**Heading (h3):** `Text Alignment`

Show three paragraphs, each inside a bordered box (demo CSS), one per alignment class:

```html
<p class="text-left">Left-aligned text — the default for body content. 
Reads naturally in left-to-right languages.</p>

<p class="text-center">Centre-aligned text — use sparingly; best for 
short headings, labels, or call-to-action copy.</p>

<p class="text-right">Right-aligned text — useful for numerical data 
in tables or right-side UI elements.</p>
```

### Sub-section: Display helpers

**Heading (h3):** `Display Helpers`

Show each class with a visible element:

```html
<!-- .d-none: hidden — show the class name as a label so it's clear the element exists -->
<span class="d-none">This text is hidden with .d-none (display: none)</span>

<!-- .d-block -->
<span class="d-block" style="background: #f4f5f6; padding: 1.2rem;">
  This span is block-level with .d-block
</span>

<!-- .d-flex -->
<div class="d-flex" style="gap: 1.6rem; background: #f4f5f6; padding: 1.2rem;">
  <span>Flex child 1</span>
  <span>Flex child 2</span>
  <span>Flex child 3</span>
</div>
```

### Sub-section: Float helpers

**Heading (h3):** `Float Helpers (Legacy)`

**Copy:** `.float-left` and `.float-right` are included for legacy use cases. Prefer flexbox or CSS Grid for layout.

Show a clearfix example — a small image floated left with text wrapping around it:

```html
<div style="overflow: hidden;">
  <img class="float-left" src="https://placehold.co/120x80" alt="Floated image"
       style="margin: 0 1.6rem 1.6rem 0;">
  <p>This paragraph wraps around the floated image to the right. Float-based layout
  was the standard approach before flexbox. ZelfCSS includes .float-left and 
  .float-right for backward compatibility — use .row/.column for new layouts.</p>
</div>
```

---

## Section 18 — Spacing Tokens

**Section `id`:** `spacing` (shown in nav as part of Utilities or as a separate section)  
**Section heading (h2):** `Spacing Tokens`  
**Purpose sentence:** Visualise the `$space-1` through `$space-8` spacing scale to help developers choose consistent spacing values.

**Intro copy:**

> ZelfCSS uses an 8px base spacing scale. Tokens run from `$space-1` (4px) to `$space-8` (64px). These values drive internal spacing in the framework — use them as reference when writing component or page-level CSS.

**Display as a table:**

| Token | Value | px equivalent | Visual bar |
|---|---|---|---|
| `$space-1` | `0.4rem` | 4px | (thin bar) |
| `$space-2` | `0.8rem` | 8px | |
| `$space-3` | `1.2rem` | 12px | |
| `$space-4` | `1.6rem` | 16px | |
| `$space-5` | `2.4rem` | 24px | (used for wrapper padding, grid gaps) |
| `$space-6` | `3.2rem` | 32px | |
| `$space-7` | `4.8rem` | 48px | |
| `$space-8` | `6.4rem` | 64px | (thickest bar) |

**Implementation note for developer:** Render each row with a coloured bar `<div style="width: <px value>; height: 1.6rem; background: #2563eb; border-radius: 2px;">` in a table cell to give a visual scale. This is demo-only CSS.

---

## Section 19 — Footer

**Element:** `<footer>` with `.wrapper`  
**Purpose:** Close the page cleanly and credit the framework.

**Content:**

```
ZelfCSS — A minimalist CSS framework

Based on Milligram by CJ Patoilo · Extended by Ruan van Heerden · MIT Licence

[GitHub] [Download CSS] [Report an issue]   ← .button.button-clear links
```

**Small copy below:**

> This page demonstrates ZelfCSS version 2026.05.31. All HTML elements on this page are styled solely by `dist/zelfcss.min.css` plus minimal demo-only overrides for coloured swatch boxes, grid demo boxes, and section padding. No other CSS framework is used.

---

## Demo-Only CSS Summary

The `example.html` file needs a small `<style>` block for demo scaffolding. This is not part of the framework. Include these classes:

```css
/* Demo scaffolding — not part of ZelfCSS */

body { padding: 0; }

.demo-header {
  position: sticky;
  top: 0;
  background: #fafafa;
  border-bottom: 1px solid #e5e7eb;
  padding: 1.6rem 2.4rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1.6rem;
  z-index: 100;
}

.demo-header nav a {
  margin-left: 1.6rem;
  font-size: 1.4rem;
  text-decoration: none;
}

.demo-section {
  padding: 4.8rem 0;
}

.demo-section h2 {
  border-bottom: 2px solid #e5e7eb;
  padding-bottom: 0.8rem;
  margin-bottom: 2.4rem;
}

.demo-box {
  background: #f4f5f6;
  padding: 2.4rem;
  border-radius: 4px;
  text-align: center;
}

.swatch {
  height: 6rem;
  border-radius: 4px;
  margin-bottom: 0.8rem;
}
```

---

## Acceptance Checklist for the Developer

Before marking `example.html` complete, verify:

- [ ] Sticky nav links correctly to every section `id`
- [ ] All 6 heading levels visible
- [ ] Body text paragraphs rendered with `text-wrap: pretty` (inspect computed styles)
- [ ] All button variants shown: solid, outline, clear, disabled
- [ ] All form input types present: text, email, tel, password, number, date, url, color, search, month, week, select (single + multiple), textarea, checkbox, radio
- [ ] Flexbox grid: equal columns (2/3/4), explicit widths, offsets, and vertical alignment rows
- [ ] CSS Grid: `.grid-2`, `.grid-3`, `.grid-4`, `.grid-auto` all shown
- [ ] Table includes `<caption>`, `<th>` headers, and 6 data rows
- [ ] Unordered, ordered, and nested lists all present
- [ ] Inline code and block code both shown with real ZelfCSS snippets
- [ ] Blockquote renders with left border
- [ ] Responsive image and LQIP technique both shown
- [ ] All 5 alert variants present (default, success, info, warning, danger)
- [ ] `<hr>` shown as divider
- [ ] `.sr-only` / `.visually-hidden` demonstrated
- [ ] Text alignment classes shown (.text-left, .text-center, .text-right)
- [ ] Display helpers shown (.d-none, .d-block, .d-flex)
- [ ] Float helpers shown (.float-left, .float-right)
- [ ] Colour token swatches and table present
- [ ] Spacing token table with visual bars present
- [ ] Footer with credits present
- [ ] Playwright render passes with no console errors

