---
name: unhide-design
description: "This skill should be used when the user explicitly says 'Unhide style', 'Unhide design', '/unhide-design', or directly asks to use/apply the Unhide design system. NEVER trigger automatically for generic UI or design tasks."
version: 1.0.0
allowed-tools: [Read, Write, Edit, Glob, Grep]
---

# Unhide

You are a senior product designer. When this skill is active, every UI decision follows this design language.

**Before starting any design work, declare which fonts are required and how to load them** (see `references/platform-mapping.md`). Never assume fonts are already available.

---

## 1. DESIGN PHILOSOPHY

Warm tactile luxury. A cashmere blanket folded on a linen sofa — premium restraint meets cozy approachability. The Unhide design language draws from high-end home goods catalogs and Scandinavian interior editorials: cream canvases, olive-gold accents, and serif typography that breathes.

The primary tension is between editorial sophistication and domestic warmth. Headlines are italic serif — elegant but never cold. Layouts are generous with whitespace, letting product photography do the emotional work. Color is used sparingly: olive and gold whisper where lesser brands would shout.

Design lineage: Kinfolk magazine, Aesop packaging, The Row retail, Cereal magazine. Objects and textures matter more than interface chrome.

---

## 2. CRAFT RULES — HOW TO COMPOSE

### Visual Hierarchy Layers

| Layer | Role | How |
|-------|------|-----|
| **Hero** | Emotional anchor | Full-bleed photography or warm gradient, italic serif headline at display scale |
| **Primary** | Core content | Serif headings (Cormorant Garamond), generous padding, product imagery |
| **Secondary** | Supporting info | Sans-serif body (Nunito Sans), muted text colors, smaller scale |
| **Tertiary** | Metadata | Captions, timestamps, ratings in text3 color |

### Typography Discipline

Two fonts maximum per screen: Cormorant Garamond for display/headings, Nunito Sans for body/UI. The serif does the heavy lifting — hierarchy comes from scale and italic style, not from weight or color variations. Headlines are light (400 weight) and breathe with negative letter-spacing (-0.03em).

### Spacing Semantics

Generous spacing is identity-defining. Sections breathe with 64-96px vertical rhythm. Cards use 8px internal padding — tight enough to feel considered, not crammed. The base grid is 8px. When in doubt, add more space, not less.

### Color Strategy

Monochrome-forward. The palette is cream, olive, gold, and near-black. Chromatic color appears only for semantic states (teal for positive, warm red for sale/error, yellow-green for badges). Every screen should read as warm-neutral at a glance, with color as punctuation.

### Composition Approach

Photography-first. Let images occupy 60-70% of visual weight. UI chrome recedes — no heavy borders, no shadows, no gradients on surfaces. Cards are white on cream, distinguished by the faintest material shift. Borders are decorative whispers (1px, warm gray).

### Squint Test

Squint at the screen. You should see: warm cream field, blocks of lifestyle imagery, one or two olive/gold accent touches, and generous breathing room. If you see busy UI, colored blocks, or dense interface chrome — pull back.

---

## 3. ANTI-PATTERNS — WHAT TO NEVER DO

- **No drop shadows on cards or surfaces.** Depth comes from background color shifts (white on cream), never from shadows.
- **No border-radius above 10px on cards or containers.** Only badges/pills use large radius (40px). Cards are 4-5px — barely there.
- **No saturated accent colors.** The brand palette is earth-toned. No electric blues, vivid purples, or neon anything.
- **No uppercase text-transform on headings.** Headlines are sentence case or title case, never all-caps. Labels may use uppercase sparingly.
- **No heavy font weights on headings.** Display and h1 are weight 400. h3 is 500 max. Bold (700+) is banned from headings.
- **No more than 2 chromatic colors per screen.** Olive/gold for accents, one semantic color if needed. That's it.
- **No gradient backgrounds on surfaces.** Surfaces are flat solid colors — cream, white, or the dark-mode equivalents.
- **No skeleton loading screens.** Use subtle opacity fade-in instead.
- **No icon-heavy UI.** Icons are functional wayfinding only (search, cart, account). Never decorative, never in feature sections.
- **No cold grays.** Every neutral must be warm-tinted. Blue-gray is a foreign element in this language.
- **No toast notifications.** Status changes appear inline, not as floating popups.
- **No thin sans-serif for headings.** If it's a heading, it's the serif. The sans handles body and UI only.

---

## 4. WORKFLOW

1. **Declare fonts** — check `references/platform-mapping.md` for loading instructions
2. **Set tokens** — apply variables from `references/tokens.md`
3. **Build components** — use specs from `references/components.md`
4. **Check hierarchy** — squint test: warm cream canvas, serif headlines, photography dominance?
5. **Verify both modes** — light and dark must both feel warm, not clinical
6. **Test extremes** — long product names, empty collections, single item, 100 items
7. **Platform-adapt** — consult `references/platform-mapping.md` for output conventions

---

## 5. REFERENCE FILES

| File | Contains |
|------|----------|
| `references/tokens.md` | Fonts, type scale, color system (light + dark), spacing, radii, elevation, motion, iconography |
| `references/components.md` | Buttons, cards, inputs, badges, navigation, overlays, state patterns |
| `references/platform-mapping.md` | HTML/CSS, SwiftUI, React/Tailwind — platform-specific code and loading instructions |
