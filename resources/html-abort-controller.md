# Abort Controller

- [Don't Sleep on AbortController](https://kettanaito.com/blog/dont-sleep-on-abort-controller)
- [I Cannot Believe Abort Controller Can Do This](https://www.youtube.com/watch?v=BeZfiCPhZbI&t=454s)

Calling controller.abort() removes the resize listener from the window. That is an extremely elegant way of handling event listeners because you no longer need to abstract the listener function just so you can provide it to .removeEventListener().

```js
// const listener = () => {}
// window.addEventListener('resize', listener)
// window.removeEventListener('resize', listener)

const controller = new AbortController()
window.addEventListener('resize', () => {}, { signal: controller.signal })
controller.abort()
```
