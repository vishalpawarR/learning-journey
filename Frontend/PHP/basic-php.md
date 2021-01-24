# PHP

- PHP is one of the server side scripting language and the php code run on server.

- We write the php code inside a `<?php ?>` tag inside the html and the file has an extension of `.php`.

## PHP case sensitivity :

- The php is the `keywords`, `classes`, `functions`, and `user defined function` are not case sensitive.

EX :

```php
<!DOCTYPE html>
<html>
<body>

<?php
ECHO "Hello World!<br>";
echo "Hello World!<br>";
EcHo "Hello World!<br>";
?>

</body>
</html>
```

> Note: variables are case sensitive color, COLOR are both are different.

## Comments in PHP :

- The php has single-line comment and multiline comment.

```php
// Single line comment
/*
This is an multiline comment
*/
```

## Variables in PHP :

- The variables of php starts with an `$` sign to use the variable also we need to use the `$` sign to access the variable value.

```php
<?php
$x = 5;
$y = 4;
echo $x + $y;
?>
```

### Variable scopes :

- PHP has three variable scope.

1. Local
2. Global
3. Static

4. Local - The local variable are declared with in a method is called as a local variable.

5. Global - The global variables are declared outside the function.

```php
<?php
$x = 5; // global scope

function myTest() {
  // using x inside this function will generate an error
  echo "<p>Variable x inside function is: $x</p>";
}
myTest();

echo "<p>Variable x outside function is: $x</p>";
?>
```

### `global` keyword :

- The global keyword is used to access the global variable from the local scope.

```php
<?php
$x = 5;
$y = 10;

function myTest() {
  global $x, $y;
  $y = $x + $y;
}

myTest();
echo $y; // outputs 15
?>
```

### `GLOBALS` array :

- The php stores the global variables inside an array called GLOBALS array and we can access them using the indexes in the place of index pass the variable name.
  We can write the above example like this

```php
<?php
$x = 5;
$y = 10;

function myTest() {
  $GLOBALS['y'] = $GLOBALS['x'] + $GLOBALS['y'];
}

myTest();
echo $y; // outputs 15
?>
```

### `static` variable :

- We can declare the variable as static using the `static` keyword.

```php
<!DOCTYPE html>
<html>
<body>

<?php
function myTest() {
  static $x = 0;
  echo $x;
  $x++;
}

myTest();
echo "<br>";
myTest();
echo "<br>";
myTest();
?>

</body>
</html>
```

### `echo` and `print` :

- The both of them does the same work there are only some minor difference in both of them.

#### `echo` vs `print`

- echo doesn't return any value and print returns a value `1` so it can be used in expression.
- echo can take multiple parameters (although such usage is rare) while print can take one argument. echo is marginally faster than print.

## PHP Datatype :

- The following are the datatype of the php

1. String
2. Integer
3. Float(Double)
4. Boolean
5. Array
6. Object
7. NULL
8. Resources

> Note: The datatype of the variable can be found programmatically using the `var_dump()` and value.

### String :

- Methods of the strings
  - `strlen()` : returns length of the string.
  ```php
  <?php
  echo strlen("Hello world!"); // outputs 12
  ?>
  ```
  - `str_word_count()` : return no of words in given string.
  ```php
  <?php
  echo str_word_count("Hello world!"); // outputs 2
  ?>
  ```
  - `strrev()` : returns reversed string.
  ```php
  <?php
  echo strrev("Hello world!"); // outputs !dlrow olleH
  ?>
  ```
  - `strpos()` : search for the given string and return position if found else it will return false.
  ```php
  <?php
  echo strpos("Hello world!", "world"); // outputs 6
  ?>
  ```
  - `str_replace()` : Replaces text with in string.
  ```php
  <?php
  echo str_replace("world", "Dolly", "Hello world!"); // outputs Hello Dolly!
  ?>
  ```

### [PHP String Functions](https://www.w3schools.com/php/php_ref_string.asp)

## Numbers :

### Integer :

