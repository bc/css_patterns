# 🎨 textures.css

A programmatic, color-driven CSS texture library for light background surfaces.

`textures.css` allows you to generate a full surface design—background, accents, and text colors—using **one single color variable**.

## 🚀 Quick Start (CDN)

The easiest way to use the library is via **jsDelivr**, which mirrors this GitHub repository.

Add this to your `<head>`:
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/bc/css_patterns/textures.css">
```

## 🛠 How to Use

### 1. Basic Implementation
Apply the `.tex` base class, a pattern class, and a strength tier.

```html
<!-- A medium-strength honeycomb pattern in a rose color -->
<div class="tex tex-hex tier-medium c-rose">
  <h2>Hello World</h2>
</div>
```

### 2. Custom Colors
You aren't limited to presets. You can pass any hex color using a CSS variable:

```html
<div class="tex tex-aurora" style="--c: #0d9488">
  <h2>Custom Teal Glow</h2>
</div>
```

### 3. The "One Color" Engine
The library uses `color-mix()` and relative color syntax to derive a complete palette from `--c`:
- `--p` (Primary): The soft, tinted background.
- `--s` (Secondary): The hue-shifted pattern accent.
- `--ink` (Ink): A high-contrast text color for readability.

### 4. Customization Knobs
| Variable | Description | Example |
| :--- | :--- | :--- |
| `--hue` | Shifts the accent color hue (in degrees) | `style="--hue: 180deg"` |
| `--k` | Scales the pattern size | `.size-sm`, `.size-lg`, `.size-xl` |
| `.tier-subtle` | Quiet, fine-grain patterns | `class="tex tex-dots tier-subtle"` |
| `.tier-medium` | Clearly defined patterns | `class="tex tex-hex tier-medium"` |
| `.tier-bold` | High-impact, oversized shapes | `class="tex tex-bands tier-bold"` |

## 📂 Library Structure

- **Subtle**: Safe for long-form text (dots, grid, paper).
- **Medium**: Perfect for cards and headers (hex, scales, waves).
- **Bold**: Best for hero sections and big titles (bands, sunburst, cubes).
- **Blends**: Advanced combinations of gradients, noise, and masks (aurora, mesh, holo).

## 📜 License
MIT License. 
Inspired by the works of Lea Verou and Temani Afif.
