# CSS Container Queries (`container-type`, `container-name`, `@container`)

## CSS Style Queries

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
