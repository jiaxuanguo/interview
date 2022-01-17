## [Logical Properties](https://web.dev/learn/css/logical-properties/)

- not all languages are left ot right, so properties like `margin-left` and `margin-right` may not work for certain languages; use [logical properties](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Logical_Properties) for better internationalization
- logical properties refer to the edges of a box relative to the flow, instead of their physical location
- element placement involves two types of orthogonal flows: block flow and inline flow
- `margin-block-start` is the equivalent of `margin-top` in a top to bottom flow
- `max-inline-size` is equivalent to `max-width`, while `max-block-size` is equivalent to `max-height`
- align text to `start` or `end`
- `vi`(i for inline) is equivalent to `vw`, while `vb`(b for block) is equivalent to `vh`
- logical properties' use cases exceed internationalization; for example, styling the label of a chart's y-axis
