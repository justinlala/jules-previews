# Unhide — Platform Mapping

## 1. HTML / CSS / WEB

### Font Loading

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,500;1,400;1,500&family=Nunito+Sans:wght@400;500;600&family=DM+Mono:wght@400&display=swap" rel="stylesheet">
```

### Icon Loading

```html
<link rel="stylesheet" href="https://unpkg.com/@phosphor-icons/web@2/src/thin/style.css">
```

Usage: `<i class="ph-thin ph-magnifying-glass"></i>`

### CSS Custom Properties — Light Mode (Default)

```css
:root,
[data-theme="light"] {
  /* Colors */
  --bg: #FAF7F0;
  --surface1: #FFFFFF;
  --surface2: #F4F0E7;
  --surface3: #EBE1D0;
  --border: #EBE1D0;
  --border-visible: #DADACA;
  --text1: #1E1E1E;
  --text2: #5C5850;
  --text3: #7A756A;
  --text4: #AAA494;
  --accent: #665C34;
  --accent-subtle: #F7F3EB;
  --accent-secondary: #B59C63;
  --success: #11998E;
  --warning: #D4A843;
  --error: #B4463E;

  /* Typography */
  --font-display: "Cormorant Garamond", Georgia, "Times New Roman", serif;
  --font-body: "Nunito Sans", "Avenir", "Helvetica Neue", sans-serif;
  --font-mono: "DM Mono", "Courier New", monospace;

  /* Spacing */
  --space-2xs: 2px;
  --space-xs: 4px;
  --space-sm: 8px;
  --space-md: 16px;
  --space-lg: 24px;
  --space-xl: 32px;
  --space-2xl: 48px;
  --space-3xl: 64px;
  --space-4xl: 96px;

  /* Radii */
  --radius-element: 4px;
  --radius-control: 5px;
  --radius-component: 5px;
  --radius-container: 10px;
  --radius-pill: 40px;
  --radius-full: 999px;

  /* Elevation */
  --shadow-hover: 0 2px 8px rgba(30, 30, 30, 0.06);
  --shadow-overlay: 0 8px 32px rgba(30, 30, 30, 0.12);

  /* Motion */
  --duration-fast: 100ms;
  --duration-normal: 200ms;
  --duration-long: 500ms;
  --easing: cubic-bezier(.36, .07, .19, .97);
}
```

### CSS Custom Properties — Dark Mode

```css
[data-theme="dark"] {
  --bg: #121110;
  --surface1: #1E1E1E;
  --surface2: #2E2B27;
  --surface3: #45413B;
  --border: #2E2B27;
  --border-visible: #45413B;
  --text1: #FAF7F0;
  --text2: #AAA494;
  --text3: #7A756A;
  --text4: #5C5850;
  --accent: #B59C63;
  --accent-subtle: #1C1A10;
  --accent-secondary: #C6AD78;
  --success: #11998E;
  --warning: #D4A843;
  --error: #B4463E;

  --shadow-hover: 0 2px 8px rgba(0, 0, 0, 0.15);
  --shadow-overlay: 0 8px 32px rgba(0, 0, 0, 0.3);
}
```

---

## 2. SWIFTUI / iOS

### Color Extension

```swift
import SwiftUI

extension Color {
    // Neutral
    static let unhideBg = Color("bg") // #FAF7F0 light, #121110 dark
    static let unhideSurface1 = Color("surface1")
    static let unhideSurface2 = Color("surface2")
    static let unhideSurface3 = Color("surface3")
    static let unhideBorder = Color("border")
    static let unhideBorderVisible = Color("borderVisible")
    static let unhideText1 = Color("text1")
    static let unhideText2 = Color("text2")
    static let unhideText3 = Color("text3")
    static let unhideText4 = Color("text4")

    // Brand
    static let unhideAccent = Color("accent") // #665C34 light, #B59C63 dark
    static let unhideAccentSubtle = Color("accentSubtle")
    static let unhideAccentSecondary = Color("accentSecondary")

