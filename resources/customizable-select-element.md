# The `Customizable <select>` (ex `<selectlist>` ⇢ ex `<selectmenu>` ⇢ ex `<select> v2`)

<img height="260" src="https://github.com/user-attachments/assets/28975bd5-5cbc-464d-8217-7479f271a317" />
<img height="260" src="https://github.com/user-attachments/assets/9554f86c-7868-4db5-9e91-20b642f0bbca" />

- [WHATWG Stage 1: Stylable `<select>` element](https://github.com/whatwg/html/issues/9799)
- [Open UI's explainer](https://open-ui.org/components/selectlist)
- [Open UI's design decisions](https://open-ui.org/components/selectlist/#design-decisions)
- [Open UI's issues](https://github.com/openui/open-ui/issues?q=is%3Aissue+is%3Aopen+label%3Aselect)
- [Open UI's `<selectlist>` demos](https://microsoftedge.github.io/Demos/selectlist/index.html)
- [2023-06-01 — Advanced Form Control Styling With Selectmenu And Anchoring API](https://www.smashingmagazine.com/2023/06/advanced-form-control-styling-selectmenu-anchoring-api/)
- [2023-07-25 — Demo examples](https://codepen.io/collection/BNZjPe)
- [2024-09-19 — Custom `<select>` boilerplate + transitions](https://nerdy.dev/custom-select-with-transitions-boilerplate)

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
