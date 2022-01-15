# [Color](https://web.dev/learn/css/color/)

- numeric colors:
    1. hex
        - add another two digits to the end to represent alpha
    2. rgb/rgba
        - use space as separator, instead of comma
        - rgba for alpha
        - parameters can be either numbers from 0 to 255, or percentages
    3. [hsl](https://en.wikipedia.org/wiki/HSL_and_HSV): hue, saturation, lightness
        - basically, hsl describes the color space with a cylindrical coord system
        - rgba for alpha
    4. lab/lch: new functions to cover the large color spaces supported by modern screens
- color keywords: named colors, plus `transparent` and `currentColor`
    - `currentColor` matches the dynamic value of the `color` property
