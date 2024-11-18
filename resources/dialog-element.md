# The `<dialog>` element

> [!NOTE]
> The dialog element has reached the tipping point of generally being the better option for web developers who need to implement dialogs in their web pages. The number of accessibility requirements a developer needs to be aware of, and the level of effort to implement custom ARIA dialogs is now largely taken care of by browsers. — [Scott O'Hara](https://www.scottohara.me/blog/2023/01/26/use-the-dialog-element.html)

```html
<button commandfor="my-dialog" command="show-modal" type="button">☰</button>

<dialog id="my-dialog" closedby="any">
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

- [2024-11-14 — Have a dialog](https://nerdy.dev/have-a-dialog)
- [2024-11-01 — Dialog light dismiss behavior: `closedby` attribute / `requestClose`](https://github.com/whatwg/html/pull/10737)
- [2023-01-26 — Use the dialog element (reasonably)](https://www.scottohara.me/blog/2023/01/26/use-the-dialog-element.html)
- [2022-04-13 — Building a dialog component](https://web.dev/building-a-dialog-component/)
- [2022-03-08 — A look at the dialog element's super powers](https://www.stefanjudis.com/blog/a-look-at-the-dialog-elements-super-powers/)
- [2022-02-08 — Replace JavaScript Dialogs With the New HTML Dialog Element](https://css-tricks.com/replace-javascript-dialogs-html-dialog-element/)
- [(Invokers Proposal) Add InvokeElement & InvokeEvent IDLs & invocation steps for Dialog & Popover](https://github.com/whatwg/html/pull/9841)
- [Bikeshed a name for "light dismiss for dialog"](https://github.com/openui/open-ui/issues/834)
- [Consider preventing page scroll when modal dialog is visible](https://github.com/whatwg/html/issues/7732)
- [Entry/Exit <dialog> animation 2024](https://codepen.io/jh3y/pen/LYoZWmJ)

<img src="https://web.dev/static/articles/building/a-dialog-component/image/screenshot-chrome-devtoo-cbb3686684fa1_856.png?hl=fr" height="420" />
