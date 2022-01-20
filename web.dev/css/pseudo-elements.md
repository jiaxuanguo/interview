## [Pseudo-elements](https://web.dev/learn/css/pseudo-elements/)

- a pseudo-element is an element selectable or creatable only through css
- `::before` and `::after` create a child element
    - must have a `content` property to be valid
    - does not work with elements that do not accept children
- `::first-letter`
  - only on block elements
  - `color`, `background`, `border`, `float`, font and text properties
- `::first-line`
- `::backdrop`: target the backdrop beneath an element in fullscreen mode
- `::marker`
  - bullet of `ul` and `ol` or arrow of `summary`
  - `color`, `content`, `white-space`, font properties, `animation`, `transition`
- `::selection`: target selected text
- `::placeholder`: target placeholder of form controls
- `::cue`: target `video` caption
