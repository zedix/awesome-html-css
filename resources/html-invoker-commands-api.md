### The `commandfor` & `command` attributes (Invoker Commands API)

New syntax:

```html
<button commandfor="my-modal" command="show-modal">Trigger dialog</button>
<dialog id="my-modal">This is my dialog</dialog>
```

```html
<div class="counter">
  <button commandfor="num" command="step-down">-</button>
  <input type="number" min="1" id="num" value="1">
  <button commandfor="num" id="btn" command="step-up">+</button>
</div>
```

- [2024-07-15 — An update on invokers: Invoker commands in HTML](https://utilitybend.com/blog/an-update-on-invokers-invoker-commands-in-html)
- [2024-03-24 — I love invokers and you should too](https://buttondown.email/cascade/archive/018-i-love-invokers-and-you-should-too/)
- [Full list of built-in commands](https://open-ui.org/components/invokers.explainer/#defaults)
- [Can I use HTML attribute: invokeaction](https://caniuse.com/mdn-html_global_attributes_invokeaction)
- [Explainer](https://open-ui.org/components/invokers.explainer/)
- [Invokers Proposal](https://github.com/whatwg/html/pull/9841)
- [Intent to Prototype: Invokers (Chrome)](https://groups.google.com/a/chromium.org/g/blink-dev/c/tDanwUCp2cg)
- [Ship Invokers proposal to all major browsers (Nov 2023)](https://www.keithcirkel.co.uk/working-on/#ship-invokers-proposal-to-all-major-browsers)

Old syntax:

```html
<button invoketarget="my-dialog">This opens a dialog</button>
<dialog id="my-dialog">This is the dialog</dialog>
```

Adding `invoketarget` and `invokeaction` attributes to `<button>` and `<input type="button">` / `<input type="reset">` elements would allow authors to assign behaviour to buttons in a more accessible and declarative way, while reducing bugs and simplifying the amount of JavaScript pages are required to ship for interactivity. Buttons with invoketarget will - when clicked, touched, or enacted via keypress - dispatch an `InvokeEvent` on the element referenced by invoketarget, with some default behaviours.
