# [FLEXBOX](https://scrimba.com/learn/flexbox/your-first-flexbox-layout-flexbox-tutorial-canLGCw)

- To make it to flex just add `display: flex;`

## Axis

The flex box is generally in the form of `row` from `left to right`. Generally we use the `left-right` axis onlyTo change direction to `column` we need to add `flex-direction: column;`
This is called as main-axis.

```css
flex-rotation: row | column;
```

## To add space between element

When the flex is created the elements will not have space to add space we use the `justify-content: ;`

```css
justify-content: flex-start | flex-end | center | space-around | space-between |
  space-evenly;
```

## [Using margin to add space to the element](https://scrimba.com/learn/flexbox/positioning-items-flexbox-tutorial-cGNK6fN)

`justify-content: ;` this is used to add the space but to customize the space between them we can use the margin property.

```css
margin-left: auto;
```

## Making the flex element responsive

To make the elements of the flex to grow and shrink we can use `flex: ;` it is short hand for the ["flex-grow, flex-shrink, flex-basis"](https://scrimba.com/learn/flexbox/flex-grow-shrink-basis-flexbox-tutorial-ck6L7fv). We will learn about this in next parts.

```css
flex: 1;
```

## [To align elements in cross axis](https://scrimba.com/learn/flexbox/align-items-flexbox-tutorial-cJqymH9)

(if main axis is row then the cross axis opposite of main axis here it is a column).
To do this use the `align-item: ;` to move it in cross axis.

## [Flex direction column](https://scrimba.com/learn/flexbox/flex-direction-column-flexbox-tutorial-cDzJ3Uq)

This is same as the row.

> Note: set the flex box `height: 100%` and we must set want of body and html to 100%; and `justify-content: ;` and

## [Flex wrapping](https://scrimba.com/learn/flexbox/wrapping-flexbox-tutorial-cJqk7fW)

This is like test wrapping in IDES it will move the text down if screen size is small. We can do this by using `flex-wrap: ;`. by default the `flex-wrap: nowrap;`

## [Order](https://scrimba.com/learn/flexbox/order-flexbox-tutorial-ck6LpuM)
