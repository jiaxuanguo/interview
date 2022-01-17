# [Specificity](https://web.dev/learn/css/specificity/)

- level based scoring system
- design selectors with scores just as high as needed; rules with high scores can be hard to override
- order:
    1. inline
    2. id
    3. class, pseudo-class, attribute
    4. element, pseudo-element
    5. universal
- repeatedly add class to boost specificity; do **not** abuse this
