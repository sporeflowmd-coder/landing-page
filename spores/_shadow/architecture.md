---
Description: Language-agnostic technical blueprint for sporeflow-page.
Status: growing
---
# System DNA

## 🏗️ Folder Structure Convention
```
/root/               # Source files (HTML, CSS, JS, assets)
  
/spores/             # Intent definition (domain logic)
  /_shadow/          # Technical blueprints (this directory)
  /_food/            # Nutrients (bugs, prompts, post-mortems)
  /[domain]/         # Responsibility folders
  
/substrate/          # Protected secrets (not read by Agent)
```

## 📐 Design System Rules

### Typography Scale (CSS Custom Properties)
- Base size: 20px (desktop), 18px (mobile)
- Scale: 1.25 (major third)
- H1: clamp(2rem, 8vw, 4.5rem)
- H2: 2.4rem
- H3: 1.25rem
- Body: 1rem (20px base)
- Small: 0.9rem

### Color Palette (Earth Tones)
```css
--color-cream: #f5f0e6;
--color-parchment: #ebe3d4;
--color-sand: #d4c5a9;
--color-mushroom: #c9b896;
--color-brown: #6b5b4f;
--color-dark-brown: #4a3f35;
--color-bark: #3d3229;
--color-subtle-green: #8a9a7a;
--color-moss: #5c6b52;
```

### Responsive Breakpoints
- Desktop: > 1024px
- Tablet: 768px - 1024px
- Mobile: 480px - 768px
- Small Mobile: < 480px

### Spacing System
- xs: 0.5rem
- sm: 1rem
- md: 2rem
- lg: 4rem
- xl: 6rem

## 🔌 HTML Component Contracts

### Required Meta Tags
```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### Semantic Structure
- `<header class="header">` - Fixed navigation
- `<nav class="nav">` - Navigation container
- `<main class="content">` - Primary content area
- `<section class="section">` - Content sections with IDs for anchors
- `<footer class="footer">` - Page footer

### Class Naming Convention (BEM-ish)
- Block: `.header`, `.nav`, `.hero`
- Element: `.nav-links`, `.hero-content`, `.feature`
- Modifier: `.feature:hover`, `.nav-links a::after`

## 🧩 Component Patterns

### Navigation
- Logo: Left-aligned with decorative underline
- Links: Horizontal list with hover underline animation
- Mobile: Vertical stack with flex-wrap

### Hero Section
- Minimum height: 80vh (desktop), 60vh (mobile)
- Centered content with radial gradient background
- Pulsing animation on pseudo-element

### Features Grid
- CSS Grid with `auto-fit, minmax(250px, 1fr)`
- Cards with hover lift effect (transform + box-shadow)
- Padding: var(--space-md)

## 🔧 File Manifest

### /root/src/
| File | Purpose |
|------|---------|
| index.html | Main HTML document |
| styles.css | All CSS with custom properties |

## ✅ Consistency Rules
1. Always use CSS custom properties for colors, fonts, spacing
2. Use clamp() for responsive typography
3. Mobile-first approach for breakpoints
4. Semantic HTML5 elements
5. Smooth scroll behavior
6. Backdrop-filter for fixed headers
7. Grid for feature layouts
