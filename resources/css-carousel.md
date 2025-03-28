# CSS Carousel

- [CSS Carousel Gallery (Chrome 135)](https://chrome.dev/carousel/)
- [CSS Carousel Configurator (Chrome 135)](https://chrome.dev/carousel-configurator/)

> [!NOTE]
> - Works with JavaScript disabled.
> - No hydration or lazy sizing (reduce CLS).
> - Ready for all kinds of scroll animation and triggers.
> - Accessibility is included.
> - Touch, mouse, and keyboard friendly.

## Snap Scroller

```html
<ul class="carousel">
  <li>…</li>
  <li>…</li>
  …
<ul>
```

```css
.carousel {
  overflow-x: auto;
  overscroll-behavior-x: contain;
  scroll-snap-type: x mandatory;
  anchor-name: --carousel;

  > li {
    scroll-snap-align: center;
  }
}
```

## Scroll Buttons

```css
.carousel {
  &::scroll-button(*) {
    position: fixed;
    position-anchor: --carousel;
    font-family: "Material Symbols Outlined";
  }

  &::scroll-button(right) {
    position-area: inline-end center;
    content: 'arrow_forward' / 'Next';
  }

  &::scroll-button(left) {
    position-area: inline-start center;
    content: 'arrow_back' / 'Previous';
  }
}
```

## Scroll Markers

```css
.carousel {
  scroll-marker-group: after;

  &::scroll-marker-group {
    position: fixed;
    position-anchor: --carousel;
    position-area: block-end;
    margin: 10px;

    display: grid;
    grid-auto-columns: 20px;
    grid-auto-flow: column;
    gap: 20px;
  }

  & > li::scroll-marker {
    content: ' ';

    &:target-current {
      background: var(--accent);
    }
  }
}
```

```css
.carousel {
  &::scroll-button(left) {
    content: "⬅" / "Scroll Left";
  }
  &::scroll-button(right) {
    content: "⮕" / "Scroll Right";
  }
  &::scroll-button(*)::focus-visible {
    outline-offset: 5px;
  }

  scroll-marker-group: after;

  > li::scroll-marker {
    content: ' ';

    &:target-current {
      background: var(--accent);
    }
  }
}
```

- [2025-03-20 — Carousels with CSS](https://developer.chrome.com/blog/carousels-with-css)
