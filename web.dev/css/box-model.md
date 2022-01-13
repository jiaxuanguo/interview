## [Box Model](https://web.dev/learn/css/box-model/)

- every element displayed is a box
- extrinsic sizing means providing fixed dimension values, intrinsic sizing means let the browser adjust the size based on content
- content will overflow if the container is not large enough
- the box includes content, padding, border and margin
- scrollbars occupy padding space
- outlines and box-shadows occupy margin space
- think of the box model as a framed picture
- a `block` element will fill available inline space, whereas an `inline` element will be as large as its content
- an `inline` element's margin will not be respected
- value of `box-sizing` determines how dimensions of the box will be calculated
- default value for `box-sizing` is `content-box`, but behaviour of `border-box` is more predictable
