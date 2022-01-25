## [Shadows](https://web.dev/learn/css/shadows/)

### box shadow
- `box-shadow` adds shadow to the box of an element
- shorthand includes horizontal offset, vertical offset, blur radius, spread radius and color
- add `inset` before any value to create an inner shadow
- possible to add multiple shadows on the same element
- the parent container may cut the shadow

### text shadow
- works only on text nodes
- has no spread radius, cannot be `inset`
- no clipping, will be visible if text is somewhat transparent

### drop shadow
- `drop-shadow` function as value of `filter` property
- usually used to add shadow to a cutout image
- has no spread radius, cannot be `inset`