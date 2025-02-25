# CSS Custom Functions (aka Mixins)

- [Intent to Ship: CSS Custom Functions (@function)](https://groups.google.com/a/chromium.org/g/blink-dev/c/bvi4D7eD7wI/m/djYVLu6OAwAJ)
- [Proposal: Custom CSS Functions & Mixins](https://github.com/w3c/csswg-drafts/labels/css-mixins)
- [Custom CSS Custom Functions + Nested Style Queries: --light-dark()](https://codepen.io/bramus/pen/xbxGOdw)

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