- PHP has the following functions to check if the type of a variable is integer:

1. is_int()
2. is_integer() - alias of is_int()
3. is_long() - alias of is_int()

```php
<?php
$x = 5985;
var_dump(is_int($x));

$x = 59.85;
var_dump(is_int($x));
?>
```

### Float :

- PHP has the following functions to check if the type of a variable is float:

1. is_float()
2. is_double() - alias of is_float()

```php
<?php
$x = 10.365;
var_dump(is_float($x));
?>
```

### PHP Infinity

- value larger than the `PHP_FLOAT_MAX` is considered as the infinity.
- PHP has the following functions to check if a numeric value is finite or infinite:

1. is_finite()
2. is_infinite()

```php
<?php
$x = 1.9e411;
var_dump($x);
?>
```

### PHP NaN :

- Not a number which will come when the impossible mathematical operation will come.
- PHP has the following functions to check if a value is not a number:

1. is_nan()

```php
<?php
$x = acos(8);
var_dump($x);
?>
```

### PHP numerical string :

- The PHP `is_numeric()` function can be used to find whether a variable is numeric. The function returns true if the variable is a number or a numeric string, false otherwise.

```php
<?php
$x = 5985;
var_dump(is_numeric($x));

$x = "5985";
var_dump(is_numeric($x));

$x = "59.85" + 100;
var_dump(is_numeric($x));

$x = "Hello";
var_dump(is_numeric($x));
?>
```

> Note: From PHP 7.0: The is_numeric() function will return FALSE for numeric strings in hexadecimal form (e.g. 0xf4c3b00c), as they are no longer considered as numeric strings.

## Type Casting :

## To Integer :

- Sometimes you need to cast a numerical value into another data type.

- The `(int)`, `(integer)`, or `intval()` function are often used to convert a value to an integer.

```php
<?php
// Cast float to int
$x = 23465.768;
$int_cast = (int)$x;
echo $int_cast;

echo "<br>";

// Cast string to int
$x = "23465.768";
$int_cast = (int)$x;
echo $int_cast;
?>
```

## PHP Math :

These are some of the useful to perform the task.

- `pi()` : Returns value of pi.

```php
<?php
echo(pi()); // returns 3.1415926535898
?>
```

- `min()` and `max()` :

```php
<?php
echo(min(0, 150, 30, 20, -8, -200));  // returns -200
echo(max(0, 150, 30, 20, -8, -200));  // returns 150
?>
```

- `abs()` returns positive absolute value.

```php
<?php
echo(abs(-6.7));  // returns 6.7
?>
```

- `sqrt()` : Returns the square root value.

```php
<?php
echo(sqrt(64));  // returns 8
?>
```

- `round()` : Round off the number.

```php
<?php
echo(round(0.60));  // returns 1
echo(round(0.49));  // returns 0
?>
```

- `rand()` : returns random number.

```php
<?php
echo(rand());
?>
```

### [PHP Math Reference](https://www.w3schools.com/php/php_ref_math.asp)

## PHP Constants

- A constant is an identifier (name) for a simple value. The value cannot be changed during the script.

- A valid constant name starts with a letter or underscore (no $ sign before the constant name).

> Note: Unlike variables, constants are automatically global across the entire script.

SYNTAX :

```php
define(name, value, case-insensitive)
```

name : specify the name of the constant i.e., variable name.

value : specify the value of the constant.

case-insensitive : default value is False.

```php
<?php
define("GREETING", "Welcome to W3Schools.com!");
echo GREETING;
?>
```

> Note : constants are global variable.

## PHP Operators :

- Exponential operator : `**`.

### Comparison operator :

