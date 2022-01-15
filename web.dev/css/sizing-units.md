# [Sizing Units](https://web.dev/learn/css/sizing/)

- number values
    - use numbers on `line-height`, so it scales with `font-size`
- percentage values
    - percentage `margin`/`padding` is calculated by multiplying the parent's **width**
    - percentage `transform` is calculated by multiplying the element's sizes
- attach a unit to a number to form a dimension; lengths are dimensions that refer to distance
- absolute length resolves against the same base; the base can be either physical measurement or device pixel
- relative length is calculated against a base value
    - font-size: `rem`/`em`, `rlh`/`lh`, `ch`/`ic`, `cap`, `ex`
    - viewport: `vw`/`vh`, `vi`/`vb`, `vmin`/`vmax`
- misc:
    - angles: `1turn` = `3.14rad` = `360deg` = `400grad`
    - resolution: `dpi`
