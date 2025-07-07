# CSS `oklch()`

The `oklch()` functional notation expresses a given color in the Oklab color space.

```css
/* Absolute values */
oklch(40.1% 0.123 21.57)
oklch(59.69% 0.156 49.77)
oklch(59.69% 0.156 49.77 / .5)

/* Relative values */
oklch(from green l c h / 0.5)
oklch(from #0000FF calc(l + 0.1) c h)
oklch(from hsl(180 100% 50%) calc(l - 0.1) c h)
oklch(from var(--aColor) l c h / calc(alpha - 0.1))
```

- [2025-05-28 — Exploring the OKLCH ecosystem and its tools](https://evilmartians.com/chronicles/exploring-the-oklch-ecosystem-and-its-tools)
