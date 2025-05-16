## CSS `ident()`

> The ident() function may be used to construct CSS identifiers dynamically, e.g. the concatenation of a string part and an integer part.

```css
.item {
  /* vtl-1, vtl-2, vtl-3, … */
  view-timeline-name: ident("vtl-" sibling-index());
}
```

```css
.card[id] {
	/* E.g. card1, card2, card3, … */
	--id: attr(id);

	view-transition-name: ident(var(--id));
	view-transition-class: card;

	h1 {
		/* E.g. card1-title, card2-title, card3-title, … */
		view-transition-name: ident(var(--id) "-title");
		view-transition-class: card-title;
	}
}
```

- https://x.com/bramus/status/1922551283585614159