| Operator | Name                     | Example   | Result                                                                                                                                            |
| -------- | ------------------------ | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| ==       | Equal                    | $x == $y  | Returns true if $x is equal to $y                                                                                                                 |
| ===      | Identical                | $x === $y | Returns true if $x is equal to $y, and they are of the same type                                                                                  |
| !=       | Not equals               | $x != $y  | Returns true if $x is not equal to $y                                                                                                             |
| <>       | Not equals               | $x <> $y  | Returns true if $x is not equal to $y                                                                                                             |
| !==      | Not identical            | $x !== $y | Returns true if $x is not equal to $y, or they are not of the same type                                                                           |
| >        | Greater than             | $x > $y   | Returns true if $x is greater than $y                                                                                                             |
| <        | Less than                | $x < $y   | Returns true if $x is less than $y                                                                                                                |
| >=       | Greater than or Equal to | $x >= $y  | Returns true if $x is greater than or equal to $y                                                                                                 |
| <=       | Less than or Equal to    | $X <= $y  | Returns true if $x is less than or equal to $y                                                                                                    |
| <=>      | Spaceship                | $x <=> $y | Returns an integer less than, equal to, or greater than zero, depending on if $x is less than, equal to, or greater than $y. Introduced in PHP 7. |

|

### Logical operators

| Operator | Name | Example    | Results                                       |
| -------- | ---- | ---------- | --------------------------------------------- |
| and      | And  | $x and $y  | True if both $x and $y are true               |
| or       | Or   | $x or $y   | True if either $x or $y is true               |
| xor      | Xor  | $x xor $y  | True if either $x or $y is true, but not both |
| &&       | And  | $x && $y   | True if both $x and $y are true               |
| \|\|     | Or   | $x \|\| $y | True if either $x or $y is true               |
| !        | Not  | !$x        | True if $x is not true                        |

### PHP String Operators

| Operator | Name                     | Example        | Result                           |
| -------- | ------------------------ | -------------- | -------------------------------- |
| .        | Concatenation            | $txt1 . $txt2  | Concatenation of $txt1 and $txt2 |
| .=       | Concatenation assignment | $txt1 .= $txt2 | Appends $txt2 to $txt1           |

### PHP Array Operators

| Operator | Name         | Example   | Result                                                                                          |
| -------- | ------------ | --------- | ----------------------------------------------------------------------------------------------- |
| +        | Union        | $x + $y   | Union of $x and $y                                                                              |
| ==       | Equality     | $x == $y  | Returns true if $x and $y have the same key/value pairs                                         |
| ===      | Identity     | $x === $y | Returns true if $x and $y have the same key/value pairs in the same order and of the same types |
| !=       | Inequality   | $x != $y  | Returns true if $x is not equal to $y                                                           |
| <>       | Inequality   | $x <> $y  | Returns true if $x is not equal to $y                                                           |
| !==      | Non-identity | $x !== $y | Returns true if $x is not identical to $y                                                       |

### PHP Conditional Assignment Operators

| Operator | Name            | Example                    | Result                                                                                                                                                              |
| -------- | --------------- | -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ?:       | Ternary         | $x = expr1 ? expr2 : expr3 | Returns the value of $x. The value of $x is expr2 if expr1 = TRUE. The value of $x is expr3 if expr1 = FALSE                                                        |
| ??       | Null coalescing | $x = expr1 ?? expr2        | Returns the value of $x.The value of $x is expr1 if expr1 exists, and is not NULL.If expr1 does not exist, or is NULL, the value of $x is expr2.Introduced in PHP 7 |

## PHP if else :

Syntax

```php
if (condition) {
  code to be executed if this condition is true;
} elseif (condition) {
  code to be executed if first condition is false and this condition is true;
} else {
  code to be executed if all conditions are false;
}
```

## PHP Switch :

```php
switch (n) {
  case label1:
    code to be executed if n=label1;
    break;
  case label2:
    code to be executed if n=label2;
    break;
  case label3:
    code to be executed if n=label3;
    break;
    ...
  default:
    code to be executed if n is different from all labels;
}
```

## PHP Loops

Loops are used to do same task multiple times until the condition is true.

### The PHP while Loop

```php
while (condition is true) {
  code to be executed;
}
```

### PHP do while Loop

```php
do {
  code to be executed;
} while (condition is true);
```

### The PHP for Loop

