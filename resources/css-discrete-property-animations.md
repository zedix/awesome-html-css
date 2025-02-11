## CSS Discrete Property Animations

Ability to animate discrete animations, such as animating to and from `display: none`.

```css
.card {
  transition: opacity 0.25s, display 0.25s;
  transition-behavior: allow-discrete; /* Note: be sure to write this after the shorthand */
}

.card.fade-out {
  opacity: 0;
  display: none;
}
```
