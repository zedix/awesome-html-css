# CSS Mixins & Functions

- [2025-03-26 — CSS Mixins are ready for experimentation](https://nerdy.dev/css-mixins-ready-for-experimentation)
- [Official spec](https://drafts.csswg.org/css-mixins/)
- [Intent to Ship: CSS Custom Functions (@function)](https://groups.google.com/a/chromium.org/g/blink-dev/c/bvi4D7eD7wI/m/djYVLu6OAwAJ)
- [CSS Mixins & Functions Explainer](https://css.oddbird.net/sasslike/mixins-functions/)
- [Proposal: Custom CSS Functions & Mixins](https://github.com/w3c/csswg-drafts/labels/css-mixins)
- [Custom CSS Custom Functions + Nested Style Queries: --light-dark()](https://codepen.io/bramus/pen/xbxGOdw)

```css
@mixin --box {
  aspect-ratio: 1;
  inline-size: 100px;
  block-size: 100px;
}

.box {
  @apply --box;
}
```


```css
@function --light-dark(--light, --dark) {
   result: var(--light);
   @media (prefers-color-scheme: dark) {
     result: var(--dark);
   }
}

div {
  background-image: --light-dark(black-logo.png, white-logo.png);
}
```
