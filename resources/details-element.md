# The `<details>` element

The HTML `details` element represents a disclosure widget. It can also be used as a part of an `accordion` widget.
The user experience more consistent, and generally better, in a number of areas:
- keyboard shortcuts and focus handling,
- exposure via ARIA to assistive technology, and
- integration with browser features such as find-in-page.

Exclusive Accordion:

```html
<details name="my-accordion">
  <summary>Summary 1</summary>
  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
</details>

<details name="my-accordion" open>
  <summary>Summary 2</summary>
  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
</details>
```

The `<details>` elements that are part of an exclusive accordion don't necessarily need to be siblings. They can be scattered across the document.

- [Real-World sidebar build with `<dialog>`/`<details`>](https://sport.tv2.dk/)
- [2024-07-08 — Comeau tweet on `<details>`: "🔥 It feels like magic"](https://x.com/JoshWComeau/status/1810327228477055133)
- [2024-07-15 — Animated exclusive accordions with CSS](https://x.com/jh3yy/status/1812966924294238558)
- [2024-09-25 — Open & Close Transitions with `<details>`](https://nerdy.dev/open-and-close-transitions-for-the-details-element)
- [#9951 — ::details-content vs details::part(content)](https://github.com/w3c/csswg-drafts/issues/9951#issuecomment-1997916879) - Exposing the shadow tree could lead to UAs being restricted in how they can change the component in the future
- [#9879 — Improve styling of `<details>`/`<summary>` elements](https://github.com/w3c/csswg-drafts/issues/9879#issuecomment-2121658036)

```css
details::details-content {
  --open-close-duration: 500ms;
  height: 0;
  overflow: hidden;
  transition: height var(--open-close-duration), content-visibility var(--open-close-duration) allow-discrete;
}

details[open]::details-content {
  height: calc-size(max-content);
}
```
