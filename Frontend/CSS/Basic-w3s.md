# CSS

## `Background-image:;`

We can add images to the background.

```css
body {
  background-image: url("gradient_bg.png");
}
```

## Background-repeat

```css
body {
  background-image: url("gradient_bg.png");
  background-repeat: repeat-x;
}
/*background-repeat: repeat-x | repeat-y | no-repeat */
```

## CSS background-position

The background-position property is used to specify the position of the background image.

```css
body {
  background-image: url("img_tree.png");
  background-repeat: no-repeat;
  background-position: right top;
}
```

## CSS background-attachment

The background-attachment property specifies whether the background image should scroll or be fixed (will not scroll with the rest of the page):

```css
body {
  background-image: url("img_tree.png");
  background-repeat: no-repeat;
  background-position: right top;
  background-attachment: fixed;
  /* background-attachment : fixed | scroll |*/
}
```

## Background shorthand

Order of the background shorthand

- background-color
- background-image
- background-repeat
- background-attachment
- background-position

```css
body {
  background: #ffffff url("img_tree.png") no-repeat right top;
}
```

## Border

- Other [background property](https://www.w3schools.com/css/css_background_shorthand.asp)
- We can give different border color to using `border-color:` short-hand.
- The border property is a shorthand property for the following individual border properties:
  - border-width
  - border-style (required)
  - border-color

## [Outline](https://www.w3schools.com/css/css_outline_offset.asp)

## CSS Text

1. color:
2. text-align: left | right | center | justify |
3. direction: rtl
4. unicode-bidi: bidi-override
5. vertical-align: top | center | bottom.
6. text-decoration: overline | none | line-through | underline.
7. text-transform: uppercase | lowercase | capitalize.
8. text-indent: The text-indent property is used to specify the indentation of the first line of a text:
9. letter-spacing: increase or decrease.
10. line-height: line height.
11. word-spacing: space between the words.
12. white-space: nowrap;
13. text-shadow:

## CSS Fonts

1. font-family
   > Note : [Web safe fonts](https://www.w3schools.com/css/css_font_websafe.asp)
2. font-style: italic | normal | oblique.
3. font-weight: normal | bold.
4. font-variant: small | small-caps.
5. [font-size:](https://www.w3schools.com/css/css_font_size.asp)

- `vw` is viewport width, ex: 1vw = 1% of viewport width.

6. [Font google](https://www.w3schools.com/css/css_font_google.asp)

### Enabling Font Effects

- Google have also enabled different font effects that you can use.

- First add effect=effectname to the Google API, then add a special class name to the element that is going to use the special effect. The class name always starts with font-effect- and ends with the effectname.

## [Font pairing](https://www.w3schools.com/css/css_font_pairings.asp)

## [Font short hand](https://www.w3schools.com/css/css_font_shorthand.asp)

## [CSS ICONS](https://www.w3schools.com/css/css_icons.asp)

- [Font Awesome 5 Introduction](https://www.w3schools.com/icons/fontawesome5_intro.asp)
- [Icons Reference](https://www.w3schools.com/icons/icons_reference.asp)
- [Icons Tutorial](https://www.w3schools.com/icons/default.asp)

## CSS Links

- The four links states are:

  - a:link - a normal, unvisited link
  - a:visited - a link the user has visited
  - a:hover - a link when the user mouses over it
  - a:active - a link the moment it is clicked

## CSS List

1. list-style-type: circle | square | upper-roman | lower-alpha ;
2. list-style-image: url(); we can set image as marker.
3. list-style-position: outside | inside ;
4. list-style-type: none; to remove the order.
5. list short hand : list-style: list-style-type list-style-position list-style-image.

## CSS Table

1. border: short hand
2. width:
3. height:
4. border-collapse: collapse.
5. text-align:
6. vertical-align:
7. padding:
8. :hover
9. stripped table : nth-child( even | odd )
10. [Responsive Table](https://www.w3schools.com/css/css_table_responsive.asp)

## [display](https://www.w3schools.com/css/css_display_visibility.asp)

1. display: block | inline | inline-block |
   Hide an Element - display:none or visibility:hidden?

- inline-block allows us to set the width and height to the inline element.

## width and max-width

- It is better to use the max-width it becomes responsive and width will not be responsive.

## [position property](https://www.w3schools.com/css/css_positioning.asp)

1. position : static | relative | fixed | absolute | sticky | -webkit-sticky.

- The position element are positioned with top, bottom, left, right.
  By default it is `static`.
- fixed stays in same position.

## [CSS Overflow](https://www.w3schools.com/css/css_overflow.asp)

overflow: visible | hidden | scroll | auto.

> Note: The overflow property only works for block elements with a specified height.

- overflow-x: hidden; /_ Hide horizontal scrollbar _/
- overflow-y: scroll; /_ Add vertical scrollbar _/

## float

- float: left | right | none | inherit.
- [clear](https://www.w3schools.com/css/css_float_clear.asp): none | left | right | both | inherit.

## CSS Combinators

There are four different combinators in CSS:

- descendant selector (space)
- child selector (>)
- adjacent sibling selector (+)
- general sibling selector (~)
  |Selector | Example | Example description|
  |-----------|--------------|--------------|
  |element element | div p | Selects all <p> elements inside <div> elements|
  |element>element | div > p | Selects all <p> elements where the parent is a <div> element|
  |element+element | div + p | Selects the first <p> element that are placed immediately after <div> elements|
  |element1~element2 | p ~ ul | Selects every <ul> element that are preceded by a <p> element|
