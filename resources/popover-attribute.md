# The `popover` attribute

> [!NOTE]
> Built-in accessibility via keyboard behavior, tab focus management, top-layer support, and (optional) light-dismiss

The Popover API helps you build menus, selection, and tooltips. It supports:

- **Promotion to the top layer.** Popovers will appear on a separate layer above the rest of the page, so you don't have to play around with z-index.
- **Light-dismiss functionality.** Clicking outside of the popover area will close the popover and return focus.
- **Default focus management.** Opening the popover makes the next tab stop inside the popover.
- **Accessible keyboard bindings.** Hitting the esc key or double toggling will close the popover and return focus.
- **Accessible component bindings.** Connecting a popover element to a popover trigger semantically.

<img src="https://github.com/zedix/awesome-html-css/assets/27975/ecc6f4f7-1488-4a90-a349-6c0b2b2457a7" />

```html
<button invoketarget="actions">Actions</button>
<div role="menu" id="actions" popover>
  <button role="menuitem" tabindex=-1 autofocus>Edit</button>
  <button role="menuitem" tabindex=-1>Hide</button>
  <button role="menuitem" tabindex=-1>Delete</button>
</div>
```

Progressively-enhanced entry/exit animation to your popovers or dialogs:
- [Entry/exit animation code (1)](https://nerdy.dev/steal-this-popover-starter-kit)
- [Entry/exit animation code (2)](https://x.com/Una/status/1777735424850497799)

```css
/* Transition to these styles on entry, and from these styles on exit */
[popover]:popover-open {
  opacity: 1;
  rotate: 0turn;
  transition: rotate .5s, opacity .5s, display .5s allow-discrete, overlay .5s allow-discrete;
}

/* Entry transition starts with these styles */
@starting-style {
  [popover]:popover-open {
    opacity: 0;
    rotate: 1turn;
  }
}

/* Exit transition ends with these styles */
[popover]:not(:popover-open) {
  scale: 0;
  transition: scale .3s, display .3s allow-discrete, overlay .3s allow-discrete;
}
```

- [Living Standard](https://html.spec.whatwg.org/multipage/popover.html#the-popover-attribute)
- [Popover API Demo](https://www.oidaisdes.org/popover-api-accessibility.en/)
- [2024 Dropdown Menu with Popover and Anchor Pos (Floating UI fallback)](https://codepen.io/jh3y/pen/xxNZXMO)
- [2024-03-21 — On popover accessibility: what the browser does and doesn’t do ](https://hidde.blog/popover-accessibility/)
- [2024-03-04 — The Popover API, invokers, anchor positioning and @starting-style ✨](https://frontendmasters.com/blog/menus-toasts-and-more/)
