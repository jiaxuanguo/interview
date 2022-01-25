## [Focus](https://web.dev/learn/css/focus/)

- focus state management improves accessibility
- form controls, buttons and links are focusable by default. navigate between them with `Tab` and `Enter+Tab`
- add `tabindex` attribute to a html element to make it focusable and/or change its order among focusable elements on the page
  - `tabindex="-1"` means the element can only be focused programmatically
  - honor document source order whenever possible (`tabindex="0"`)
- default focused behavior is browser and platform dependent, but usually involves a colored ring around the element
  - target the focused element with `:focus`, `:focus-within` and `:focus-visible` pseudo-classes
  - make sure the contrast is strong
  - `outline` is usually a good choice for focused indicator
  - `box-shadow` is not. for one, Windows in high contrast mode will not show shadows