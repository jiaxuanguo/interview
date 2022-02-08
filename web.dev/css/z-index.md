## [Z-index and stacking contexts](https://web.dev/learn/css/z-index/)

- the `z-index` property sets a layer order along the z axis; element with a higher z-index will appear closer
- elements with no explicit `z-index` value will be arranged according to document source order
- `postion` has to be set to anything other than `static` for `z-index` to be effective
- > A stacking context is a group of elements that have a common parent and move up and down the z axis together.
- the `z-index` is relative to the base of the current stacking context
- certain css [properties](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Positioning/Understanding_z_index/The_stacking_context) create stacking contexts