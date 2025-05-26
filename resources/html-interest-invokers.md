# Interest Invokers API (`[interesttarget]`)

> Goodbye unstylable `[title]` attribute; hello `[interesttarget]`! Combine it with the _Anchor Positioning API_ and _Popover API_ to create rich, responsive, and interactive UI elements like tooltips or hover cards, without JavaScript.

```html
<button interesttarget="profile-callout">
  ...
</button>

<div id="profile-callout" popover>
  ...
</div>
```

```css
[interesttarget] {
  /* Entry Exit delay */
  interest-target-delay: 0s 1s;

  &:has-interest {
    background-color: yellow;
  }
}
```


- [CBS News example (author name)](https://www.cbsnews.com/baltimore/news/human-remains-passenger-compartment-fire-vehicle-anne-arundel-county-police/)
  - [Source](https://youtu.be/VTCIStB6y8s?t=2701)
