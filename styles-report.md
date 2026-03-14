## 1. Selected UI element

- **Element:** 
  Button `Get Started`

---


## 2. Analyze five CSS properties

- **Property 1:**  `background-color`

Computed value:
rgb(240, 240, 240)

Rule:
button { background-color: buttonface; }

Generated CSS:
user agent stylesheet

Original source:
This property is not defined in the project styles. The visual background
of the button is instead provided by the gradient applied through
`background-image` in the `.jb-btn--primary` rule, the
`@include jb-gradient-button($jb-btn-gradient-c1, $jb-btn-gradient-c2)` style.scss:46;


- **Property 2:**  `color`

Computed value:
rgb(249, 250, 251)

Rule:
.jb-btn--primary { color: #f9fafb; }

Generated CSS:
Mapped in source maps

Original source:
Defined in styles.scss:45, the variable color `$jb-btn-text-light`. 
This value traces back to the design token `$color-text-light: #f9fafb` from _tokens.scss:9.


- **Property 3:**  `border-bottom-color`

Computed value:
rgba(249, 250, 251, 0.1)

Rule:
.jb-btn--primary { border-color: rgba(249, 250, 251, 0.1); }

Generated CSS:
Mapped in source maps

Original source:
Defined in styles.scss:48, the shorthand property `border-color: rgba(249, 250, 251, 0.1)`
The browser resolves this shorthand and applies the value to all four individual sides, 
showing up as border-bottom-color (along with top, left, and right) in the Computed tab.


- **Property 4:**  `box-shadow`

Computed value:
0 0 0 1px rgba(15, 23, 42, 0.9), 0 18px 45px rgba(15, 23, 42, 0.9), 0 0 45px rgba(255, 75, 139, 0.45);

Rule:
.jb-btn--primary { box-shadow: 0 0 0 1px rgba(15, 23, 42, 0.9), 0 18px 45px rgba(15, 23, 42, 0.9), 0 0 45px rgba(255, 75, 139, 0.45); }

Generated CSS:
Mapped in source maps

Original source:
This property is not defined directly in the class styles. The complex multi-layered 
shadow of the button is instead provided by the mixin applied through the `.jb-btn--primary` rule,
 the `@include jb-gradient-button($jb-btn-gradient-c1, $jb-btn-gradient-c2)` styles.scss:45;


- **Property 5:**  `cursor`

Computed value:
pointer

Rule:
.jb-btn { cursor: pointer; }

Generated CSS:
Mapped in source maps

Original source:
Defined in styles.scss:30 inside the base `.jb-btn` class. 
This property is applied directly from the base component styles and is not overridden by the primary modifier.

---


## 3. Ambiguous / Indirect Mapping Cases

1. **Shorthand Properties**

Example: `Property 3: border-bottom-color`

This happens because the code uses a "shorthand" like border-color, which the browser then splits into four separate sides (top, bottom, left, right).

2. **SCSS Variables and Mixins**

Example: `Property 2: color` and `Property 4: box-shadow`

The mapping can be indirect when using SCSS features. Source Maps can point to a specific line, 
but the actual values (like colors or coordinates) are not there. Instead, only a variable name or a @include command can be seen. 
To find the real values, an additional step is required to trace the code back to the original tokens or mixin definitions in other files.

3. **Overlapping Styles**

Example: `Property 1: background-color`

The information in DevTools can be technically correct but practically useless for styling. 
For example, background-color can be traced to a default browser style, but it stays hidden because a background-image (gradient) is placed on top of it.
In this case, the right source of the element's look can only be found by checking a different, overlapping property.