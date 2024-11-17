# Awesome HTML & CSS (with super powers)

- [Web Platform Explorer](https://web-platform-dx.github.io/web-features-explorer/)
- [Web Platform Baseline](https://web.dev/baseline)
- [Web Platform Status](https://webstatus.dev/)

> [!TIP]
> Stop writing unnecessary, heavy, thread-blocking JavaScript — Una Kravets

> [!TIP]
> CSS is now the most powerful design tool for the Web — [Matthias Ott](https://youtu.be/su6WA0kUUJE?t=340)

> [!TIP]
> With all the new web features right on their way (view-transitions, @​starting-style, calc-size(), speculation rules, style and container queries, relative color syntax, ... the list goes on and on), it's time to face it... 🫣👇 — <a href="https://x.com/stefanjudis/status/1801176094243991995">Stefan Judis</a>

<img src="https://pbs.twimg.com/media/GP8PXZBXsAAnFP_?format=jpg&name=large" height="280" />

## HTML

- [The `<dialog>` element](./resources/dialog-element.md)
- [The `<details>` element](./resources/details-element.md)
- [The customizable `<select>` element](./resources/customizable-select-element.md)
- [The `popover` attribute](./resources/popover-attribute.md)
- [The `command` attribute](./resources/invoker-commands-api.md)
- [The `focusgroup` attribute](./resources/focusgroup-attribute.md)
- [The `switch` attribute](./resources/switch-attribute.md)
- [The `CloseWatcher` api](./resources/closewatcher-api.md)

### All HTML elements (115)

- Document element (1): `<html>`
- Document metadata (6): `<head>`, `<title>`, `<base>`, `<link>`, `<meta>`, `<style>`,
- Sections (15): `<body>`, `<article>`, `<section>`, `<nav>`, `<aside>`, `<h1-6>`, `<hgroup>`, `<header>`, `<footer>`, `<address>`
- Grouping content (16): `<p>`, `<hr>`, `<pre>`, `<blockquote>`, `<ol>`, `<ul>`, `<menu>`, `<li>`, `<dl>`, `<dt>`, `<dd>`, `<figure>`, `<figcaption>`, `<main>`, `<search>`, `<div>`
- Text-level semantics (29): `<a>`, `<em>`, `<strong>`, `<small>`, `<s>`, `<cite>`, `<q>`, `<dfn>`, `<abbr>`, `<ruby>`, `<rt>`, `<rp>`, `<data>`, `<time>`, `<code>`, `<var>`, `<samp>`, `<kbd>`, `<sub>`, `<sup>`, `<i>`, `<b>`, `<u>`, `<mark>`, `<bdi>`, `<bdo>`, `<span>`, `<br>`, `<wbr>`
- Edits (2): `<ins>`, `<del>`
- Embedded content (13): `<picture>`, `<source>`, `<img>`, `<iframe>`, `<embed>`, `<object>`, `<video>`, `<audio>`, `<track>`, `<map>`, `<area>`, `<math>`, `<svg>`
- Tabular data (10): `<table>`, `<caption>`, `<colgroup>`, `<col>`, `<tbody>`, `<thead>`, `<tfoot>`, `<tr>`, `<td>`, `<th>`
- Forms (14): `<form>`, `<label>`, `<input>`, `<button>`, `<select>`, `<datalist>`, `<optgroup>`, `<option>`, `<textarea>`, `<output>`, `<progress>`, `<meter>`, `<fieldset>`, `<legend>`
- Interactive elements (3): [`<details>`](https://html.spec.whatwg.org/multipage/interactive-elements.html#the-details-element), `<summary>`, [`<dialog>`](https://html.spec.whatwg.org/multipage/interactive-elements.html#the-dialog-element)
- Custom elements (2): `<template>`, `<slot>`
- Scripting (3): `<script>`, `<noscript>`,`<canvas>`
- Experimental (1): `<portal>`
- Proposed (-): [`<selectedoption>`](https://open-ui.org/components/selectlist/)

> [!NOTE]
> These last element landed in the HTML spec was the [`<search>`](https://www.scottohara.me/blog/2023/03/24/search-element.html) element, at March 24th 2023.


### HTML over the wire (instead of JSON)

- [The AHA Stack](https://ahastack.dev/)
- [htmx](https://htmx.org/)
- [Livewire](https://livewire.laravel.com/)
- [Hotwire](https://hotwired.dev/)
- [Alpine](https://github.com/alpinejs/alpine)


## CSS

### CSS `subgrid`

- [CSS Subgrid](https://web.dev/articles/css-subgrid)
- [CSS Subgrid to design advanced layouts](https://blog.logrocket.com/using-css-subgrid-design-advanced-layouts/)

### CSS `color-mix()`

- [2024-03-08 — Creating color palettes with the CSS color-mix() function](https://developer.mozilla.org/en-US/blog/color-palettes-css-color-mix/)

### CSS Container Queries (`container-type`, `container-name`, `@container`)

### CSS Style Queries

```css
figure {
  container-name: figure;
  --featured: true;
}

@container figure style(--featured: true) {
  figcaption {
    /* Custom styling */
  }
}
```

- [Container Style Query Explainer](https://css.oddbird.net/rwd/style/explainer/) by Miriam Suzanne
- [CSS Style Queries Use Cases](https://ishadeed.com/article/css-container-style-queries/)
- [CSS Style Container Queries (custom properties) #828](https://github.com/web-platform-tests/interop/issues/828)
- [#10744 Allow applying style rules to the container itself](https://github.com/w3c/csswg-drafts/issues/10744)

### CSS `if()` notation (inline conditionals on custom properties / self-styling feature)

- [CSS Values and Units Module Level 5](https://www.w3.org/TR/css-values-5/)
- [#10064 [css-values-5] What is the MVP for inline conditionals on custom properties? 🔥](https://github.com/w3c/csswg-drafts/issues/10064)

```css
zx-tag {
  /* if(condition(): foo; else: bar) */
  background-color: if(
    (--variant: success): green;
    else: white;
  );
}
```

### CSS Custom Functions & Mixins

- [Proposal: Custom CSS Functions & Mixins](https://github.com/w3c/csswg-drafts/labels/css-mixins)

### CSS Anchor Position API

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

<img src="https://drafts.csswg.org/css-anchor-position-1/images/inset-area-example.png" width="420" />


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

## CSS Scroll-Driven Animations (`view-timeline`, `animation-timeline`, `view()`)

- [CSS Scroll-triggered Animations with Style Queries](https://ryanmulligan.dev/blog/scroll-triggered-animations-style-queries/)
- [Scroll-Driven Animations: You want overflow: clip, not overflow: hidden](https://www.bram.us/2024/02/14/scroll-driven-animations-you-want-overflow-clip-not-overflow-hidden/)
- [Demo: show off Scroll-driven Animations](https://scroll-driven-animations.style/)
- [Demo: CSS-Only Sticky CTA](https://x.com/jh3yy/status/1765166342502559923?s=20)
- [Real World examples](https://x.com/Una/status/1767237843330433298?s=20)

```css
@keyframes slide-left {
    from { transform: scale(0.7); }
    to   { transform: scale(1); }
}
.scroll-animate-slide-left {
    transform-origin: top right;
    animation: slide-left ease-out both;
    animation-timeline: view(block -64px);
    animation-range: entry 0% entry 50%;
}
```

## CSS Custom Highlight API

- [Custom Highlight API](https://www.bram.us/2024/02/18/custom-highlight-api-for-syntax-highlighting/)

```css
::highlight(example) {
  color: hotpink;
}
```

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

## CSS View Transitions

- [2024-02-24 — View transitions: Handling aspect ratio changes](https://jakearchibald.com/2024/view-transitions-handling-aspect-ratio-changes/)
- [2024-11-17 — Bramus - Supercharge Web UX with View Transitions!](https://www.youtube.com/watch?v=pMaAHpKFEAo) - React Brussels 2024

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

### CSS Tips

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

## Resources

- [12 Days of Web](https://12daysofweb.dev/)
- [Interop 2024 Dashboard](https://webkit.org/blog/14955/the-web-just-gets-better-with-interop/)
- [CSS Wrapped 2023](https://developer.chrome.com/blog/css-wrapped-2023)
- [New to the web platform](https://web.dev/blog)
- [Better, Faster, Stronger Web UI](https://una.github.io/better-faster-stronger-web-ui/) by Una Kravets
- [Modern CSS patterns in Campfire](https://dev.37signals.com/modern-css-patterns-and-techniques-in-campfire/)
- [Write better CSS with modern CSS](https://css-tip.com/better-modern-css/)
- [The latest in Web UI (Google I/O ‘24)](https://www.youtube.com/watch?v=_-6LgEjEyzE)
- [Adam Argyle blog](https://nerdy.dev/)
- [Transition to `height: auto` & `display: none` Using Pure CSS](https://blog.css-weekly.com/transition-to-height-auto-display-none-using-pure-css)


## UI Kit

- `<dialog>`: modal content, sidebars
- `<details>`: accordions, disclosures
- `popover`: menus, custom toast notifications, content pickers
- `anchor`: tooltips
