# CSS Tips

- [Safe/unsafe alignment in CSS flexbox](https://www.stefanjudis.com/today-i-learned/safe-unsafe-alignment-in-css-flexbox/)

```css
.container {
  display: flex;
  flex-direction: column;
  align-items: safe center;
  width: 38%;
}
```

- [The Complex But Awesome CSS border-image Property](https://www.smashingmagazine.com/2024/01/css-border-image-property/)

```css
.overlay {
  border-image: fill 0 linear-gradient(#0003, #000);
}
```


- [Dynamic mask using a progressive CSS scroll-driven animation](https://x.com/jh3yy/status/1918118919614665086)
  - [Codepen demo](https://codepen.io/jh3y/pen/OPPQvxR)

```css
input {
  animation: in;
  animation-timeline: scroll(self inline);
  animation-range: 0 6ch;
  mask-position: 0 0;
}
@keyframes in { 0% { mask-position: -6ch 0; }}
```

### Demos

- [CSS Number Animation](https://codepen.io/jh3y/pen/gbbYZEz)


## CSS Handy (Old) Things

- [:any-link](https://developer.mozilla.org/en-US/docs/Web/CSS/:any-link)
- :empty
- :first-child
- :focus-visible
- :focus-within
- accent-color
- [aspect-ratio](https://developer.mozilla.org/en-US/docs/Web/CSS/aspect-ratio)
- [backdrop-filter](https://developer.mozilla.org/en-US/docs/Web/CSS/backdrop-filter)
- border-image
- caret-color
- columns
- [drop-shadow()](https://developer.mozilla.org/fr/docs/Web/CSS/filter-function/drop-shadow)
- [fit-content()](https://developer.mozilla.org/en-US/docs/Web/CSS/fit-content_function)
- gap
- inset
- list-style
- matrix3d()
- object-fit
- [overscroll-behavior](https://developer.mozilla.org/en-US/docs/Web/CSS/overscroll-behavior)
- [scroll-margin](https://developer.mozilla.org/en-US/docs/Web/CSS/scroll-margin)
- [scroll-snap](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_scroll_snap)
- @supports (hover)


[Above list from Adam Argyle](https://x.com/KevinJPowell/status/1766488365904392399?s=20)


## Courses

- [The Craft of UI](https://www.craftofui.dev/)

## Resources

- [Good vs Great Animations](https://emilkowal.ski/ui/good-vs-great-animations)
