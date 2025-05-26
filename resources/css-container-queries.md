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
