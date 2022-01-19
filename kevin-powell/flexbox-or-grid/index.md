# [Flexbox or grid - How to decide?](https://www.youtube.com/watch?v=3elGSZSWTbM)

- `grid-auto-flow: column` makes grid behavior very similar to flexbox
- `flex-wrap: wrap` to allow flex items to wrap to new row; grid automatically wraps its children
- both flexbox and grid can create 2d layouts, but only grid is structured along the second dimension
- flexbox respects children's intrinsic sizing more than grid
- basically, use flexbox if the sizes of the items are not known and should be respected; use grid if the layout has to be rigid
