---
name: design-damngoodbrands-com
description: Apply the visual design language of damngoodbrands.com (colors, typography, spacing, radii, shadows, motion) when building or restyling UI. Use when the user asks for a page, component or app that should look like damngoodbrands.com (accents: #e1ff46), font: Nord.
---

# Design system — damngoodbrands.com

Source: https://damngoodbrands.com/ — "Damn Good Brands | (Ad)venture™ Fund"

## How to use this skill

Reproduce the **look and feel** of damngoodbrands.com: palette, type, rhythm, shape and motion. Do **not** copy its text, logos, brand names, illustrations, photos or proprietary code — write original content and keep the structure of the user's own project.

1. Declare the tokens below as CSS custom properties (or map them into the project's theme: Tailwind config, theme.ts, etc.).
2. Use only these tokens for color, type size, spacing, radius and shadow — avoid ad-hoc values.
3. Check contrast (WCAG AA) for every text/background pair before finishing.
4. Make it responsive using the breakpoints listed, and keep keyboard focus visible.

## Colors

**Accent / brand colors** (most used first):

| Token | Hex | Uses |
|---|---|---|
| accent-1 | `#e1ff46` | 1 |

**Neutrals** (backgrounds, text, borders):

| Token | Hex | Uses |
|---|---|---|
| neutral-1 | `#000000` | 6 |
| neutral-2 | `#ffffff` | 4 |
| neutral-3 | `#ababab` | 2 |
| neutral-4 | `#f5f5f5` | 1 |
| neutral-5 | `#111111` | 1 |

**Observed roles:**

- Backgrounds seen most: `#000000`, `#ababab`, `#e1ff46`
- Text colors seen most: `#ffffff`, `#ababab`

## Typography

- Font families (by frequency): **Nord**, **NeueMontreal**, **Chomsky**, **InstrumentSerif**, **F37Stout**
- Self-hosted @font-face: Nord, NeueMontreal, Chomsky, InstrumentSerif, F37Stout, Mayonice
- Stack 1: `Nord`
- Stack 2: `monospace`
- Stack 3: `NeueMontreal`

**Type scale (observed):** 12px · 14px · 18px
- Weights: 400, 900, 500, 600
- Line heights: 1, .83, 1.4, 1.3, .7
- Letter spacing: .02em, -.05em, .024em, .015em

## Shape & depth

- Border radius: `4px`, `50%`, `5px`, `10px`
- Border widths: `1px`, `2px`

## Spacing & layout

- Spacing scale (px): 10
- Breakpoints (px): 580, 800, 801, 1200, 1600

## Motion

- Durations: .3s, .5s, .2s, .1s
- Easings: `ease-in-out`, `ease`, `ease-out`
- Respect `prefers-reduced-motion`.

## Ready-to-paste tokens

```css
:root {
  --accent-1: #e1ff46;
  --neutral-1: #000000;
  --neutral-2: #ffffff;
  --neutral-3: #ababab;
  --neutral-4: #f5f5f5;
  --neutral-5: #111111;
  --font-primary: Nord;
  --font-secondary: "NeueMontreal", system-ui, sans-serif;
  --text-1: 0.75rem; /* 12px */
  --text-2: 0.88rem; /* 14px */
  --text-3: 1.13rem; /* 18px */
  --space-1: 0.63rem; /* 10px */
  --radius-1: 4px;
  --radius-2: 50%;
  --radius-3: 5px;
}
```

## Original CSS variables (reference)

```css
--body-background: #000;
--body-color: #fff;
--body-color-rgb: 255,255,255;
--body-background-rgb: 0,0,0;
--body-border-color: rgba(var(--body-color-rgb),.2);
--body-subdued-color: rgba(var(--body-color-rgb),.5);
--active-color: lime;
```

## Checklist before finishing

- [ ] Colors come only from the tokens above
- [ ] Fonts loaded (Google Fonts or a close free alternative if the original is proprietary)
- [ ] Same radius / shadow language across all components
- [ ] Text contrast ≥ 4.5:1, focus states visible, mobile layout checked
- [ ] No copied copy, logos or images from the source site
