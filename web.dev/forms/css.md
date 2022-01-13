## [CSS](https://web.dev/learn/forms/styling/)

### Styling forms
- different browsers provide different sets of default styling for form elements
- [progressive enhancement](https://developer.mozilla.org/en-US/docs/Glossary/Progressive_Enhancement): start with a widely compatible core functionality and build on that
- change `font-size` and `line-height` to ensure readability; use responsive units such as `rem` and `em`
- group element of the same form field together and separate different form fields
- form controls should look like form controls
- add styles to the submit button to emphasize it
- style different states of the form control differently

### Styling form controls
- css rule `appearance: none` will remove agent default styles
- [*replaced elements*](https://developer.mozilla.org/en-US/docs/Web/CSS/Replaced_element) like `option` cannot be styled with css
- radio and checkbox cannot be styled directly; hide them and provide a custom version (as pseudo-elements)
  - hide via `opacity: 0` instead of `display: none` to retain them in the accessibility tree
  - implement the replacement as pseudo-element so they **won't** show up in the accessibility tree
  - do **not** get too wild
- css property `accent-color` allows quick customization of the coloring of form controls
- 

