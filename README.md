# US Time Zone Dashboard

A minimal, dark-mode web dashboard displaying real-time clocks for the four major CONUS time zones.

## Features

- **4 timezone columns** — Pacific, Mountain, Central, and Eastern, each color-coded
- **Dual time format** — 12-hour (large) and 24-hour (smaller, dimmed) in each column
- **Local time bar** — top bar shows your browser's local time with seconds
- **UTC time bar** — bottom bar shows UTC with seconds in Amazon orange
- **Responsive layout** — scales to fill the browser window using fluid typography (`clamp`/`vmin` units)
- **Dark mode** — designed for low-light environments

## Usage

No build step, dependencies, or server required — it's a single self-contained HTML file.

## Layout

```
┌──────────────────────────────────────────┐
│           Local Time (with seconds)      │
├──────────┬──────────┬──────────┬─────────┤
│          │          │          │         │
│ Pacific  │ Mountain │ Central  │ Eastern │
│  12-hr   │  12-hr   │  12-hr   │  12-hr  │
│  24-hr   │  24-hr   │  24-hr   │  24-hr  │
│          │          │          │         │
├──────────┴──────────┴──────────┴─────────┤
│            UTC Time (with seconds)       │
└──────────────────────────────────────────┘
```

## Color Scheme

| Element  | Color                        |
|----------|------------------------------|
| Pacific  | Purple (`#c084fc`)           |
| Mountain | Orange (`#f59e42`)           |
| Central  | Green (`#34d399`)            |
| Eastern  | Blue (`#60a5fa`)             |
| UTC bar  | Amazon Orange (`#ff9900`)    |
| Local bar| White (`#e0e0e0`)            |
| Background | Near-black (`#0f0f13`)     |

## Fonts

The dashboard uses Amazon Ember as the primary font with system fallbacks:

- **UI text**: Amazon Ember → SF Pro Display → system default
- **Time bars**: Amazon Ember Mono → SF Mono → Fira Code → monospace

Amazon Ember will render if installed locally; otherwise the fallback fonts are used.

## Browser Compatibility

Works in all modern browsers (Chrome, Firefox, Safari, Edge). Requires JavaScript enabled and `Intl.DateTimeFormat` support for timezone detection.
