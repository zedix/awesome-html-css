# CSS `inherit` function

> It has a ton of potential to revolutionize how we use design tokens in components and UI libraries today.
— [Lea Verou](https://bsky.app/profile/lea.verou.me/post/3m37ln7vzak2t)

- [Original Proposal](https://github.com/w3c/csswg-drafts/issues/2864)

## Use Cases

Nested indentation:

```css
--indent: calc(inherit(--indent, 0) + 1);
```

[Overridable](https://bsky.app/profile/justinfagnani.com/post/3m35wkj7qkk24) design token defaults:

```css
/*
Before:
:host {
  --default-primary-color: blue;
}
:host {
  background-color: var(--primary-color, var(--default-primary-color));
}
*/

--primary-color: inherit(--primary-color, blue);
```
