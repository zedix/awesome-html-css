# CSS Typed `attr()` new capabilities

```html
<ui-rating data-rating="4.5"></ui-rating>
```

```css
ui-rating {
  --percent-fill: calc(attr(data-rating type(<number>)) * 20%);
  background: linear-gradient(to right, gold var(--percent-fill), transparent var(--percent-fill));
}
```

- [2025-04-03 — Exploring the modern attr() in CSS](https://ishadeed.com/article/modern-attr/)
- [2025-03-25 — Custom progress element using attr()](https://css-tip.com/custom-progress/)
- [2025-02-25 — How to Use attr() in CSS for Columns, Colors, and Font-Size](https://frontendmasters.com/blog/how-to-use-attr-in-css-for-columns-colors-and-font-size/)
- [2025-01-21 — New capabilities for attr()](https://una.im/advanced-attr/)
- [Can I Use —  attr() function for all properties](https://caniuse.com/css3-attr)
