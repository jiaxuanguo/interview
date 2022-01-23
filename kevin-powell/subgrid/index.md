# [This is going to be a game changer!](https://www.youtube.com/watch?v=dZHnAsYu2eU)

#### problem
align columns from two different grid containers, with some column widths based on fr
#### solution
1. turn the common ancestor into a grid container
2. set the original grid containers' `grid-template-columns`/`grid-template-rows` to `subgrid`
#### explanation
- essentially tells a grid container to use the column/row dimensions of its parent
- [mdn article](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Subgrid)
#### support
only firefox, as of 2022/1/23
