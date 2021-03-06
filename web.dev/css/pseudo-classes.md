## [Pseudo-classes](https://web.dev/learn/css/pseudo-classes/)

- use pseudo-classes to select the different states of an (form control) element
- differentiating states with color alone is bad - some people are visually impaired or colorblind
- interactive states:
  - `:hover`
  - `:active`
  - `:focus`: if an element is focused 
    - `:focus-within`: if one of the descendents of an element is focused
    - `:focus-visible`: if the browser deems the focused state requires indication
  - `:target`: select the element with an id matching the url hash
    - use case: highlight the target region after user clicked on an anchor
  - `:link` and `:visited`: if the link of an `a` element hasn't or has been visited, respectively
    - the LVHA rule: style `a` in the order `:link` > `:visited` > `:hover` > `:active` to avoid unexpected overriding
- form states:
  - `:disabled` and `:enabled`
  - `:checked`, `:not(:checked)` and `:indeterminate`: checkboxes and radios
  - `:placeholder-shown`
  - `:valid`, `:invalid`, `:required`, `:optional` and `:in-range`
- hierarchical states:
  - `:first-child`, `:last-child` and `:nth-child`
  - `:only-child` and `:only-of-type`
  - `:first-of-type`, `:last-of-type` and `:nth-of-type`
  - [An+B microsyntax](https://www.w3.org/TR/css-syntax-3/#anb-microsyntax): every Ath after B
  - `:empty` if an element has no children; **whitespace counts as a child**
- `:is`: compact way to write select group `:is(h2, li, img)`
- `:not`: negation
