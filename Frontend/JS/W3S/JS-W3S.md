# JavaScript

## JS W3S

- `getElementByClassName()`
- `getElementById()` - > Most used tag in JS.

## JS Output

Using JS we can display data in different ways :

- Writing into an HTML element, using `innerHTML`.
- Writing into the HTML output using `document.write()`.
- Writing into the alert box, using `window.alert()`.
- Write into the browser console, using `console.log()`.

### USing the `innerHTML`

- To access an html element, JS can use the `document.getElementById(id)` method.
- The `id` attribute defines the HTMl element. The innerHTML property defines the HTML content:
  Example

```html
<!DOCTYPE html>
<html>
  <body>
    <h1>My First Web Page</h1>
    <p>My First Paragraph</p>

    <p id="demo"></p>

    <script>
      document.getElementById("demo").innerHTML = 5 + 6;
    </script>
  </body>
</html>
```

### Using `document.write()`

For testing purposes, it is convenient to use `document.write()`

```html
<!DOCTYPE html>
<html>
  <body>
    <h1>My First Web Page</h1>
    <p>My first paragraph.</p>

    <script>
      document.write(5 + 6);
    </script>
  </body>
</html>
```

> Note: Using document.write() after an HTML document is loaded, will **delete all existing HTML**:

```html
<!DOCTYPE html>
<html>
  <body>
    <h1>My First Web Page</h1>
    <p>My first paragraph.</p>

    <button type="button" onclick="document.write(5 + 6)">Try it</button>
  </body>
</html>
```

> Note: The document.write() method should only be used for testing.

### Using `window.alert()`

You can use an alert box to display data:
Example

```html
<!DOCTYPE html>
<html>
  <body>
    <h1>My First Web Page</h1>
    <p>My first paragraph.</p>

    <script>
      window.alert(5 + 6);
    </script>
  </body>
</html>
```

- You can skip the `window` keyword.

- In JavaScript, the window object is the global scope object, that means that variables, properties, and methods by default belong to the window object. This also means that specifying the `window` keyword is optional:

```html
<!DOCTYPE html>
<html>
  <body>
    <h1>My First Web Page</h1>
    <p>My first paragraph.</p>

    <script>
      alert(5 + 6);
    </script>
  </body>
</html>
```

### Using `console.log()`

- For debugging purposes, you can call the `console.log()` method in the browser to display data.

```html
Example
<!DOCTYPE html>
<html>
  <body>
    <script>
      console.log(5 + 6);
    </script>
  </body>
</html>
```

### JavaScript Print

- JavaScript does not have any print object or print methods.

- You cannot access output devices from JavaScript.

- The only exception is that you can call the `window.print()` method in the browser to print the content of the current window.

Example

```html
<!DOCTYPE html>
<html>
  <body>
    <button onclick="window.print()">Print this page</button>
  </body>
</html>
```

## JavaScript Type Operators

| Operator   | Description                                                |
| ---------- | ---------------------------------------------------------- |
| typeof     | Returns the type of a variable                             |
| instanceof | Returns true if an object is an instance of an object type |

```html
typeof "" // Returns "string" typeof "John" // Returns "string" typeof "John
Doe" // Returns "string"
```

- Undefined is when the value of the datatype is not defined. To remove value set the value to undefined.
- We can do this by using `null` but null is an object type. To empty an object set it to null.

## Difference Between Undefined and Null

undefined and null are equal in value but different in type:

```js
typeof undefined; // undefined
typeof null; // object

null === undefined; // false
null == undefined; // true
```

## JS Objects

The JS Objects are stored as `name:value` pair and JS class can also have methods.

```js
var person = {
  firstName: "John",
  lastName: "Doe",
  id: 5566,
  fullName: function () {
    return this.firstName + " " + this.lastName;
  },
};
```

## The **[this](https://www.w3schools.com/js/js_this.asp)** Keyword

In a function definition, `this` refers to the "owner" of the function.

In the example above, `this` is the **person object** that "owns" the fullName function.

In other words, `this.firstName` means the `firstName` property of this object.

Read more about the `this` keyword at JS this Keyword.

### Accessing Object Methods

Following syntax is to access the method :

Syntax :
`objectName.methodName()`

If you access a method **without** the () parentheses, it will return the **function definition**:

Example

`name = person.fullName;`

> Note: Do Not Declare Strings, Numbers, and Booleans as Objects!
> When a JavaScript variable is declared with the keyword "`new`", the variable is created as an object:

```js
var x = new String(); // Declares x as a String object
var y = new Number(); // Declares y as a Number object
var z = new Boolean(); // Declares z as a Boolean object
```

> Note: Avoid `String`, `Number`, and `Boolean` objects. They complicate your code and slow down execution speed.

## JavaScript Events

