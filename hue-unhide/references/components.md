# Unhide — Components

## 1. BUTTONS

### Variants

| Variant | Background | Text Color | Border | Radius | Padding | Font | Weight |
|---------|-----------|------------|--------|--------|---------|------|--------|
| **Primary** | `--accent` | `#FFFFFF` | `1px solid --accent` | 5px | `15px 50px` | Body | 500 |
| **Secondary** | `--surface1` | `--text1` | `1px solid --text1` | 5px | `12px 24px` | Body | 500 |
| **Dark** | `--text1` | `--surface1` | `1px solid --text1` | 5px | `15px 50px` | Body | 500 |
| **Ghost** | `transparent` | `--text1` | `none` | 0px | `8px 0` | Body | 400 |

### States

| State | Primary | Secondary | Dark |
|-------|---------|-----------|------|
| **Hover** | Background darkens 8% | Background `--surface2` | Background `--surface3` (dark mode) |
| **Active** | `transform: scale(0.98)` | `transform: scale(0.98)` | `transform: scale(0.98)` |
| **Focus** | `outline: 2px solid --accent` offset 2px | Same | Same |
| **Disabled** | `opacity: 0.4` | `opacity: 0.4` | `opacity: 0.4` |

### Usage Rules

- Primary (olive) for checkout, add-to-cart — the single most important action
- Secondary (white with border) for CTAs within hero sections on photography
- Dark (black) for "Quick Add", secondary prominence actions
- Ghost for inline text links ("Continue shopping", "No thanks")
- Max one primary button per view. Two darks allowed. Unlimited ghosts.

---

## 2. CARDS / SURFACES

### Product Card (Observed)

| Property | Value |
|----------|-------|
| **Background** | `--surface1` (white) |
| **Border** | None |
| **Radius** | 4px |
| **Padding** | `8px 8px 15px` |
| **Shadow** | None (rest), `0 2px 8px rgba(30,30,30,0.06)` (hover) |
| **Image radius** | 4px |
| **Image fit** | `object-fit: cover` |

### Product Card Anatomy

```
┌─────────────────────────────┐
│  [Badge: "Our bestseller"]  │  ← pill badge, top-left overlay
│                             │
│       Product Image         │  ← 4px radius, cover fit
│                             │
├─────────────────────────────┤
│  ★★★★★ 2349 Reviews        │  ← gold stars + caption text
│  Marshmallow Blanket        │  ← h3, serif
│  A lil' blanket with big... │  ← body-sm, text2
│  From $49  On Sale $36.75   │  ← strikethrough + error color
│  Available in 9 colors      │  ← caption, text3
│                             │
│  [    Quick Add    ]        │  ← dark button, full-width
└─────────────────────────────┘
```

### Feature Card (Derived)

| Property | Value |
|----------|-------|
| **Background** | `--surface2` |
| **Border** | `1px solid --border` |
| **Radius** | 5px |
| **Padding** | `24px` |
| **Shadow** | None |

---

## 3. INPUTS

### Text Input (Observed — email style)

| Property | Value |
|----------|-------|
| **Background** | `transparent` |
| **Border** | Bottom only: `1px solid --text1` |
| **Radius** | 0px |
| **Padding** | `8px 0` |
| **Font** | Body, 16px, weight 400 |
| **Placeholder color** | `--text4` |

### Text Input (Derived — bordered)

| Property | Value |
|----------|-------|
| **Background** | `--surface1` |
| **Border** | `1px solid --border-visible` |
| **Radius** | 5px |
| **Padding** | `12px 16px` |
| **Font** | Body, 16px, weight 400 |
| **Focus border** | `1px solid --accent` |

### Select / Dropdown (Observed)

| Property | Value |
|----------|-------|
| **Background** | `#F2F2F2` → `--surface2` |
| **Border** | None |
| **Radius** | 4px |
| **Height** | 34px |
| **Font** | Body, 14px |

### Input States

| State | Treatment |
|-------|-----------|
| **Rest** | Default border |
| **Focus** | Border color → `--accent` |
| **Error** | Border color → `--error`, helper text in `--error` below |
| **Disabled** | `opacity: 0.4`, no pointer events |

---

## 4. BADGES & TAGS

### Promotional Badge (Observed)

| Property | Value |
|----------|-------|
| **Background** | `#E2E05D` (yellow-green) |
| **Text** | `#000000` |
| **Radius** | 40px (pill) |
| **Padding** | `6px 16px` |
| **Font** | Body, 14px, weight 400 |
| **Use** | "Our bestseller", "Great gift" |

### Status Badge (Observed)

