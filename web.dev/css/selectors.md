## [Selectors](https://web.dev/learn/css/selectors/)

- simple selectors: 
  - universal `*`
  - type/tag/element `h1`
  - class `.class`
  - id `#id`
  - attribute `[attribute="value"]`
    - add `s` or `i` to toggle case sensitivity
    - `*=`, `^=` and `$=` for inexact matching
  - group `,`
- pseudo-classes describe the state an element is in
- pseudo-elements are dom elements inserted with css
- combinators:
  - descendant ` `
  - child: `>`
  - sibling: `~`
  - next sibling: `+`
- combine multiple selectors to form a compound selector
