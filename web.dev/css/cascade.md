# [The Cascade](https://web.dev/learn/css/the-cascade/)

- > The cascade is the algorithm for solving conflicts where multiple CSS rules apply to an HTML element
- position and order of appearance
    - the later one wins
    - use this to provide a fallback for new features
- specificity
    - each selector has a specificity, the higher one wins
    - this is one reason why selectors should be kept simple
- origin, notice the symmetry
    1. user agent `!important`
    2. local user `!important`
    3. authored `!important`
    4. authored css: actual css from page
    5. local user styles: css from browser extensions etc.
    6. user agent defaults
- importance
    1. `transition` ???
    2. `!important`
    3. `animation`
    4. everything else
