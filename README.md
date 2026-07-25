# Animated SVG Icons UI Library

A complete, high-performance library of animated SVG icons optimized for modern user interfaces. These icons use pure CSS and SMIL for lightweight, scalable, and crisp animations without external JavaScript dependencies.

## 🚀 Features

* **Infinite Scalability:** Sharp rendering at any resolution or pixel density.
* **Ultra Lightweight:** Smaller file sizes than GIFs or Lottie JSON files.
* **Interactive Triggers:** Built-in support for hover, click, and loop states.
* **Easy Customization:** Control colors, stroke widths, and speeds via CSS variables.
* **Framework Agnostic:** Works natively in HTML, React, Vue, Angular, and Svelte.

---

## 📦 Installation

### Option 1: Direct Download
Copy the SVGs directly from the `/icons` directory into your project's asset folder.

### Option 2: CDN (Recommended for vanilla HTML)
Add the global stylesheet to your `<head>` tag to enable animations:
```html
<link rel="stylesheet" href="https://jsdelivr.net">
```

---

## 🛠️ Usage Examples

### 1. Vanilla HTML (Inline SVG)
Inline usage allows full CSS control and interactive hover triggers.

```html
<!-- Example: Animated Search Icon -->
<svg class="animated-icon icon-search" viewBox="0 0 24 24" width="24" height="24">
  <circle cx="11" cy="11" r="8" class="search-glass" />
  <line x1="21" y1="21" x2="16.65" y2="16.65" class="search-handle" />
</svg>
```

### 2. React Component
```jsx
import React from 'react';
import './icons.css';

export const SearchIcon = ({ size = 24, color = 'currentColor' }) => (
  <svg 
    className="animated-icon icon-search" 
    viewBox="0 0 24 24" 
    width={size} 
    height={size}
    stroke={color}
  >
    <circle cx="11" cy="11" r="8" className="search-glass" />
    <line x1="21" y1="21" x2="16.65" y2="16.65" className="search-handle" />
  </svg>
);
```

---

## 🎨 Customization

You can globally or individually customize the icons using standard CSS custom properties.

```css
:root {
  --icon-color: #3b82f6;       /* Primary icon color */
  --icon-hover-color: #1d4ed8; /* Hover state color */
  --icon-stroke-width: 2px;    /* Thickness of lines */
  --icon-speed: 0.3s;          /* Animation duration */
}

/* Application example */
.animated-icon {
  stroke: var(--icon-color);
  stroke-width: var(--icon-stroke-width);
  transition: stroke var(--icon-speed) ease;
}

.animated-icon:hover {
  stroke: var(--icon-hover-color);
}
```

---

## 🧪 Core Animation Classes

Apply these helper classes directly to your SVGs to change trigger behaviors:

| Class Name | Animation Trigger | Best Used For |
| :--- | :--- | :--- |
| `.anim-loop` | Runs continuously on page load | Loaders, spinners, alerts |
| `.anim-hover` | Triggers only on mouse hover | Buttons, navigation links |
| `.anim-click` | Triggers once upon active click | Checkboxes, bookmarks, hearts |

---