```php
for (init counter; test counter; increment counter) {
  code to be executed for each iteration;
}
```

### The PHP foreach Loop

```php
foreach ($array as $value) {
  code to be executed;
}
```

## PHP Functions

PHP is having more than 1000 [built in functions](https://www.w3schools.com/php/php_ref_overview.asp).

```php
function functionName() {
  code to be executed;
}
```

The PHP is a loosely typed language and We don't declare the data type of the variable.
if we add int and string it will not give any error. like an below example.

```php
<?php
function addNumbers(int $a, int $b) {
  return $a + $b;
}
echo addNumbers(5, "5 days");
// since strict is NOT enabled "5 days" is changed to int(5), and it will return 10
?>
```

### STRICT typing

- We can make this datatype matching we can use `strict` to match the datatype and This will throw `Fatal error` if the both the datatype is not matched and to make it use the strict we use `declare(strict_type=1)`.

```php
<?php declare(strict_types=1); // strict requirement

function addNumbers(int $a, int $b) {
  return $a + $b;
}
echo addNumbers(5, "5 days");
// since strict is enabled and "5 days" is not an integer, an error will be thrown
?>
```

> Note : The strict declaration forces things to be used in the intended way.

### PHP Default Argument Value

- In the the method arguments will have default value. If we didn't pass the value then it will take the default value.

```php
<?php declare(strict_types=1); // strict requirement
function setHeight(int $minheight = 50) {
  echo "The height is : $minheight <br>";
}

setHeight(350);
setHeight(); // will use the default value of 50
setHeight(135);
setHeight(80);
?>
```

### PHP Return Type Declarations

To return the value from the function we use the `return` keyword to make the method to return the specified type of the value like the strict variable check.

- We can return the specified type of the value by mentioning the return type when declaring the method by using ( `:` ) before start of curly braces ( `{ }` ) i.e., method body as shown in below example.

```php
<?php declare(strict_types=1); // strict requirement
function addNumbers(float $a, float $b) : float {
  return $a + $b;
}
echo addNumbers(1.2, 5.2);
?>
```

### Passing Arguments by Reference

- When ever we pass an argument or variable to the method the method will have it's own copy of the value and it will not effect the variable value which we passed in the method as an argument.
  \*If we want to update the value after method operation we can pass it as an reference after the operation the value is updated. We can do this by using the `&` to pass by reference below example to learn more.

```php
<?php
function add_five(&$value) {
  $value += 5;
}

$num = 2;
add_five($num);
echo $num;
?>
```

## PHP Arrays

In PHP we use `array()` to create an array.

```php
<?php
$cars = array("Volvo", "BMW", "Toyota");
echo "I like " . $cars[0] . ", " . $cars[1] . " and " . $cars[2] . ".";
?>
```

In PHP, there are three types of arrays:

**Indexed arrays** - Arrays with a numeric index
**Associative arrays** - Arrays with named keys
**Multidimensional arrays** - Arrays containing one or more arrays

- TO find the array length we use the `count()` to find the length of an array.

#### [PHP Array Reference](https://www.w3schools.com/php/php_ref_array.asp)

### Associative Array

- In this the value are stored as same key and value pair.
  There are two ways to create an associative array:

```php
$age = array("Peter"=>"35", "Ben"=>"37", "Joe"=>"43");
//or:

$age['Peter'] = "35";
$age['Ben'] = "37";
$age['Joe'] = "43";
```

Loop through array using for each

```php
<?php
$age = array("Peter"=>"35", "Ben"=>"37", "Joe"=>"43");

foreach($age as $x => $x_value) {
  echo "Key=" . $x . ", Value=" . $x_value;
  echo "<br>";
}
?>
```

## PHP Sorting Arrays

We will go through the following PHP array sort functions:
Method Name | Description |
|----------|----------|
sort() | sort arrays in ascending order
rsort() | sort arrays in descending order
asort() | sort associative arrays in ascending order, according to the value
ksort() | sort associative arrays in ascending order, according to the key
arsort() | sort associative arrays in descending order, according to the value
krsort() | sort associative arrays in descending order, according to the key

## PHP Global Variables - Superglobals

Some predefined variables in PHP are "superglobals", which means that they are always accessible, regardless of scope - and you can access them from any function, class or file without having to do anything special.

The PHP superglobal variables are:

- $GLOBALS
- $\_SERVER
- $\_REQUEST
- $\_POST
- $\_GET
- $\_FILES
- $\_ENV
- $\_COOKIE
- $\_SESSION

### [PHP Superglobal - $\_SERVER](https://www.w3schools.com/php/php_superglobals_server.asp)

- $\_SERVER is a PHP super global variable which holds information about headers, paths, and script locations.

The example below shows how to use some of the elements in $\_SERVER:

Example

```php
<?php
echo $_SERVER['PHP_SELF'];
echo "<br>";
echo $_SERVER['SERVER_NAME'];
echo "<br>";
echo $_SERVER['HTTP_HOST'];
echo "<br>";
echo $_SERVER['HTTP_REFERER'];
echo "<br>";
echo $_SERVER['HTTP_USER_AGENT'];
echo "<br>";
echo $_SERVER['SCRIPT_NAME'];
?>
```

### [PHP Superglobal - $\_REQUEST](https://www.w3schools.com/php/php_superglobals_request.asp)

PHP $\_REQUEST is a PHP super global variable which is used to collect data after submitting an HTML form.

The example below shows a form with an input field and a submit button. When a user submits the data by clicking on "Submit", the form data is sent to the file specified in the action attribute of the <form> tag. In this example, we point to this file itself for processing form data. If you wish to use another PHP file to process form data, replace that with the filename of your choice. Then, we can use the super global variable $\_REQUEST to collect the value of the input field:

Example

```php
<html>
<body>

<form method="post" action="<?php echo $_SERVER['PHP_SELF'];?>">
  Name: <input type="text" name="fname">
  <input type="submit">
</form>

<?php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
  // collect value of input field
  $name = $_REQUEST['fname'];
  if (empty($name)) {
    echo "Name is empty";
  } else {
    echo $name;
  }
}
?>

</body>
</html>
```

### [PHP Superglobal - $\_POST](https://www.w3schools.com/php/php_superglobals_post.asp)

PHP $\_POST is a PHP super global variable which is used to collect form data after submitting an HTML form with method="post". $\_POST is also widely used to pass variables.

The example below shows a form with an input field and a submit button. When a user submits the data by clicking on "Submit", the form data is sent to the file specified in the action attribute of the <form> tag. In this example, we point to the file itself for processing form data. If you wish to use another PHP file to process form data, replace that with the filename of your choice. Then, we can use the super global variable $\_POST to collect the value of the input field:

Example

```php
<html>
<body>

<form method="post" action="<?php echo $_SERVER['PHP_SELF'];?>">
  Name: <input type="text" name="fname">
  <input type="submit">
</form>

<?php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
  // collect value of input field
  $name = $_POST['fname'];
  if (empty($name)) {
    echo "Name is empty";
  } else {
    echo $name;
  }
}
?>

</body>
</html>
```

### [PHP Superglobal - $\_GET](https://www.w3schools.com/php/php_superglobals_get.asp)

PHP $\_GET is a PHP super global variable which is used to collect form data after submitting an HTML form with method="get".

$\_GET can also collect data sent in the URL.

Assume we have an HTML page that contains a hyperlink with parameters:

```php
<html>
<body>

<a href="test_get.php?subject=PHP&web=W3schools.com">Test $GET</a>

</body>
</html>
```

When a user clicks on the link "Test $GET", the parameters "subject" and "web" are sent to "test_get.php", and you can then access their values in "test_get.php" with $\_GET.

The example below shows the code in "test_get.php":

Example

```php
<html>
<body>

<?php
echo "Study " . $_GET['subject'] . " at " . $_GET['web'];
?>

</body>
</html>
```
