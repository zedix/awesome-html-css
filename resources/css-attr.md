# CSS `attr()`

```html
<div data-width="100px" data-color="green"></div>
```

```css
div {
  width: attr(data-width type(<length>));
  background: attr(data-color type(<color>));
}
```

- [2025-02-17 — The attr() function in CSS now supports types](https://www.amitmerchant.com/attr-function-types-css/#how-to-use-attr-with-types)
