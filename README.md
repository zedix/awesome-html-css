# Awesome HTML & CSS (with super powers)

- [Interop 2024 Dashboard](https://webkit.org/blog/14955/the-web-just-gets-better-with-interop/)
- [CSS Wrapped 2023](https://developer.chrome.com/blog/css-wrapped-2023)

## HTML

### The `<dialog>` element

- [2023-01-26 — Use the dialog element (reasonably)](https://www.scottohara.me/blog/2023/01/26/use-the-dialog-element.html)

> [!TIP]
> IMO, the dialog element has reached the tipping point of generally being the better option for web developers who need to implement dialogs in their web pages. The number of accessibility requirements a developer needs to be aware of, and the level of effort to implement custom ARIA dialogs is now largely taken care of by browsers.

- [2022-04-13 — Building a dialog component](https://web.dev/building-a-dialog-component/)
- [2022-03-08 — A look at the dialog element's super powers](https://www.stefanjudis.com/blog/a-look-at-the-dialog-elements-super-powers/)
- [2022-02-08 — Replace JavaScript Dialogs With the New HTML Dialog Element](https://css-tricks.com/replace-javascript-dialogs-html-dialog-element/)

<img src="https://web.dev/static/articles/building/a-dialog-component/image/screenshot-chrome-devtoo-cbb3686684fa1_856.png?hl=fr" height="420" />


```html
<dialog open>
  <!-- This form will close its dialog when submitted -->
  <form method="dialog">
    <header>
      <h3>Dialog title</h3>
      <button onclick="this.closest('dialog').close('close')">✗</button>
    </header>
    <article>…</article>
    <footer>
      <menu>
        <button autofocus type="reset" onclick="this.closest('dialog').close('cancel')">Cancel</button>
        <button type="submit" value="confirm">Confirm</button>
      </menu>
    </footer>
  </form>
</dialog>
```

```css
dialog::backdrop {
  /* Styles and animations for the backdrop */
}
```

### The `<details>` element

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

The <details> elements that are part of an exclusive accordion don't necessarily need to be siblings. They can be scattered across the document.


### The `popover` attribute

The Popover API helps you build menus, selection, and tooltips. It supports:

- **Promotion to the top layer.** Popovers will appear on a separate layer above the rest of the page, so you don't have to play around with z-index.
- **Light-dismiss functionality.** Clicking outside of the popover area will close the popover and return focus.
- **Default focus management.** Opening the popover makes the next tab stop inside the popover.
- **Accessible keyboard bindings.** Hitting the esc key or double toggling will close the popover and return focus.
- **Accessible component bindings.** Connecting a popover element to a popover trigger semantically.

<img src="https://github.com/zedix/awesome-html-css/assets/27975/ecc6f4f7-1488-4a90-a349-6c0b2b2457a7" />

```html
<button popovertarget="actions">Actions</button>
<div role="menu" id="actions" popover>
  <button role="menuitem" tabindex=-1 autofocus>Edit</button>
  <button role="menuitem" tabindex=-1>Hide</button>
  <button role="menuitem" tabindex=-1>Delete</button>
</div>
```

- [Living Standard](https://html.spec.whatwg.org/multipage/popover.html#the-popover-attribute)
- [Popover API Demo](https://www.oidaisdes.org/popover-api-accessibility.en/)


### The `switch` attribute

```html
<input type="checkbox" switch />
```

<img src="https://github.com/zedix/awesome-html-css/assets/27975/f49d5d5d-5210-45f4-8b37-00514198e319" width="420" />

- [Switch Demo (Safari 14.3)](https://nt1m.github.io/html-switch-demos/)
  - [#9546](https://github.com/whatwg/html/pull/9546#issuecomment-1865595475)
  - [#9738](https://github.com/w3c/csswg-drafts/issues/9738)

### The `<selectmenu>` element

<img src="https://github.com/zedix/awesome-html-css/assets/27975/65d2c94c-6ec2-439a-9b7e-61f9eba431d4"  />

- [Open UI's <selectlist> demos](https://microsoftedge.github.io/Demos/selectlist/index.html)
- [2023-01-06 — Advanced Form Control Styling With Selectmenu And Anchoring API](https://www.smashingmagazine.com/2023/06/advanced-form-control-styling-selectmenu-anchoring-api/)

```html
<selectmenu class="my-custom-select">
  <div slot="button">
    <span behavior="selected-value" slot="selected-value"></span>
    <button behavior="button"></button>
  </div>
  <div slot="listbox">
    <div popover="auto" behavior="listbox">
       <option value="one">one</option>
       <option value="two">two</option>
    </div>
  </div>
</selectmenu>
```

### Appendix: all HTML elements (115)

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
- Proposed (-): [`<selectmenu>`](https://open-ui.org/components/selectlist/)

> [!NOTE]
> These last element landed in the HTML spec was the [`<search>`](https://www.scottohara.me/blog/2023/03/24/search-element.html) element, at March 24th 2023.


### HTML over the wire (instead of JSON)

- [The AHA Stack](https://ahastack.dev/)
- [htmx](https://htmx.org/)
- [Livewire](https://livewire.laravel.com/)
- [Hotwire](https://hotwired.dev/)
- [Alpine](https://github.com/alpinejs/alpine)


## CSS

### CSS Custom Functions & Mixins

- [Proposal: Custom CSS Functions & Mixins](https://github.com/w3c/csswg-drafts/labels/css-mixins)

### CSS Anchor Position API

- [Explainer: CSS Anchor Positioning](https://xiaochengh.github.io/Explainers/css-anchor-position/explainer.html)
- [Spec: CSS Anchor Positioning (Editor’s Draft)](https://drafts.csswg.org/css-anchor-position-1/)
  - [Tracking bug for implementation of Anchor Positioning feature](https://issues.chromium.org/issues/40059176)
  - [WebKit Position](https://github.com/WebKit/standards-positions/issues/167#issuecomment-1708871010)
  - [Mozilla Position](https://github.com/mozilla/standards-positions/issues/794)
- [Tether elements to each other with CSS anchor positioning](https://developer.chrome.com/blog/tether-elements-to-each-other-with-css-anchor-positioning) by Jhey Tompkins (one of the spec editors)
- [2023-03-15 — Future CSS: Anchor Positioning](https://kizu.dev/anchor-positioning-experiments/)
- [The `anchor` attribute](https://github.com/whatwg/html/pull/9144)

```css
.anchor {
  anchor-name: --my-anchor;
}

.tooltip {
  anchor-default: --my-anchor;
  position-fallback: --top-to-bottom;
}

@position-fallback --top-to-bottom {
  @try {
    bottom: anchor(top);
    left: anchor(center);
  }

  @try {
    top: anchor(bottom);
    left: anchor(center);
  }
}
```

## CSS Scroll-Driven Animations

- [CSS Scroll-triggered Animations with Style Queries](https://ryanmulligan.dev/blog/scroll-triggered-animations-style-queries/)
- [Scroll-Driven Animations: You want overflow: clip, not overflow: hidden](https://www.bram.us/2024/02/14/scroll-driven-animations-you-want-overflow-clip-not-overflow-hidden/)

## CSS Custom Highlight API

- [Custom Highlight API](https://www.bram.us/2024/02/18/custom-highlight-api-for-syntax-highlighting/)

```css
::highlight(example) {
	color: hotpink;
}
```
