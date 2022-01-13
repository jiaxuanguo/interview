## [Elements and attributes](https://web.dev/learn/forms/form/)

### The form element in depth
  - nesting form controls in `form` is not required; use the `form` element for its built-in features
  - `formaction` and `formmethod` attributes on the submit button overrides respective attributes on the `form` element
  - the `enterkeyhint` attribute can change the text on the enter key of virtual keyboards
  - `<input type="image">` creates a graphical submit button; no recommended
  - timeouts on form submissions usually hurts user experience
  - use `<input type="file">` to accept user selected files; add `enctype="multipart/form-data"` to `form` to send files via POST request

### Form fields in depth
  - `<input type="text" />` for short texts, `<textarea />` for longer text
  - play with `textarea`'s `resize` attribute; maybe [**don't**](https://catalin.red/css-resize-none-is-bad-for-ux/) set it to `none`
  - devices provide different virtual keyboards for different input `type`s
  - `type="date"` for picking dates
  - `type="color"` for picking colors
  - `type="checkbox"` for select/unselect options
  - `type="radio"` for selecting one option out of many
  - `type="select"` for selecting one or many options out of a list of many
  - `type="range"` for selecting a range of numbers
  - `type="hidden"` makes an input invisible and unmodifiable
  - there is a javascript api for implementing [custom form controls](https://web.dev/more-capable-form-controls/#form-associated-custom-elements)

### Form attributes in depth
  - `inputmode` attribute changes the virtual keyboard provided
  - browsers show inc/dec arrows for `type="number"`, so unless those are desired, use `inputmode="numeric"` instead
  - `enterkeyhint` changes the text/icon of the virtual keyboard's enter key
  - do **not** add `autofocus` because the behavior may be confusing
  - show validation error messages rather than disabling the submit button altogether; disable the button and show a loading message after submission to prevent multiple submissions
  - always show data users previously entered during a multi-step form
  - [difference](https://stackoverflow.com/questions/6003819/what-is-the-difference-between-properties-and-attributes-in-html/6004028#6004028) between `input.value` and `input.getAttribute('value')`
  - be cautious with `placeholder`, it usually causes confusion; consider placing the explanation of a field beside or beneath the input
  - setup validation attributes
