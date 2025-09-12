# Local Fonts Setup - OUSSOUD Football Website

## Overview

This folder contains locally hosted fonts to improve website performance and ensure consistent typography across all devices.

## Fonts Included

### 1. **Poppins Font Family**

- **Weights:** 300 (Light), 400 (Regular), 500 (Medium), 600 (SemiBold), 700 (Bold), 800 (ExtraBold)
- **Usage:** Primary font for headings, navigation, and general UI elements
- **Location:** `./poppins/`

### 2. **Urbanist Font Family**

- **Weights:** 400 (Regular), 500 (Medium), 600 (SemiBold), 700 (Bold)
- **Usage:** Secondary font for match details, scores, and specific content areas
- **Location:** `./urbanist/`

### 3. **Roboto Font Family**

- **Weights:** 300 (Light), 400 (Regular), 500 (Medium), 700 (Bold), 900 (Black)
- **Usage:** Fallback font and specific text elements
- **Location:** `./roboto/`

## File Structure

```
assets/fonts/
├── fonts.css              # Main font declarations file
├── README.md              # This documentation
├── poppins/
│   ├── poppins-light.woff2
│   ├── poppins-regular.woff2
│   ├── poppins-medium.woff2
│   ├── poppins-semibold.woff2
│   ├── poppins-bold.woff2
│   └── poppins-extrabold.woff2
├── urbanist/
│   ├── urbanist-regular.woff2
│   ├── urbanist-medium.woff2
│   ├── urbanist-semibold.woff2
│   └── urbanist-bold.woff2
└── roboto/
    ├── roboto-light.woff2
    ├── roboto-regular.woff2
    ├── roboto-medium.woff2
    ├── roboto-bold.woff2
    └── roboto-black.woff2
```

## Implementation

### HTML (index.html)

- **Font Preloading:** Critical fonts are preloaded for faster rendering
- **CSS Link:** `fonts.css` is loaded before other stylesheets
- **Font Loading Script:** JavaScript optimization for smooth font rendering

### CSS (css/custom.css)

- **CSS Custom Properties:** Font stacks defined as CSS variables
- **Fallback Fonts:** Proper fallback chains for all platforms
- **Font Loading States:** FOUT prevention and loading optimization

## Performance Benefits

1. **Faster Loading:** No external font requests to Google Fonts
2. **Better Privacy:** No external tracking or data collection
3. **Offline Support:** Fonts work without internet connection
4. **Consistency:** Guaranteed font availability across all users
5. **Control:** Full control over font loading and rendering

## CSS Variables Available

```css
--font-primary: "Poppins", "Roboto", -apple-system, BlinkMacSystemFont, "Segoe UI",
  "Helvetica Neue", Arial, sans-serif;
--font-secondary: "Urbanist", "Roboto", -apple-system, BlinkMacSystemFont, "Segoe UI",
  "Helvetica Neue", Arial, sans-serif;
--font-mono: "Roboto Mono", "SF Mono", Monaco, Consolas, "Liberation Mono",
  "Courier New", monospace;
```

## Usage Examples

```css
/* Using CSS Variables (Recommended) */
.heading {
  font-family: var(--font-primary);
}

.score-display {
  font-family: var(--font-secondary);
}

/* Direct Font Reference */
.brand-name {
  font-family: "Poppins", sans-serif;
  font-weight: 700;
}

.match-details {
  font-family: "Urbanist", sans-serif;
  font-weight: 600;
}
```

## Maintenance

- **File Format:** WOFF2 (optimal compression and browser support)
- **Unicode Range:** Optimized for Latin characters and common symbols
- **Font Display:** `swap` for optimal loading experience
- **Preloading:** Most critical fonts are preloaded for performance

## Browser Support

- **Chrome:** Full support
- **Firefox:** Full support
- **Safari:** Full support
- **Edge:** Full support
- **IE 11:** Fallback fonts only

---

_Last Updated: September 2025_
_Total Font Files: 15_
_Total Size: ~150KB (compressed)_