    // Semantic
    static let unhideSuccess = Color(hex: "#11998E")
    static let unhideWarning = Color(hex: "#D4A843")
    static let unhideError = Color(hex: "#B4463E")
}
```

### Font Extension

```swift
extension Font {
    static func unhideDisplay(_ size: CGFloat = 60) -> Font {
        .custom("Cormorant Garamond", size: size).italic()
    }
    static func unhideHeading(_ size: CGFloat = 42) -> Font {
        .custom("Cormorant Garamond", size: size)
    }
    static func unhideBody(_ size: CGFloat = 16) -> Font {
        .custom("Nunito Sans", size: size)
    }
    static func unhideCaption() -> Font {
        .custom("Nunito Sans", size: 12)
    }
    static func unhideLabel() -> Font {
        .custom("Nunito Sans", size: 11).weight(.medium)
    }
}
```

### Spacing & Radius Constants

```swift
enum UnhideSpacing {
    static let xxs: CGFloat = 2
    static let xs: CGFloat = 4
    static let sm: CGFloat = 8
    static let md: CGFloat = 16
    static let lg: CGFloat = 24
    static let xl: CGFloat = 32
    static let xxl: CGFloat = 48
    static let xxxl: CGFloat = 64
}

enum UnhideRadius {
    static let element: CGFloat = 4
    static let control: CGFloat = 5
    static let component: CGFloat = 5
    static let container: CGFloat = 10
    static let pill: CGFloat = 40
}
```

---

## 3. REACT / TAILWIND

### tailwind.config.js

```javascript
/** @type {import('tailwindcss').Config} */
module.exports = {
  theme: {
    extend: {
      colors: {
        bg: 'var(--bg)',
        surface: {
          1: 'var(--surface1)',
          2: 'var(--surface2)',
          3: 'var(--surface3)',
        },
        border: {
          DEFAULT: 'var(--border)',
          visible: 'var(--border-visible)',
        },
        text: {
          1: 'var(--text1)',
          2: 'var(--text2)',
          3: 'var(--text3)',
          4: 'var(--text4)',
        },
        accent: {
          DEFAULT: 'var(--accent)',
          subtle: 'var(--accent-subtle)',
          secondary: 'var(--accent-secondary)',
        },
        success: 'var(--success)',
        warning: 'var(--warning)',
        error: 'var(--error)',
      },
      fontFamily: {
        display: ['"Cormorant Garamond"', 'Georgia', 'serif'],
        body: ['"Nunito Sans"', '"Avenir"', 'sans-serif'],
        mono: ['"DM Mono"', 'monospace'],
      },
      fontSize: {
        display: ['60px', { lineHeight: '1.0', letterSpacing: '-0.03em' }],
        h1: ['42px', { lineHeight: '1.1', letterSpacing: '-0.03em' }],
        h2: ['32px', { lineHeight: '1.15', letterSpacing: '-0.02em' }],
        h3: ['24px', { lineHeight: '1.2', letterSpacing: '-0.02em' }],
        body: ['16px', { lineHeight: '1.5', letterSpacing: '-0.01em' }],
        'body-sm': ['14px', { lineHeight: '1.4', letterSpacing: '-0.005em' }],
        caption: ['12px', { lineHeight: '1.3', letterSpacing: '0em' }],
        label: ['11px', { lineHeight: '1.2', letterSpacing: '0.02em' }],
      },
      spacing: {
        '2xs': '2px',
        xs: '4px',
        sm: '8px',
        md: '16px',
        lg: '24px',
        xl: '32px',
        '2xl': '48px',
        '3xl': '64px',
        '4xl': '96px',
      },
      borderRadius: {
        element: '4px',
        control: '5px',
        component: '5px',
        container: '10px',
        pill: '40px',
      },
      transitionDuration: {
        fast: '100ms',
        normal: '200ms',
        long: '500ms',
      },
      transitionTimingFunction: {
        unhide: 'cubic-bezier(.36, .07, .19, .97)',
      },
      boxShadow: {
        hover: '0 2px 8px rgba(30, 30, 30, 0.06)',
        overlay: '0 8px 32px rgba(30, 30, 30, 0.12)',
      },
    },
  },
}
```

### Font Loading (Next.js / React)

```javascript
// app/layout.tsx or pages/_app.tsx
import { Cormorant_Garamond, Nunito_Sans, DM_Mono } from 'next/font/google'

const cormorant = Cormorant_Garamond({
  subsets: ['latin'],
  weight: ['400', '500'],
  style: ['normal', 'italic'],
  variable: '--font-display',
})

const nunitoSans = Nunito_Sans({
  subsets: ['latin'],
  weight: ['400', '500', '600'],
  variable: '--font-body',
})

const dmMono = DM_Mono({
  subsets: ['latin'],
  weight: ['400'],
  variable: '--font-mono',
})
```
