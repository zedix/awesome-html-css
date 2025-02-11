# Awesome HTML & CSS (with super powers)

- [Web Platform Explorer](https://web-platform-dx.github.io/web-features-explorer/)
- [Web Platform Baseline](https://web.dev/baseline)
- [Web Platform Status](https://webstatus.dev/)

> [!TIP]
> Stop writing unnecessary, heavy, thread-blocking JavaScript — [Una Kravets](https://una.github.io/better-faster-stronger-web-ui/)

> [!TIP]
> CSS is now the most powerful design tool for the Web — [Matthias Ott](https://youtu.be/su6WA0kUUJE?t=340)

> [!TIP]
> With all the new web features right on their way (view-transitions, @​starting-style, calc-size(), speculation rules, style and container queries, relative color syntax, ... the list goes on and on), it's time to face it... 🫣👇 — <a href="https://x.com/stefanjudis/status/1801176094243991995">Stefan Judis</a> <p><img src="https://pbs.twimg.com/media/GP8PXZBXsAAnFP_?format=jpg&name=large" height="280"/></p>

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
- Proposed (-): [`<selectedcontent>`](https://una.im/select-updates/)

> [!NOTE]
> These last element landed in the HTML spec was the [`<search>`](https://www.scottohara.me/blog/2023/03/24/search-element.html) element, at March 24th 2023.


### HTML over the wire (instead of JSON)

- [The AHA Stack](https://ahastack.dev/)
- [htmx](https://htmx.org/)
- [Livewire](https://livewire.laravel.com/)
- [Hotwire](https://hotwired.dev/)
- [Alpine](https://github.com/alpinejs/alpine)


## CSS

- [CSS Scroll Animations](./resources/css-scroll-animations.md)
- [CSS View Transitions](./resources/css-views-transitions.md)
- [CSS `if()` notation](./resources/css-if-notation.md)
- [CSS Anchor Positioning](./resources/css-anchor-positioning.md)


```
calc()
var()
clamp()
fit-content(), repeat()
min(), max()
attr()
env()
color(), rgb(), hsl(), oklch()
circle(), polygon()
url()
translate(), scale(), rotate()
matrix()
invert()
sin(), cos(), tan(), pow(), hypot(), log()
steps()
scroll(), scroll-state(), view()
```

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


### CSS Custom Functions & Mixins

- [Proposal: Custom CSS Functions & Mixins](https://github.com/w3c/csswg-drafts/labels/css-mixins)



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

## CSS scroll-state() container queries: the `stuck` query

- [Explainer](https://drafts.csswg.org/css-contain-4/scroll_state_explainer.html)

```css
#sticky {
  container-name: main-nav;
  container-type: sticky;
  position: sticky;
  top: 0;
  height: 100px;
}

@container main-nav scroll-state(stuck: top) {
   box-shadow: var(--shadow-5);
   border-radius: var(--radius-3);
   margin: var(--size-5);
 }
```


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
- [CSS Tips](https://css-tip.com/)
- [Transition to `height: auto` & `display: none` Using Pure CSS](https://blog.css-weekly.com/transition-to-height-auto-display-none-using-pure-css)
- [CSS box-decoration-break](https://12daysofweb.dev/2024/css-box-decoration-break/)
- [A standards first web framework](https://nuejs.org/blog/standards-first-web-framework/)
- [attr() is getting an upgrade](https://una.im/advanced-attr/)
- [New Front-End Features In 2025](https://www.smashingmagazine.com/2024/12/new-front-end-features-for-designers-in-2025/)
- [CSS Wrapped 2024](https://chrome.dev/css-wrapped-2024/)

## UI Kit

- `<dialog>`: modal content, sidebars
- `<details>`: accordions, disclosures
- `popover`: menus, custom toast notifications, content pickers
- `anchor`: tooltips
