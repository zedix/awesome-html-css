# CSS Mixins & Functions

- [2025-09-30 — A custom --light-dark() function in CSS that works with any type of value (not just colors!) in just 3 LOC](https://www.bram.us/2025/09/30/css-custom-light-dark/)
- [2025-08-13 — 5 Useful CSS functions using the new @function rule](https://una.im/5-css-functions/)
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
