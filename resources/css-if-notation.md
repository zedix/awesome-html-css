# CSS `if()` notation (inline conditionals on custom properties / self-styling feature)

![image](https://github.com/user-attachments/assets/4ce69b88-3a55-4ddb-8232-814579b00864)

- [CSS Values and Units Module Level 5](https://drafts.csswg.org/css-values-5/#if-notation)
- [#10064 [css-values-5] What is the MVP for inline conditionals on custom properties? 🔥](https://github.com/w3c/csswg-drafts/issues/10064)
- [Chrome Status: CSS if() function](https://chromestatus.com/feature/6313805904347136?gate=5132766385274880)
- [Chrome Intent to Prototype: CSS if() function](https://groups.google.com/a/chromium.org/g/blink-dev/c/ySEBHgVlhBM/m/zO5OcgtWEgAJ)
- [if() in CSS combined with other modern stuff](https://x.com/ChallengesCss/status/1909713366278369785)

```css
zx-tag {
  /* if(media(<media-condition>): foo; else: bar) */
  /* if(style(<style-query>): foo; else: bar) */
  /* if(<supports-condition>): foo; else: bar) */
  background-color: if(
    style(--variant: success): green;
    else: white;
  );
}
```
