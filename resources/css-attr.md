# CSS `attr()` new capabilities

```html
<ui-rating data-rating="4.5"></ui-rating>
```

```css
ui-rating {
  --percent-fill: calc(attr(data-rating type(<number>)) * 20%);
  background: linear-gradient(to right, gold var(--percent-fill), transparent var(--percent-fill));
}
```

- [2025-01-21 — New capabilities for attr()](https://una.im/advanced-attr/)
