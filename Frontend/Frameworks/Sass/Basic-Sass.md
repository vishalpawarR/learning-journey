# [Sass FCC](https://www.freecodecamp.org/learn/front-end-libraries/sass)

## Variables

The variable declared in Sass start with `$`.

```scss
$main-fonts: Arial, sans-serif;
$headings-color: green;

//To use variables:
h1 {
  font-family: $main-fonts;
  color: $headings-color;
}
```

## Nest CSS with Sass

Sass allows nesting of CSS rules, which is a useful way of organizing a style sheet.

Normally, each element is targeted on a different line to style it, like so:

### In CSS:

```css
nav {
  background-color: red;
}

nav ul {
  list-style: none;
}

nav ul li {
  display: inline-block;
}
```

### In Sass :

```scss
nav {
  background-color: red;

  ul {
    list-style: none;

    li {
      display: inline-block;
    }
  }
}
```

## [Create Reusable CSS with Mixins](https://www.freecodecamp.org/learn/front-end-libraries/sass/create-reusable-css-with-mixins)

In Sass, a mixin is a group of CSS declarations that can be reused throughout the style sheet.

### In CSS

```css
div {
  -webkit-box-shadow: 0px 0px 4px #fff;
  -moz-box-shadow: 0px 0px 4px #fff;
  -ms-box-shadow: 0px 0px 4px #fff;
  box-shadow: 0px 0px 4px #fff;
}
```

### In Sass

```scss
@mixin box-shadow($x, $y, $blur, $c) {
  -webkit-box-shadow: $x $y $blur $c;
  -moz-box-shadow: $x $y $blur $c;
  -ms-box-shadow: $x $y $blur $c;
  box-shadow: $x $y $blur $c;
}
```

Using Sass `@mixin` we can easily test out different values for `box-shadow` compared to the `CSS` and it can be reused in Sass.
