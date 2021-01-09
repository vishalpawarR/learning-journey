# CSS FCC

## CSS selector

1. Element selectors. -> element.
2. class selectors. -> `.`.
3. id selectors. -> `#`.
4. attribute selectors. -> [attr=value].

`color`: - to set color to text.

`font-size`: to set font color.

`font-family`: to change font.

`padding`, `border`, `margin` tag - is short hand.

`margin` -> to control the space between 2 elements - [Margin](https://www.freecodecamp.org/learn/responsive-web-design/basic-css/add-a-negative-margin-to-an-element).

`Absolute` and `relative` : absolute is `inch` and `mm` and `relative` units like `px`, `em`, `rem`.

Overriding ->precedence `element` < `class` < `id` < `inline style`.

Overriding the css using important -> `!important`.

Applying color : Hex, rgb(), hsl,hsla, rgba().

CSS variables - The values can be reused.

## Media query : @media

Applied visual Design :
`text-align:` - works only horizontally `justify`, `left`, `right`, `center`.

`width:`

`height:`

`font-style:`

`text-decoration:`

`box-shadow:` -> The box-shadow property takes values for `offset-x` (how far to push the shadow horizontally from the element),`offset-y` (how far to push the shadow vertically from the element),
blur-radius,
`spread-radius` and
`color`, in that order.

> Note : The `blur-radius` and `spread-radius` values are optional.

> Multiple box-shadow can be added by comma separating.

`opacity:` 0.1 to 1;

`text-transform:` `lowercase` | `uppercase`, `capitalize` | `initial` | `inherit` | `none`;

`line-height:`

`position` : `absolute` | `relative` | `fixed`| `sticky`.
position: https://www.freecodecamp.org/learn/responsive-web-design/applied-visual-design/change-an-elements-relative-position
Position pairs with the offset attribute top | bottom | left | right.

position: absolute; - Used to lock them to parent (https://www.freecodecamp.org/learn/responsive-web-design/applied-visual-design/lock-an-element-to-its-parent-with-absolute-positioning)

float : left | right | center .pairs with the width.

z-index : change the position of overlapping elements
https://www.freecodecamp.org/learn/responsive-web-design/applied-visual-design/change-the-position-of-overlapping-elements-with-the-z-index-property.

Center element horizontally using the margin property : freecodecamp.org/learn/responsive-web-design/applied-visual-design/center-an-element-horizontally-using-the-margin-property.
