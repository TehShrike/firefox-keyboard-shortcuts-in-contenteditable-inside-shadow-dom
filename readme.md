# Firefox bug with contenteditable inside the shadow dom

To reproduce locally:

```sh
npm it
```

and then open http://localhost:8080

**or**

visit https://tehshrike.github.io/firefox-keyboard-shortcuts-in-contenteditable-inside-shadow-dom/

## To reproduce

Set focus inside of each of them and try hitting Cmd+Left to set focus to the beginning of the line (or Cmd+Shift+Left to select to the beginning of the line).

### Expected behavior

Focus should move to the left side of the contenteditable element.

### Observed behavior

In the version inside the shadow dom, the cursor does not move, and the keypress is handled by the browser – in the case of Cmd+Left, the browser navigates to the previous location in the browser history.
