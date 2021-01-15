# Responsive web Design Principles

1. Make the web site responsive design use `@media` query.

2. Make the images responsive by using `CSS` like below

```css
img {
  max-width: 100%;
  height: auto;
}
```

3. Retinal image for the `retinal screen` or high resolution screen - Just use the half width and half height this will make it look good on screen.

```html
<style>
  img {
    height: 250px;
    width: 250px;
  }
</style>
<img src="coolPic500x500" alt="A most excellent picture" />
```

4. Web Design Principles: Make Typography Responsive :
   The four different viewport units are:

- `vw` (viewport width): 10vw would be 10% of the viewport's width.
- `vh` (viewport height): 3vh would be 3% of the viewport's height.
- `vmin` (viewport minimum): 70vmin would be 70% of the viewport's smaller dimension (height or width).
- `vmax` (viewport maximum): 100vmax would be 100% of the viewport's bigger dimension (height or width).
