# CSS `shape()` function

> Chrome 135 and Safari 18.4 support CSS shape(), which will be the solution for responsive SVG paths.

```css
clip-path: shape(from right center,
    line to bottom center,
    arc to top center of 50% 50% cw,
    line to right center);
```

- [The `shape()` Function](https://drafts.csswg.org/css-shapes-2/#shape-function)
- [Demo](https://codepen.io/yisi/pen/vEYGrQv)
- [`shape()` in Safari 18.4](https://webkit.org/blog/16574/webkit-features-in-safari-18-4)
- [Demo animating corner-shapes (Chrome Canary 137.0.7109.0+)](https://codepen.io/noamr/pen/KwKEjdY)
