# Unhide — Tokens

## 0. PRIMITIVES

Raw scales derived from the brand. These are the building blocks — semantic tokens reference them.

### Color Ramps

**Neutral** (warm cream-tinted)

| Step | Hex | Use |
|------|-----|-----|
| 50 | `#FAF7F0` | Lightest background (brand canvas) |
| 100 | `#F4F0E7` | Light surfaces |
| 200 | `#EBE1D0` | Borders, dividers (light) |
| 300 | `#DADACA` | Strong borders (light) |
| 400 | `#AAA494` | Placeholder text |
| 500 | `#7A756A` | Muted text |
| 600 | `#5C5850` | Secondary text |
| 700 | `#45413B` | Strong borders (dark) |
| 800 | `#2E2B27` | Dark surfaces |
| 900 | `#1E1E1E` | Darkest surface / primary text |
| 950 | `#121110` | Near-black background |

**Brand** (olive-gold)

| Step | Hex |
|------|-----|
| 50 | `#F7F3EB` |
| 100 | `#EDE5D3` |
| 200 | `#DBC9A5` |
| 300 | `#C6AD78` |
| 400 | `#B59C63` — warm gold accent |
| 500 | `#665C34` — primary accent (dark olive) |
| 600 | `#57502E` |
| 700 | `#474226` |
| 800 | `#38341E` |
| 900 | `#2A2717` |
| 950 | `#1C1A10` |

**Status Colors**

| Color | 50 (bg tint) | 500 (foreground) | 900 (dark tint) |
|-------|-------------|-----------------|-----------------|
| Red | `#FEF2EF` | `#B4463E` | `#5C2320` |
| Green | `#EEF7F6` | `#11998E` | `#0A4D47` |
| Amber | `#FFF8EB` | `#D4A843` | `#6A5422` |

### Spacing Primitives

`[0, 2, 4, 8, 12, 16, 24, 32, 40, 48, 64, 80, 96, 160]`

### Radii Primitives

`[0, 4, 5, 10, 40, 999]`

---

## 1. TYPOGRAPHY

### Font Stack

| Role | Font | Fallback | Weight | Use |
|------|------|----------|--------|-----|
| **Display / Heading** | `"Cormorant Garamond"` | `Georgia, "Times New Roman", serif` | 400, 500 | Screen titles, hero text, section headings, product names |
| **Body / UI** | `"Nunito Sans"` | `"Avenir", "Helvetica Neue", sans-serif` | 400, 500, 600 | Body text, descriptions, UI labels, buttons, navigation |
| **Mono** | `"DM Mono"` | `"Courier New", monospace` | 400 | Code snippets only (rarely used) |

### Data Font Rule

**`mono_for_code`: false | `mono_for_metrics`: false**

Unhide is a consumer lifestyle brand. All data — prices, review counts, dates — use the body font (Nunito Sans). Mono is reserved strictly for technical contexts that don't appear in the brand's consumer-facing UI. The serif Cormorant Garamond is sometimes used for large display prices in hero contexts.

### Why these fonts

Cormorant Garamond is the closest freely available match to Adonis, the brand's actual heading font (served via Typekit). Both are high-contrast transitional serifs with elegant italics and tight spacing. Nunito Sans approximates Avenir's geometric humanist character — warm, rounded, approachable without being childish.

### Type Scale

| Token | Size | Line Height | Letter Spacing | Weight | Use |
|-------|------|-------------|----------------|--------|-----|
| `--display` | 60px | 1.0 | -0.03em | 400 italic | Hero headlines, sale announcements |
| `--h1` | 42px | 1.1 | -0.03em | 400 | Page titles, collection names |
| `--h2` | 32px | 1.15 | -0.02em | 400 | Section headings |
| `--h3` | 24px | 1.2 | -0.02em | 500 | Card titles, subsections |
| `--body` | 16px | 1.5 | -0.01em | 400 | Body text, descriptions |
| `--body-sm` | 14px | 1.4 | -0.005em | 400 | Secondary text, product details |
| `--caption` | 12px | 1.3 | 0em | 400 | Timestamps, review counts, footnotes |
| `--label` | 11px | 1.2 | 0.02em | 500 | Micro-labels, metadata, uppercase tags |

### Typographic Rules

- Headlines always use Cormorant Garamond. Display size is italic; h1-h3 are roman unless editorial context calls for italic.
- Negative letter-spacing on all headings. Body text is near-zero.
- Max line length: 65ch for body text. Headlines can span full width.
- No bold (700+) on serif headings. The font's high contrast provides enough visual weight at 400.
- Prices at display scale may use the serif. Inline prices use the body font.

---

## 2. COLOR SYSTEM (Semantic Tokens)

Semantic tokens reference the primitives above. Components use semantic tokens, never primitives directly.

### Light Mode (Primary)

| Token | Value | Primitive | Use |
|-------|-------|-----------|-----|
| `--bg` | `#FAF7F0` | neutral.50 | Page canvas |
| `--surface1` | `#FFFFFF` | — | Cards, elevated surfaces |
| `--surface2` | `#F4F0E7` | neutral.100 | Nested surfaces, grouped areas |
| `--surface3` | `#EBE1D0` | neutral.200 | Input wells, subtle containers |
| `--border` | `#EBE1D0` | neutral.200 | Decorative borders |
| `--border-visible` | `#DADACA` | neutral.300 | Intentional borders |
| `--text1` | `#1E1E1E` | neutral.900 | Primary text |
| `--text2` | `#5C5850` | neutral.600 | Secondary text |
| `--text3` | `#7A756A` | neutral.500 | Tertiary text |
| `--text4` | `#AAA494` | neutral.400 | Disabled / placeholder text |
| `--accent` | `#665C34` | brand.500 | Primary interactive (dark olive) |
| `--accent-subtle` | `#F7F3EB` | brand.50 | Tinted backgrounds |
| `--accent-secondary` | `#B59C63` | brand.400 | Gold highlights, star ratings |
| `--success` | `#11998E` | green.500 | Positive states, badges |
| `--warning` | `#D4A843` | amber.500 | Caution |
| `--error` | `#B4463E` | red.500 | Sale prices, errors |

