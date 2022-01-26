# [The problem with multiple nav elements (and the simple solution)](https://www.youtube.com/watch?v=I1lq2ge7g4g)

- use `nav` for html semantics
- `nav` has a [aria landmark role](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/roles/landmark_role) 'navigation'
- problem: screen reader and other accessibility tools will have a difficult time differentiating between multiple `nav`s on the same page, since they all have the same role
- solution: add unique `aria-label`s on the `nav`s, they will be read out by the screen reader