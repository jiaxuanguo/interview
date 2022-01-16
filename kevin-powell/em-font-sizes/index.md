# [Why you shouldn't set font-sizes using em](https://www.youtube.com/watch?v=pautqDqa54I)

- em is relative to the parent's font-size, so if multiple elements use em as their font-size unit, an upstream change
of font size could cause a chain reaction
- in other words, all em based font-sizes down the hierarchy are coupled
- use rem instead, it is relative to the root's font-size
- use em for the other properties on the same element, i.e. `padding`, `line-height`; in this case, the em is relative to its own font-size
