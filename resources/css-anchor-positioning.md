# CSS Anchor Positioning

<img src="https://github.com/zedix/awesome-html-css/assets/27975/ac8ba033-5070-41eb-9a56-2a9a11a5095a" width="420" />


- [2021-03-06 — First Proposal by Melanie Richards (Microsoft)](https://melanie-richards.com/blog/anchored-positioning/)
- [2023-03-15 — Future CSS: Anchor Positioning](https://kizu.dev/anchor-positioning-experiments/)
- [2023-06-29 — First Working Draft](https://www.w3.org/TR/css-anchor-position-1/)
- [2023-12-14 — Anchor Positioning ⭐](https://12daysofweb.dev/2023/anchor-positioning/)
- [2024-02-09 — Editor’s Draft](https://drafts.csswg.org/css-anchor-position-1/)
- [2024-04-12 — Chromium Intent to Ship: CSS Anchor Positioning](https://groups.google.com/a/chromium.org/g/blink-dev/c/jGTYNuidPRs/m/-jB4agJ7AAAJ)
  - [Una's anchor-tool](http://anchor-tool.com/)
  - [Una's bunch of demos](https://codepen.io/collection/ExkRWw?grid_type=grid)
  - [`inset-area` demo exploration](https://codepen.io/kizu/pen/zYMmVJd)
  - [csswg-drafts > css-anchor-position-1](https://github.com/w3c/csswg-drafts/labels/css-anchor-position-1)
  - [Chromium tracking bug](https://issues.chromium.org/issues/40059176)
  - [Mozilla tracking bug](https://bugzilla.mozilla.org/show_bug.cgi?id=1838746)
  - [Explainer: CSS Anchor Positioning](https://xiaochengh.github.io/Explainers/css-anchor-position/explainer.html)
  - [#9663 Better handle an inset-area edge case](https://github.com/w3c/csswg-drafts/issues/9663)
  - [Tracking bug for implementation of Anchor Positioning feature](https://issues.chromium.org/issues/40059176)
  - [WebKit Position](https://github.com/WebKit/standards-positions/issues/167#issuecomment-1708871010)
  - [Mozilla Position](https://github.com/mozilla/standards-positions/issues/794)
- [Tether elements to each other with CSS anchor positioning](https://developer.chrome.com/blog/tether-elements-to-each-other-with-css-anchor-positioning) by Jhey Tompkins (one of the spec editors)
- [2024-11-18 — Anchor Positioning Is Disruptive](https://www.oddbird.net/2024/11/18/anchor-position-yearbook/)

```css
.anchor {
  anchor-name: --my-anchor;
}

.tooltip {
  /* Fixpos means we don’t need to worry about
     containing block relationships;
     the tooltip can live anywhere in the DOM. */
  position: fixed;

  /* All the anchoring behavior will default to
     referring to the --tooltip anchor. */
  position-anchor: --tooltip;

  /* Align the tooltip’s bottom to the top of the anchor;
     this also defaults to horizontally center-aligning
     the tooltip and the anchor (in horizontal writing modes). */
  inset-area: block-start;

  /* Automatically swap if this overflows the window
    so the tooltip’s top aligns to the anchor’s bottom
    instead. */
  position-try: flip-block;

  /* Prevent getting too wide */
  max-inline-size: 20em;
}
```

Update April 2024: here is all the [code](https://codepen.io/una/pen/YzgOoLb) you need to get a [basic anchor](https://x.com/Una/status/1777810507849671036) now:

```css
#my-tooltip {
  /*  Set the bottom of the anchored element (tooltip) to the top of the anchoring element  */
  bottom: calc(anchor(top));
  /*  If can't fit it in the screen anymore, flip the anchored element in the block direction */
  position-try-options: flip-block;
  /*  Center the anchor with justification  */
  justify-self: anchor-center;
}
```

- [3 lines of CSS to make your tooltips/menus stay in view 🤯](https://x.com/jh3yy/status/1778946758510260727)

```css
[popover] {
  top: anchor(top);
  left: anchor(right);
  position-try-options: flip-block, flip-inline;
}
```