HTML events are things that happens to HTML element.
When JS is used in html pages, JS can react on these events.

### HTML Events

An HTML event can be something the browser does, or something a user does.

Here are some examples of HTML events:

- An HTML web page has finished loading
- An HTML input field was changed
- An HTML button was clicked

The event handler can be added to the like this :

```js
<element event='some JavaScript'>
```

Example

```html
<button onclick="document.getElementById('demo').innerHTML = Date()">
  The time is?
</button>
```

In the next example, the code changes the content of its own element (using `this.innerHTML`):
Example :
``html
<button onclick="this.innerHTML = Date()">The time is?</button>

````
In the next example, the code changes the content of its own element (using `this.innerHTML`):
```html
<button onclick="this.innerHTML = Date()">The time is?</button>
````

JavaScript code is often several lines long. It is more common to see event attributes calling functions:
Example

```html
<button onclick="displayDate()">The time is?</button>
```

### Common HTML Events

Here is a list of some common HTML events:

| Event       | Description                                        |
| ----------- | -------------------------------------------------- |
| onchange    | An HTML element has been changed                   |
| onclick     | The user clicks an HTML element                    |
| onmouseover | The user moves the mouse over an HTML element      |
| onmouseout  | The user moves the mouse away from an HTML element |
| onkeydown   | The user pushes a keyboard key                     |
| onload      | The browser has finished loading the page          |

[ W3Schools JavaScript Reference HTML DOM Events.](https://www.w3schools.com/jsref/dom_obj_event.asp)

### What can JavaScript Do?

Event handlers can be used to handle and verify user input, user actions, and browser actions:

- Things that should be done every time a page loads
- Things that should be done when the page is closed
- Action that should be performed when a user clicks a button
- Content that should be verified when a user inputs data
- And more ...
  Many different methods can be used to let JavaScript work with events:

- HTML event attributes can execute JavaScript code directly
- HTML event attributes can call JavaScript functions
- You can assign your own event handler functions to HTML elements
- You can prevent events from being sent or being handled
- And more ...
  Six other escape sequences are valid in JavaScript:

| Code | Result               |
| ---- | -------------------- |
| \b   | Backspace            |
| \f   | Form Feed            |
| \n   | New Line             |
| \r   | Carriage Return      |
| \t   | Horizontal Tabulator |
| \v   | Vertical Tabulator   |

## String

### Breaking Long Code Lines

For best readability, programmers often like to avoid code lines longer than 80 characters.

If a JavaScript statement does not fit on one line, the best place to break it is after an operator:

Example

```html
document.getElementById("demo").innerHTML = "Hello Dolly!";
```

You can also break up a code line within a text string with a single backslash:

Example

```html
document.getElementById("demo").innerHTML = "Hello \ Dolly!";
```

> Note: The `\` method is not the preferred method. It might not have universal support.Some browsers do not allow spaces behind the `\` character.
> Example :

```html
document.getElementById("demo").innerHTML = "Hello " + "Dolly!";
```

> Note: Don't create strings as objects. It slows down execution speed. The new keyword complicates the code. This can produce some unexpected results:

## JavaScript String Methods

- String Length : `length`.
- Finding a String in a String : `indexOf()`.
  The `indexOf()` method returns the index of (the position of) the first occurrence of a specified text in a string:

```js
var str = "Please locate where 'locate' occurs!";
var pos = str.indexOf("locate");
```

The `lastIndexOf()` method returns the index of the last occurrence of a specified text in a string:
Example

```js
var str = "Please locate where 'locate' occurs!";
var pos = str.lastIndexOf("locate");
```

> Note: Both indexOf(), and lastIndexOf() return -1 if the text is not found.

Both methods accept a second parameter as the starting position for the search:
Example

```js
var str = "Please locate where 'locate' occurs!";
var pos = str.indexOf("locate", 15);
```

### Searching for a String in a String

The `search()` method searches a string for a specified value and returns the position of the match:

Example

```js
var str = "Please locate where 'locate' occurs!";
var pos = str.search("locate");
```
### Did You Notice?
The two methods, `indexOf()` and `search()`, are equal?

They accept the same arguments (parameters), and return the same value?

The two methods are NOT equal. These are the differences:

* The `search()` method cannot take a second start position argument.
* The `indexOf()` method cannot take powerful search values (regular expressions).
You will learn more about regular expressions in a later chapter.

### There are 3 methods for extracting a part of a string:

* slice(start, end)
* substring(start, end)
* substr(start, length)
### The `slice()` Method
```js
var str = "Apple, Banana, Kiwi";
var res = str.slice(7, 13);
```
If a parameter is negative, the position is counted from the end of the string.

This example slices out a portion of a string from position -12 to position -6:

```js
var str = "Apple, Banana, Kiwi";
var res = str.slice(-12, -6);
```