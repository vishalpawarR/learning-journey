# [jQuery FCC](https://www.freecodecamp.org/learn/front-end-libraries/jquery/)

## Introduction to jQuery

jQuery is one of the many libraries for JavaScript. It is designed to simplify scripting done on the client side. jQuery's most recognizable characteristic is its dollar sign ($) syntax. With it, you can easily manipulate elements, create animations and handle input events.

Steps :

- Before we begin with jQuery add `<script></script>` to your html.
- Inside your script element, add this code: $(document).ready(function() { to your script. Then close it on the following line (still inside your script element) with: });. This is also know as the `document ready function`.

> Note: We'll learn more about functions later. The important thing to know is that code you put inside this function will run as soon as your browser has loaded your page.

> Note: This is important because without your document ready function, your code may run before your HTML is rendered, which would cause bugs.

## jQuery :

```js
$("selector-goes-here").addClass("class-goes-here");
```

> Note: The selector should be added with their symbol like as it is defined class with `.` and id selector with id `#` look below for example.

> Note: All jQuery function starts with `$` -> also know as `bling`.

> Note: Add `jQuery library` and `Animation.css`

### Target HTML Elements with Selectors Using jQuery

```js
$("button").addClass("animated bounce");
```

### Target Elements by class Using jQuery

```
$(".class").addClass("animated shake");
```

### Target Elements by id Using jQuery

```js
$("#id").addClass("animated fadeout");
```

### Remove Classes from an Element with jQuery

.removeClass() -> This can be used to remove class just like adding.

```js
$("button").removeClass("btn-default");
```

### Change the CSS of an Element Using jQuery

We can change the css property of an element by using the `jQuery` function `.css()`.

```js
$("Selector").css("property", "value");
$("#target1").css("color", "red");
```

### Disable an Element Using jQuery

You can also change the non-CSS properties of HTML elements with jQuery. For example, you can disable buttons.

When you disable a button, it will become grayed-out and can no longer be clicked.

jQuery has a function called `.prop()` that allows you to adjust the properties of elements.

Here's how you would disable all buttons:

```js
$("button").prop("disabled", true);
```

Disable only the `target1` button.

### Change Text Inside an Element Using jQuery

Using the `.html()` method.

Using jQuery, you can change the text between the start and end tags of an element. You can even change HTML markup.

Has a method named `.text()` which will just alter the text.

```js
$("h3").html(<em>jQuery Playground</em>);
// This will change text and style again.
```

`.text()`

```js
$("h2").text("jQuery Playground");
// This cna be used when we want to change the text inside the tags.
```

### Remove an Element Using jQuery

Now let's remove an HTML element from your page using jQuery using `.remove()`.

```js
$("h5").remove();
// This will completely remove the tag from page
```

### [Use appendTo to Move Elements with jQuery](https://www.freecodecamp.org/learn/front-end-libraries/jquery/use-appendto-to-move-elements-with-jquery)

```js
$("selector").appendTo("selector");
$("#target2").appendTo("#right-well");
```

### Clone an Element Using jQuery

```js
#("#target1").clone().appendTo("#target2");
```

### Target the Parent of an Element Using jQuery

Using the `parent()` method we can change and access the properties and change it.

```js
$("#target1").parent().css("background-color", "blue");
```

### Target the Parent of an Element Using jQuery

We can use the `parent()` to access the property.

```js
$("selector").parent().css("property", "value");
```

### Target the Children of an Element Using jQuery

Using the `children()` method we can access the child.

```js
$("#target1").children().css("color", "orange");
```

### Target a Specific Child of an Element Using jQuery

If we don't have the proper class, id then we can use this to select a required element `target:nth-child(n)`.

```js
$(selector.nth - child(n)).addClass("animated bounce");
```

### Target Even or Odd Elements Using jQuery

Using `:odd` or `:even` selector.

> Note: The index starts from 0.

```js
$("selector:even or :odd").addClass("animated shake");
```

### [Use jQuery to Modify the Entire Page](https://www.freecodecamp.org/learn/front-end-libraries/jquery/use-jquery-to-modify-the-entire-page)

## Classes which can be added in .addClass()

1. animated
2. bounce
3. shake
4. fadeout
5. hinge
