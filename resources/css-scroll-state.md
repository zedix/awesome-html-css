# CSS scroll-state() container queries

##  The `stuck` query

- [Explainer](https://drafts.csswg.org/css-contain-4/scroll_state_explainer.html)
- [CSS picture-in-picture video transition using container queries + position: sticky 🧑‍🍳](https://x.com/jh3yy/status/1923179769123725595)

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


- [2025-05-23 — What's new in web UI — GoogleIO 2025](https://youtu.be/VTCIStB6y8s?t=1770)
