# CSS `if()` notation (inline conditionals on custom properties / self-styling feature)

- [CSS Values and Units Module Level 5](https://www.w3.org/TR/css-values-5/)
- [#10064 [css-values-5] What is the MVP for inline conditionals on custom properties? 🔥](https://github.com/w3c/csswg-drafts/issues/10064)
- [Chrome Status: CSS if() function](https://chromestatus.com/feature/6313805904347136?gate=5132766385274880)

```css
zx-tag {
  /* if(condition(): foo; else: bar) */
  background-color: if(
    (--variant: success): green;
    else: white;
  );
}
```
