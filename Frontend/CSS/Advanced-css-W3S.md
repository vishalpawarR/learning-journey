# Advanced CSS

## CSS Rounded corner

The Border can be rounded using the CSS property `border-radius`

## [CSS Border Images](https://www.w3schools.com/css/css3_border_images.asp)

CSS border-image Property
The CSS `border-image` property allows you to specify an image to be used instead of the normal border around an element.

The property has three parts:

- The image to use as the border
- Where to slice the image
- Define whether the middle sections should be repeated or stretched.

## [CSS Multiple Backgrounds](https://www.w3schools.com/css/css3_backgrounds.asp)

## [CSS colors](https://www.w3schools.com/css/css3_colors.asp)

## [CSS Gradient](https://www.w3schools.com/css/css3_gradients.asp)

CSS gradients let you display smooth transitions between two or more specified colors.

CSS defines two types of gradients:

- [Linear Gradients (goes down/up/left/right/diagonally)](https://www.w3schools.com/css/css3_gradients.asp)
- [Radial Gradients (defined by their center)](https://www.w3schools.com/css/css3_gradients_radial.asp)

### CSS Linear Gradients

To create a linear gradient you must define at least two color stops. Color stops are the colors you want to render smooth transitions among. You can also set a starting point and a direction (or an angle) along with the gradient effect.

Syntax

```css
background-image: linear-gradient(direction, color-stop1, color-stop2, ...);
```

- Direction : to right | to left | to top | to bottom | to left bottom etc.

### Using Angles

If you want more control over the direction of the gradient, you can define an angle, instead of the predefined directions (to bottom, to top, to right, to left, to bottom right, etc.). A value of 0deg is equivalent to "to top". A value of 90deg is equivalent to "to right". A value of 180deg is equivalent to "to bottom".

Syntax

```css
background-image: linear-gradient(angle, color-stop1, color-stop2);
```

## CSS Shadow Effects

- text-shadow
- box-shadow

```css
text-shadow: horizontal Vertical blur color;
```

```css
h1 {
  color: white;
  text-shadow: 2px 2px 4px #000000;
}
```

Multiple Shadows

```css
h1 {
  text-shadow: 0 0 3px #ff0000, 0 0 5px #0000ff;
}
```

You can also use the text-shadow property to create a plain border around some text (without shadows):

Border around text!
Example

```css
h1 {
  color: yellow;
  text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;
}
```

### box-shadow Property

To apply shadow to the elements

```css
div {
  box-shadow: horizontal Vertical blur color;
}
```

## CSS Text

In this chapter you will learn about the following properties:

- text-overflow
- word-wrap
- word-break
- writing-mode

### text-overflow

- `overflow` this property makes text to be not to overflow that is it will not let the text to be come out side of the box. by combining it with the `text-overflow` we can show ellipsis (...) or any other style.

```css
p.test1 {
  white-space: nowrap;
  width: 200px;
  border: 1px solid #000000;
  overflow: hidden;
  text-overflow: clip;
}

p.test2 {
  white-space: nowrap;
  width: 200px;
  border: 1px solid #000000;
  overflow: hidden;
  text-overflow: ellipsis;
}
```

### CSS Word Wrapping

This will wrap the text if it is overflow outside the boxes.

```css
p {
  word-wrap: break-word;
}
```

### CSS Word Breaking

The CSS word-break property specifies line breaking rules.

```css
p.test1 {
  word-break: keep-all;
}

p.test2 {
  word-break: break-all;
}
```

### CSS Writing Mode

```css
p.test1 {
  writing-mode: horizontal-tb;
}

span.test2 {
  writing-mode: vertical-rl;
}

p.test2 {
  writing-mode: vertical-rl;
}
```

## CSS Web Fonts

### The CSS @font-face Rule

Your "own" fonts are defined within the CSS `@font-face` rule.

### Using The Font You Want

In the `@font-face` rule; first define a name for the font (e.g. myFirstFont) and then point to the font file.

Tip: Always use lowercase letters for the font URL. Uppercase letters can give unexpected results in IE.

To use the font for an HTML element, refer to the name of the font (myFirstFont) through the `font-family` property:

Example

```html
@font-face { font-family: myFirstFont; src: url(sansation_light.woff); } div {
font-family: myFirstFont; }
```

### CSS 2D Transforms

CSS transforms allow you to move, rotate, scale, and skew elements.
In this chapter you will learn about the following CSS property:

- transform

### CSS 2D Transforms Methods

With the CSS `transform` property you can use the following 2D transformation methods:

- `translate()`
- `rotate()`
- `scaleX()`
- `scaleY()`
- `scale()`
- `skewX()`
- `skewY()`
- `skew()`
- `matrix()`

### The translate() Method

The `translate()` method moves an element from its current position (according to the parameters given for the X-axis and the Y-axis).

The following example moves the `<div>` element 50 pixels to the right, and 100 pixels down from its current position:

Example

```css
div {
  transform: translate(50px, 100px);
}
```

### The rotate() Method

The `rotate()` method rotates an element clockwise or counter-clockwise according to a given degree.

The following example rotates the `<div>` element clockwise with 20 degrees:

Example

```css
div {
  transform: rotate(20deg);
}
```

> Note: Using negative values will rotate the element counter-clockwise.

### The scale() Method

The `scale()` method increases or decreases the size of an element (according to the parameters given for the width and height).

The following example increases the `<div>` element to be two times of its original width, and three times of its original height:

Example

```css
div {
  transform: scale(2, 3);
}
```

### The scaleX() Method

The `scaleX()` method increases or decreases the width of an element.

The following example increases the `<div>` element to be two times of its original width:

Example

```css
div {
  transform: scaleX(2);
}
```

### The scaleY() Method

The `scaleY()` method increases or decreases the height of an element.

The following example increases the `<div>` element to be three times of its original height:

Example

```css
div {
  transform: scaleY(3);
}
```

### The skewX() Method

The `skewX()` method skews an element along the X-axis by the given angle.

The following example skews the `<div>` element 20 degrees along the X-axis:

Example

```css
div {
  transform: skewX(20deg);
}
```

### The skewY() Method

The `skewY()` method skews an element along the Y-axis by the given angle.

The following example skews the `<div>` element 20 degrees along the Y-axis:

Example

```css
div {
  transform: skewY(20deg);
}
```

### The skew() Method

The `skew()` method skews an element along the X and Y-axis by the given angles.

The following example skews the `<div>` element 20 degrees along the X-axis, and 10 degrees along the Y-axis:

Example

```css
div {
  transform: skew(20deg, 10deg);
}
```

### The matrix() Method

The `matrix()` method combines all the 2D transform methods into one.

The matrix() method take six parameters, containing mathematic functions, which allows you to rotate, scale, move (translate), and skew elements.

The parameters are as follow: matrix(scaleX(),skewY(),skewX(),scaleY(),translateX(),translateY())

Example

```css
div {
  transform: matrix(1, -0.3, 0, 1, 0, 0);
}
```

## [CSS 3D Transform](https://www.w3schools.com/css/css3_3dtransforms.asp)

## [CSS Transitions](https://www.w3schools.com/css/css3_transitions.asp)

In this chapter you will learn about the following properties:

- `transition`
- `transition-delay`
- `transition-duration`
- `transition-property`
- `transition-timing-function`

### How to Use CSS Transitions?

To create a transition effect, you must specify two things:

the CSS property you want to add an effect to
the duration of the effect

Example

```css
div {
  width: 100px;
  height: 100px;
  background: red;
  transition: width 2s;
}
```

The transition effect will start when the specified CSS property (width) changes value.

Now, let us specify a new value for the width property when a user mouses over the `<div>` element:

Example

```css
div:hover {
  width: 300px;
}
```

### Specify the Speed Curve of the Transition

The `transition-timing-function` property specifies the speed curve of the transition effect.

The transition-timing-function property can have the following values:

- `ease` - specifies a transition effect with a slow start, then fast, then end slowly (this is default)
- `linear` - specifies a transition effect with the same speed from start to end
- `ease-in` - specifies a transition effect with a slow start
- `ease-out` - specifies a transition effect with a slow end
- `ease-in-out` - specifies a transition effect with a slow start and end
- `cubic-bezier(n,n,n,n)` - lets you define your own values in a cubic-bezier function.
  The following example shows the some of the different speed curves that can be used:

Example

```css
#div1 {
  transition-timing-function: linear;
}
#div2 {
  transition-timing-function: ease;
}
#div3 {
  transition-timing-function: ease-in;
}
#div4 {
  transition-timing-function: ease-out;
}
#div5 {
  transition-timing-function: ease-in-out;
}
```

> Transition + Transformation

## [CSS Animations](https://www.w3schools.com/css/css3_animations.asp)

CSS allows animation of HTML elements without using JavaScript or Flash!

In this chapter you will learn about the following properties:

- `@keyframes`
- `animation-name`
- `animation-duration`
- `animation-delay`
- `animation-iteration-count`
- `animation-direction`
- `animation-timing-function`
- `animation-fill-mode`
- `animation`

### The @keyframes Rule

When you specify CSS styles inside the `@keyframes` rule, the animation will gradually change from the current style to the new style at certain times.

To get an animation to work, you must bind the animation to an element.

The following example binds the "example" animation to the `<div>` element. The animation will last for 4 seconds, and it will gradually change the background-color of the `<div>` element from "red" to "yellow":

Example

```css
/* The animation code */
@keyframes example {
  from {
    background-color: red;
  }
  to {
    background-color: yellow;
  }
}

/* The element to apply the animation to */
div {
  width: 100px;
  height: 100px;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
}
```

## [CSS Tooltip](https://www.w3schools.com/css/css_tooltip.asp)

Create tooltips with CSS.

## [Object fit](https://www.w3schools.com/css/css3_object-fit.asp)

## [CSS Multiple Columns](https://www.w3schools.com/css/css3_multiple_columns.asp)

### CSS Multi-column Properties

In this chapter you will learn about the following multi-column properties:

- `column-count`
- `column-gap`
- `column-rule-style`
- `column-rule-width`
- `column-rule-color`
- `column-rule`
- `column-span`
- `column-width`

### CSS Create Multiple Columns

The `column-count` property specifies the number of columns an element should be divided into.

The following example will divide the text in the <div> element into 3 columns:

Example

```css
div {
  column-count: 3;
}
```

### CSS Specify the Gap Between Columns

The `column-gap` property specifies the gap between the columns.

The following example specifies a 40 pixels gap between the columns:

Example

```css
div {
  column-gap: 40px;
}
```

### CSS Column Rules

The `column-rule-style` property specifies the style of the rule between columns:

Example

```css
div {
  column-rule-style: solid;
}
```

The `column-rule-width` property specifies the width of the rule between columns:

Example

```css
div {
  column-rule-width: 1px;
}
```

The `column-rule-color` property specifies the color of the rule between columns:

Example

```css
div {
  column-rule-color: lightblue;
}
```

The `column-rule` property is a shorthand property for setting all the `column-rule-*` properties above.

The following example sets the width, style, and color of the rule between columns:

Example

```css
div {
  column-rule: 1px solid lightblue;
}
```

### Specify How Many Columns an Element Should Span

The `column-span` property specifies how many columns an element should span across.

The following example specifies that the `<h2>` element should span across all columns:

Example

```css
h2 {
  column-span: all;
}
```

### Specify The Column Width

The column-width property specifies a suggested, optimal width for the columns.

The following example specifies that the suggested, optimal width for the columns should be 100px:

Example

```css
div {
  column-width: 100px;
}
```

## CSS User Interface

In this chapter you will learn about the following CSS user interface properties:

- `resize`
- `outline-offset`

`resize: horizontal | vertical | both | none`.

> Note: The resize property works with the overflow.

### CSS Resizing

The `resize` property specifies if (and how) an element should be resizable by the user.

The following example lets the user resize only the width of a `<div>` element:

Example

```css
div {
  resize: horizontal;
  overflow: auto;
}
```

### CSS Outline Offset

The `outline-offset` property adds space between an outline and the edge or border of an element.

> Note: Outline differs from borders! Unlike border, the outline is drawn outside the element's border, and may overlap other content. Also, the outline is NOT a part of the element's dimensions; the element's total width and height is not affected by the width of the outline.

The following example uses the `outline-offset` property to add space between the border and the outline:

```css
Example div.ex1 {
  margin: 20px;
  border: 1px solid black;
  outline: 4px solid red;
  outline-offset: 15px;
}

div.ex2 {
  margin: 10px;
  border: 1px solid black;
  outline: 5px dashed blue;
  outline-offset: 5px;
}
```

## CSS Variables - The `var()` Function

The `var()` function is used to insert the value of a CSS variable.

CSS variables have access to the DOM, which means that you can create variables with local or global scope, change the variables with JavaScript, and change the variables based on media queries.

A good way to use CSS variables is when it comes to the colors of your design. Instead of copy and paste the same colors over and over again, you can place them in variables.

### Syntax of the var() Function

The `var()` function is used to insert the value of a CSS variable.

The syntax of the `var()` function is as follows:
syntax

```css
var(name, value)
```

> Note: Value is optional it is a fallback value if the variable value is not found.

### CSS Overriding Variables

Sometimes we want the variables to change only in a specific section of the page.

Assume we want a different color of blue for button elements. Then, we can re-declare the --blue variable inside the button selector. When we use var(--blue) inside this selector, it will use the local --blue variable value declared here.

We see that the local --blue variable will override the global --blue variable for the button elements:

Example

```css
:root {
  --blue: #1e90ff;
  --white: #ffffff;
}

body {
  background-color: var(--blue);
}

h2 {
  border-bottom: 2px solid var(--blue);
}

.container {
  color: var(--blue);
  background-color: var(--white);
  padding: 15px;
}

button {
  --blue: #0000ff;
  background-color: var(--white);
  color: var(--blue);
  border: 1px solid var(--blue);
  padding: 5px;
}
```

### CSS Change Variables With JavaScript

#### Change Variables With JavaScript

CSS variables have access to the DOM, which means that you can change them with JavaScript.

Here is an example of how you can create a script to display and change the --blue variable from the example used in the previous pages. For now, do not worry if you are not familiar with JavaScript. You can learn more about JavaScript in our JavaScript Tutorial:

Example

```html
<script>
  // Get the root element
  var r = document.querySelector(":root");

  // Create a function for getting a variable value
  function myFunction_get() {
    // Get the styles (properties and values) for the root
    var rs = getComputedStyle(r);
    // Alert the value of the --blue variable
    alert("The value of --blue is: " + rs.getPropertyValue("--blue"));
  }

  // Create a function for setting a variable value
  function myFunction_set() {
    // Set the value of variable --blue to another value (in this case "lightblue")
    r.style.setProperty("--blue", "lightblue");
  }
</script>
```

### Using Variables in Media Queries

Here, we first declare a new local variable named --fontsize for the .container class. We set its value to 25 pixels. Then we use it in the .container class further down. Then, we create a @media rule that says "When the browser's width is 450px or wider, change the --fontsize variable value of the .container class to 50px."

Here is the complete example:

Example

```css
/* Variable declarations */
:root {
  --blue: #1e90ff;
  --white: #ffffff;
}

.container {
  --fontsize: 25px;
}

/* Styles */
body {
  background-color: var(--blue);
}

h2 {
  border-bottom: 2px solid var(--blue);
}

.container {
  color: var(--blue);
  background-color: var(--white);
  padding: 15px;
  font-size: var(--fontsize);
}

@media screen and (min-width: 450px) {
  .container {
    --fontsize: 50px;
  }
}
```

## CSS Box Sizing

## CSS Media Queries

Media Query Syntax
A media query consists of a media type and can contain one or more expressions, which resolve to either true or false.

```css
@media not|only mediatype and (expressions) {
  CSS-Code;
}
```

The result of the query is true if the specified media type matches the type of device the document is being displayed on and all expressions in the media query are true. When a media query is true, the corresponding style sheet or style rules are applied, following the normal cascading rules.

Unless you use the not or only operators, the media type is optional and the all type will be implied.

You can also have different stylesheets for different media:

```html
<link
  rel="stylesheet"
  media="mediatype and|not|only (expressions)"
  href="print.css"
/>
```

### CSS3 Media Types

| Value  | Description                                           |
| ------ | ----------------------------------------------------- |
| all    | Used for all media type devices                       |
| print  | Used for printers                                     |
| screen | Used for computer screens, tablets, smart-phones etc. |
| speech | Used for screenreaders that "reads" the page out loud |

Media Queries Simple Examples
One way to use media queries is to have an alternate CSS section right inside your style sheet.

The following example changes the background-color to lightgreen if the viewport is 480 pixels wide or wider (if the viewport is less than 480 pixels, the background-color will be pink):

Example

```css
@media screen and (min-width: 480px) {
  body {
    background-color: lightgreen;
  }
}
```

The following example shows a menu that will float to the left of the page if the viewport is 480 pixels wide or wider (if the viewport is less than 480 pixels, the menu will be on top of the content):

Example

```css
@media screen and (min-width: 480px) {
  #leftsidebar {
    width: 200px;
    float: left;
  }
  #main {
    margin-left: 216px;
  }
}
```

### [CSS Flexbox](https://www.w3schools.com/css/css3_flexbox.asp)

CSS Flexbox Layout Module
Before the Flexbox Layout module, there were four layout modes:

- Block, for sections in a webpage
- Inline, for text
- Table, for two-dimensional table data
- Positioned, for explicit position of an element

The Flexible Box Layout Module, makes it easier to design flexible responsive layout structure without using float or positioning.
Like we specified in the previous chapter, this is a flex container (the blue area) with three flex items:

The flex container becomes flexible by setting the `display` property to flex:

The flex container properties are:

- flex-direction
- flex-wrap
- flex-flow
- justify-content
- align-items
- align-content

The column value stacks the flex items vertically (from top to bottom):
Example

```css
.flex-container {
  display: flex;
  flex-direction: column;
}
```

Example
The column-reverse value stacks the flex items vertically (but from bottom to top):

```css
.flex-container {
  display: flex;
  flex-direction: column-reverse;
}
```

Example
The row value stacks the flex items horizontally (from left to right):

```css
.flex-container {
  display: flex;
  flex-direction: row;
}
```

Example
The row-reverse value stacks the flex items horizontally (but from right to left):

```css
.flex-container {
  display: flex;
  flex-direction: row-reverse;
}
```

- flex-wrap: wrap | nowrap | wrap-reverse`

### The flex-flow Property

The `flex-flow` property is a shorthand property for setting both the `flex-direction` and `flex-wrap` properties.

```css
Example .flex-container {
  display: flex;
  flex-flow: row wrap;
}
```

### The justify-content Property

- `justify-content: center | flex-start | flex-end | space-around | space-between`

### The align-items Property

- `align-items: center | flex-start | flex-end | stretch | baseline`

### The align-content Property