### Dark Mode

| Token | Value | Primitive | Use |
|-------|-------|-----------|-----|
| `--bg` | `#121110` | neutral.950 | Page canvas |
| `--surface1` | `#1E1E1E` | neutral.900 | Cards, elevated surfaces |
| `--surface2` | `#2E2B27` | neutral.800 | Nested surfaces |
| `--surface3` | `#45413B` | neutral.700 | Input wells |
| `--border` | `#2E2B27` | neutral.800 | Decorative borders |
| `--border-visible` | `#45413B` | neutral.700 | Intentional borders |
| `--text1` | `#FAF7F0` | neutral.50 | Primary text |
| `--text2` | `#AAA494` | neutral.400 | Secondary text |
| `--text3` | `#7A756A` | neutral.500 | Tertiary text |
| `--text4` | `#5C5850` | neutral.600 | Disabled text |
| `--accent` | `#B59C63` | brand.400 | Primary interactive (warm gold) |
| `--accent-subtle` | `#1C1A10` | brand.950 | Tinted backgrounds |
| `--accent-secondary` | `#C6AD78` | brand.300 | Gold highlights |
| `--success` | `#11998E` | green.500 | Positive states |
| `--warning` | `#D4A843` | amber.500 | Caution |
| `--error` | `#B4463E` | red.500 | Sale prices, errors |

---

## 3. SPACING

| Token | Value | Use |
|-------|-------|-----|
| `--space-2xs` | 2px | Hairline gaps |
| `--space-xs` | 4px | Tight internal padding |
| `--space-sm` | 8px | Card internal padding, inline gaps |
| `--space-md` | 16px | Standard component padding |
| `--space-lg` | 24px | Section internal spacing |
| `--space-xl` | 32px | Between related sections |
| `--space-2xl` | 48px | Between unrelated sections |
| `--space-3xl` | 64px | Major section breaks |
| `--space-4xl` | 96px | Page-level vertical rhythm |

---

## 4. BORDERS & RADII

### Corner Philosophy

Barely-there softness. Cards and buttons use 4-5px — enough to avoid sharpness without looking rounded. The brand is not pill-first; pills appear only on badges and promotional tags.

| Token | Value | Use |
|-------|-------|-----|
| `--radius-element` | 4px | Small controls, images, badges |
| `--radius-control` | 5px | Buttons, inputs |
| `--radius-component` | 5px | Cards, product tiles |
| `--radius-container` | 10px | Modals, feature panels |
| `--radius-pill` | 40px | Promotional badges, tags |
| `--radius-full` | 999px | Color swatches, avatar circles |

### Border Style

- Default: `1px solid var(--border)` — decorative, barely visible
- Visible: `1px solid var(--border-visible)` — intentional separation
- Active/Selected: `1px solid var(--text1)` — near-black for emphasis

---

## 5. ELEVATION & SHADOWS

### Strategy: Flat

Depth comes from background color shifts, not shadows. Cards are white (`--surface1`) sitting on cream (`--bg`). The material shift is the depth signal.

| Level | Value | Use |
|-------|-------|-----|
| **Rest** | `none` | Default state for all surfaces |
| **Hover** | `0 2px 8px rgba(30, 30, 30, 0.06)` | Subtle lift on interactive cards |
| **Overlay** | `0 8px 32px rgba(30, 30, 30, 0.12)` | Modals, dropdowns |

---

## 6. MOTION & INTERACTION

### Personality: Smooth

Calm, unhurried transitions. Nothing snaps or bounces — everything eases into place like fabric settling.

| Token | Value | Use |
|-------|-------|-----|
| `--duration-fast` | 100ms | Micro-interactions: hover color |
| `--duration-normal` | 200ms | Standard transitions: opacity, transform |
| `--duration-long` | 500ms | Page transitions, image reveals |
| `--easing` | `cubic-bezier(.36, .07, .19, .97)` | All transitions |

### Interaction States

- **Hover:** Subtle background shift or faint shadow. Never color change on text.
- **Active:** Scale down slightly (0.98) for buttons.
- **Focus:** 2px outline using `--accent` with 2px offset. Accessible, not decorative.
- **Disabled:** Opacity 0.4, no pointer events.

---

## 7. ICONOGRAPHY

### Brand Reality

Unhide uses very few icons — thin-stroke functional icons for search, cart, and account only. The brand is photography-driven; icons are wayfinding, not decorative.

### Fallback Kit: Phosphor Thin

| Property | Value |
|----------|-------|
| **Kit** | Phosphor (thin weight) |
| **CDN** | `https://unpkg.com/@phosphor-icons/web@2/src/thin/style.css` |
| **Class prefix** | `ph-thin ph-` |
| **Match score** | High |

**Match reasoning:** Phosphor thin matches the observed thin-stroke (~1px), soft-terminal, humanist icon style. The brand barely uses icons — Phosphor thin's delicate weight won't compete with the photography-first aesthetic.

> **Disclaimer:** Icons in generated output are a best-match fallback from the Phosphor kit. The brand's actual icons are custom and not redistributed with this skill.