| Property | Value |
|----------|-------|
| **Background** | `--success` (#11998E) |
| **Text** | `#FFFFFF` |
| **Radius** | 4px |
| **Padding** | `3px 8px` |
| **Font** | Caption, 12px |
| **Use** | "Best-seller" (product page) |

### Derived Tag

| Property | Value |
|----------|-------|
| **Background** | `--accent-subtle` |
| **Text** | `--accent` |
| **Radius** | 4px |
| **Padding** | `4px 10px` |
| **Font** | Caption, 12px, weight 500 |
| **Use** | Category tags, filter chips |

---

## 5. SIZE & COLOR SELECTORS

### Size Selector (Observed)

| Property | Value |
|----------|-------|
| **Background** | `--surface1` |
| **Border** | `1px solid --border-visible` |
| **Radius** | 4px |
| **Padding** | `8px 16px` |
| **Font** | Body-sm, 14px |
| **Selected** | `border-color: --text1` |

### Color Swatch (Observed)

| Property | Value |
|----------|-------|
| **Size** | 28px x 28px |
| **Radius** | 50% (circle) |
| **Border** | `1px solid --border-visible` |
| **Selected** | `outline: 2px solid --text1` with 2px offset |

---

## 6. STAR RATING (Observed)

| Property | Value |
|----------|-------|
| **Color (filled)** | `--accent-secondary` (#B59C63, gold) |
| **Color (empty)** | `--border-visible` |
| **Size** | 14px |
| **Gap** | 1px |
| **Review count** | Caption font, `--text3` |

---

## 7. NAVIGATION

### Header (Observed)

| Property | Value |
|----------|-------|
| **Background** | `--bg` |
| **Border bottom** | None |
| **Height** | ~60px |
| **Logo font** | Cormorant Garamond, ~28px, weight 600 |
| **Nav links** | Cormorant Garamond, 20px, weight 400, `--text1` |
| **Active link** | Italic style (Mother's Day Sale) |
| **Icons** | Thin stroke, right-aligned (search, account, cart) |

### Announcement Bar (Observed)

| Property | Value |
|----------|-------|
| **Background** | `--accent` (dark olive) |
| **Text** | `#FFFFFF` |
| **Font** | Body-sm, 14px |
| **Padding** | `10px 16px` |
| **Text align** | Center |

### Footer (Observed)

| Property | Value |
|----------|-------|
| **Background** | `--bg` |
| **Border top** | `1px solid --border` |
| **Padding** | `96px 0 10px` (generous top) |
| **Link color** | `--text1` |
| **Link hover** | `--accent-secondary` (gold) |
| **Wordmark** | Massive Cormorant Garamond, full-width |

---

## 8. OVERLAYS

### Modal (Derived)

| Property | Value |
|----------|-------|
| **Background** | `--surface1` |
| **Radius** | 10px |
| **Shadow** | `0 8px 32px rgba(30,30,30,0.12)` |
| **Padding** | `32px` |
| **Max width** | 480px |
| **Backdrop** | `rgba(30,30,30,0.5)` |
| **Close button** | Top-right, ghost style, thin "X" |

### Dropdown (Derived)

| Property | Value |
|----------|-------|
| **Background** | `--surface1` |
| **Border** | `1px solid --border` |
| **Radius** | 5px |
| **Shadow** | `0 8px 32px rgba(30,30,30,0.12)` |
| **Padding** | `8px 0` |
| **Item padding** | `10px 16px` |
| **Item hover** | `background: --surface2` |

---

## 9. STATE PATTERNS

### Empty State

- Centered layout, generous vertical padding (96px)
- Serif heading: "Nothing here yet" or contextual message
- Body-sm description in `--text3`
- Single CTA button (secondary variant)
- No illustrations — text does the work

### Loading

- Opacity fade-in (200ms) for content appearing
- Subtle shimmer on placeholders using `--surface2` → `--surface3` gradient animation
- No skeleton screens, no spinners

### Error

- Inline error text below the affected field in `--error`
- Error border on the input (`border-color: --error`)
- No toast notifications — errors appear in context

### Disabled

- `opacity: 0.4` on the entire component
- `pointer-events: none`
- No color changes — just the opacity reduction

---

## 10. PRICING DISPLAY

### Regular Price

| Context | Font | Size | Weight | Color |
|---------|------|------|--------|-------|
| Product card | Body | 16px | 400 | `--text1` |
| Product page | Body | 18px | 400 | `--text1` |
| Hero/display | Serif | Display | 400 | `--text1` |

### Sale Price

| Element | Treatment |
|---------|-----------|
| Original price | `text-decoration: line-through`, `--text3` |
| Sale label | "On Sale" in `--error` |
| Sale price | `--error` (#B4463E), same size as original |
| Savings | `(-$47.25)` in `--error`, parenthesized |
