# [min(), max(), and clamp() are CSS magic!](https://www.youtube.com/watch?v=U9VF-4euyRo)

- `width: 70%; max-width: 500px` is equivalent to `width: min(70%, 500px);`
- `width: 70%; min-width: 500px` is equivalent to `width: max(70%, 500px);`
- `min` and `max` can take more than two arguments; and they can be used together if necessary
- `clamp` is basically combining `min` and `max`; use it to create a responsive font-size
