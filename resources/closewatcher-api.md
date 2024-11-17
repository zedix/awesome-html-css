
# The `CloseWatcher` API

> "Close requests" are a new concept that encompasses user requests to close something currently open, using the Esc key on desktop or the back gesture/button on Android.

- [Explainer with use cases](https://github.com/WICG/close-watcher)
- [Close requests and close watchers](https://html.spec.whatwg.org/multipage/interaction.html#close-requests-and-close-watchers)

```js
const watcher = new CloseWatcher();

// This fires when the user sends a close request, e.g. by pressing Esc on
// desktop or by pressing Android's back button.
watcher.onclose = () => {
  myModal.close();
};

// You should destroy watchers which are no longer needed, e.g. if the
// modal closes normally. This will prevent future events on this watcher.
myModalCloseButton.onclick = () => {
  watcher.destroy();
  myModal.close();
};
```
