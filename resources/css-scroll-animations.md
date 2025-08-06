# CSS Scroll-Driven Animations (`view-timeline`, `animation-timeline`, `view()`)

- [Scroll-Driven Sticky Heading](https://css-tricks.com/scroll-driven-sticky-heading/)
- [Silky-smooth, uninterrupted scroll-driven web animations](https://webstudio.is/scroll-driven-animations)
- [Introducing "Unleash the power of Scroll-Driven Animations"](https://developer.chrome.com/blog/scroll-driven-animations-video-course?hl=en)
- [CSS Scroll-triggered Animations with Style Queries](https://ryanmulligan.dev/blog/scroll-triggered-animations-style-queries/)
- [Scroll-Driven Animations: You want overflow: clip, not overflow: hidden](https://www.bram.us/2024/02/14/scroll-driven-animations-you-want-overflow-clip-not-overflow-hidden/)
- [Demo: show off Scroll-driven Animations](https://scroll-driven-animations.style/)
- [Demo: CSS-Only Sticky CTA](https://x.com/jh3yy/status/1765166342502559923?s=20)
- [Real World examples](https://x.com/Una/status/1767237843330433298?s=20)
- [Spec: scroll-animations-1 examples](https://github.com/w3c/csswg-drafts/pull/11421)
- [First look into scroll-driven animations](https://www.builder.io/blog/scroll-driven-animations)
- [30 CSS scroll driven animation examples](https://nerdy.dev/notebook/scroll-driven-animations.html)

```css
@keyframes slide-left {
    from { transform: scale(0.7); }
    to   { transform: scale(1); }
}
.scroll-animate-slide-left {
    transform-origin: top right;
    animation: slide-left ease-out both;
    animation-timeline: view(block -64px);
    animation-range: entry 0% entry 50%;
}
```


## Examples

- [Scroll-driven Animations Demos](https://scroll-driven-animations.style/)
- [Photo gallery with Scroll Driven Animation](https://codepen.io/argyleink/pen/LEYOgxy)
