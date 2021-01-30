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
