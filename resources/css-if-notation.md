# CSS `if()` notation (inline conditionals on custom properties / self-styling feature)

<img src="https://lea.verou.me/blog/2024/css-conditionals-now/images/callouts.png" height="340" />

```css
.callout {
	border-color: if(
		style(--variant: success) ? var(--color-success-30) :
		style(--variant: danger) ? var(--color-danger-30) :
		/* (other variants) */
		var(--color-neutral-30)
	);
	background-color: if(
		style(--variant: success) ? var(--color-success-95) :
		style(--variant: danger) ? var(--color-danger-95) :
		/* (other variants) */
		var(--color-neutral-95)
	);

	@container (style(--variant: success)) {
		&::before {
			content: var(--icon-success);
			color: var(--color-success-05);
		}
	}

	/* (other variants) */
}
```

![image](https://github.com/user-attachments/assets/4ce69b88-3a55-4ddb-8232-814579b00864)

- [Intent to Ship: Short-circuiting var(), attr()](https://groups.google.com/a/chromium.org/g/blink-dev/c/VqnJ6-4vGFs/m/OzblXmg7AAAJ)
- [CSS Values and Units Module Level 5](https://drafts.csswg.org/css-values-5/#if-notation)
- [#10064 [css-values-5] What is the MVP for inline conditionals on custom properties? 🔥](https://github.com/w3c/csswg-drafts/issues/10064)
- [Chrome Status: CSS if() function](https://chromestatus.com/feature/6313805904347136?gate=5132766385274880)
- [Chrome Intent to Prototype: CSS if() function](https://groups.google.com/a/chromium.org/g/blink-dev/c/ySEBHgVlhBM/m/zO5OcgtWEgAJ)
- [if() in CSS combined with other modern stuff](https://x.com/ChallengesCss/status/1909713366278369785)
- [Inline conditionals in CSS?](https://lea.verou.me/blog/2024/css-conditionals/)
- [[css-values-5] What is the MVP for inline conditionals on custom properties? #10064](https://github.com/w3c/csswg-drafts/issues/10064)

> The major author pain point remains unsolved, and authors have to resort to HTML attributes instead (as explained in [#5624](https://github.com/w3c/csswg-drafts/issues/5624)).


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
