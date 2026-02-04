# The `Customizable <select>` (ex `<selectlist>` ⇢ ex `<selectmenu>` ⇢ ex `<select> v2`)

<img height="260" src="https://github.com/user-attachments/assets/28975bd5-5cbc-464d-8217-7479f271a317" />
<img height="260" src="https://developer.chrome.com/static/blog/new-in-web-ui-io-2025-recap/image/select-layout_856.png" />

- [2026-02-03 — Nice Select](https://nerdy.dev/nice-select)
- [2025-07-05 — custom `<select>` with CSS 🧑‍🍳](https://x.com/jh3yy/status/1941272674464039232?s=20)
- [2025-07-01 — Custom Select (that comes up from the bottom on mobile)](https://frontendmasters.com/blog/custom-select-that-comes-up-from-the-bottom-on-mobile/)
- [2025-03-24 — The `<select>` element can now be customized with CSS (Chrome 135)](https://developer.chrome.com/blog/a-customizable-select?hl=en)
- [2025-03-15 — The customizable select - Part one: history, trickery, and styling the select with CSS](https://utilitybend.com/blog/the-customizable-select-part-one-history-trickery-and-styling-the-select-with-css)
- [2025-03-10 —Future of CSS: Select styling without the hacks
](https://dev.to/link2twenty/future-of-css-select-styling-without-the-hacks-38c2)
- [2025-01-10 — Updates to the customizable select API](https://una.im/select-updates/)
- [2024-12-03 — 2025 gonna be the year of customized `<select>`](https://x.com/wesbos/status/1863977220110217250)
- [2024-09-19 — Custom `<select>` boilerplate + transitions](https://nerdy.dev/custom-select-with-transitions-boilerplate)
- [2023-07-25 — Demo examples](https://codepen.io/collection/BNZjPe)
- [2023-06-01 — Advanced Form Control Styling With Selectmenu And Anchoring API](https://www.smashingmagazine.com/2023/06/advanced-form-control-styling-selectmenu-anchoring-api/)
- [Open UI's `<selectlist>` demos](https://microsoftedge.github.io/Demos/selectlist/index.html)
- [Open UI's issues](https://github.com/openui/open-ui/issues?q=is%3Aissue+is%3Aopen+label%3Aselect)
- [Open UI's design decisions](https://open-ui.org/components/selectlist/#design-decisions)
- [Open UI's explainer](https://open-ui.org/components/selectlist)
- [WHATWG Stage 1: Stylable `<select>` element](https://github.com/whatwg/html/issues/9799)

Opt-in mode:

```css
select, ::picker(select) {
  appearance: base-select;
}
```

Alternative [snippet](https://frontendmasters.com/blog/custom-select-that-comes-up-from-the-bottom-on-mobile/#the-base):

```css
select {
  appearance: none;
  @supports (appearance: base-select) {
    &,
    &::picker(select) {
      appearance: base-select;
    }
  }
}
```

```html
<select class="my-custom-select">
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
</select>
```

![image](https://github.com/zedix/awesome-html-css/assets/27975/5fbbd69c-c1fe-4b7b-b165-77023eb6a578)


```html
<select>
  <button class="action-btn" type="button">
    <selectedoption>
      <span class="preview-heading">Create a merge commit</span>
      <span class="action-heading">Merge Pull Request</span>
      <span class="description">All commits from this branch will be added to the base branch via a merge commit.</span>
    </selectedoption>
  </button>
  <button class="open-list-btn" type="selectlist">
    <span class="arrow">
      <figure>↓</figure> <!-- should be image, using this for demo shortcut only -->
    </span>
  </button>
  <listbox>
    <option value="merge-commit">
      <span class="preview-heading">Create a merge commit</span>
      <span class="action-heading">Merge Pull Request</span>
      <span class="description">All commits from this branch will be added to the base branch via a merge commit.</span>
    </option>
    <option value="squash-merge">
      <span class="preview-heading">Squash and merge</span>
      <span class="action-heading">Squash and merge</span>
      <span class="description">The 1 commit from this branch will be added to the base branch.</span>
    </option>
    <option value="rebase-merge">
      <span class="preview-heading">Rebase and merge</span>
      <span class="action-heading">Rebase and merge</span>
      <span class="description">The 1 commit from this branch will be rebased and added to the base branch.</span>
    </option>
  </listbox>
</select>
```


## Mode `multiple`

- [2026-01-15 —An update on customizable selects: the multiple select](https://utilitybend.com/blog/an-update-on-customizable-selects-the-multiple-select)
- [Customizable select listbox #42358](https://github.com/mdn/content/issues/42358)
    - [Customizable select listbox (Chrome 145+)](https://chromestatus.com/feature/6222145025867776?gate=5204361793503232)
