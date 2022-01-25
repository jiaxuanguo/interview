## [Borders](https://web.dev/learn/css/borders/)

- border is the frame of the element's box
- `border-style` varies between browsers
  - `border-color` determines the border's color; the default is `currentColor`, which matches the element's font color
  - `border-color` can be set for each edge individually
  - `border-width` can be set to a length or keyword; it can also be set for each edge individually
  - `border-radius` determines the border box's corner radius. shorthand start from top-left and proceeds clockwise
  - a radius value actually consists of two lengths - the vertical and horizontal lengths. by providing two different lengths, the corner can be made unsymmetrical
  - it's possible to use an image as border by using the `border-image` property. the family of properties is similar to that of `background-image`