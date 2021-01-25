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

## OOPS

### Defining a class

```php
<?php
class Fruit {
  // code goes here...
}
?>
```

### Example

```php
<?php
class Fruit {
  // Properties
  public $name;
  public $color;

  // Methods
  function set_name($name) {
    $this->name = $name;
  }
  function get_name() {
    return $this->name;
  }
}
?>
```

### Creating the Object of the class

```php
<?php
class Fruit {
  // Properties
  public $name;
  public $color;

  // Methods
  function set_name($name) {
    $this->name = $name;
  }
  function get_name() {
    return $this->name;
  }
}

$apple = new Fruit();
$banana = new Fruit();
$apple->set_name('Apple');
$banana->set_name('Banana');

echo $apple->get_name();
echo "<br>";
echo $banana->get_name();
?>
```

### PHP - The $this Keyword

The $this keyword refers to the current object, and is only available inside methods.

### PHP - `instanceof`

You can use the `instanceof` keyword to check if an object belongs to a specific class:

```php
<?php
$apple = new Fruit();
var_dump($apple instanceof Fruit);
?>
```

## Constructor `__constructor()`

Example

```php
<?php
class Fruit {
  public $name;
  public $color;

  function __construct($name) {
    $this->name = $name;
  }
  function get_name() {
    return $this->name;
  }
}

$apple = new Fruit("Apple");
echo $apple->get_name();
?>
```

## Destructors `__destructor()`

The destructor is called at the end of the script automatically.

```php
<?php
class Fruit {
  public $name;
  public $color;

  function __construct($name) {
    $this->name = $name;
  }
  function __destruct() {
    echo "The fruit is {$this->name}.";
  }
}

$apple = new Fruit("Apple");
?>
```

## Access Modifiers

Properties and methods can have access modifiers to specify their access.

- `public`
- `protected`
- `private`

```php
<?php
class Fruit {
  public $name;
  protected $color;
  private $weight;
}

$mango = new Fruit();
$mango->name = 'Mango'; // OK
$mango->color = 'Yellow'; // ERROR
$mango->weight = '300'; // ERROR
?>
```

## Inheritance

The inheritance occurs using the `extends` keyword.

> Note: PHP only supports single inheritance.

```php
<?php
class Fruit {
  public $name;
  public $color;
  public function __construct($name, $color) {
    $this->name = $name;
    $this->color = $color;
  }
  public function intro() {
    echo "The fruit is {$this->name} and the color is {$this->color}.";
  }
}

// Strawberry is inherited from Fruit
class Strawberry extends Fruit {
  public function message() {
    echo "Am I a fruit or a berry? ";
  }
}
$strawberry = new Strawberry("Strawberry", "red");
$strawberry->message();
$strawberry->intro();
?>
```

### PHP - Overriding Inherited Methods

Look at the example below. The **construct() and intro() methods in the child class (Strawberry) will override the **construct() and intro() methods in the parent class (Fruit):

```php
<?php
class Fruit {
  public $name;
  public $color;
  public function __construct($name, $color) {
    $this->name = $name;
    $this->color = $color;
  }
  public function intro() {
    echo "The fruit is {$this->name} and the color is {$this->color}.";
  }
}

class Strawberry extends Fruit {
  public $weight;
  public function __construct($name, $color, $weight) {
    $this->name = $name;
    $this->color = $color;
    $this->weight = $weight;
  }
  public function intro() {
    echo "The fruit is {$this->name}, the color is {$this->color}, and the weight is {$this->weight} gram.";
  }
}

$strawberry = new Strawberry("Strawberry", "red", 50);
$strawberry->intro();
?>
```

### PHP - The final Keyword

The `final` keyword can be used to prevent class inheritance or to prevent method overriding.

```php
<?php
final class Fruit {
  // some code
}

// will result in error
class Strawberry extends Fruit {
  // some code
}
?>
```

Method Overriding

```php
<?php
class Fruit {
  final public function intro() {
    // some code
  }
}

class Strawberry extends Fruit {
  // will result in error
  public function intro() {
    // some code
  }
}
?>
```

## PHP - Class Constants

- Constants cannot be changed once it is declared.

- Class constants can be useful if you need to define some constant data within a class.

- A class constant is declared inside a `class` with the const keyword.

- Class constants are case-sensitive. However, it is recommended to name the constants in all uppercase letters.

- We can access a constant from outside the class by using the class name followed by the **scope resolution operator** (`::`) followed by the constant name, like here:

Example

```php
<?php
class Goodbye {
  const LEAVING_MESSAGE = "Thank you for visiting W3Schools.com!";
}

echo Goodbye::LEAVING_MESSAGE;
?>
```

Or, we can access a constant from inside the class by using the `self` keyword followed by the scope resolution operator (::) followed by the constant name, like here:

```php
<?php
class Goodbye {
  const LEAVING_MESSAGE = "Thank you for visiting W3Schools.com!";
  public function byebye() {
    echo self::LEAVING_MESSAGE;
  }
}

$goodbye = new Goodbye();
$goodbye->byebye();
?>
```

## Abstract Classes and Methods

- An abstract class is a class that contains at least one abstract method. An abstract method is a method that is declared, but not implemented in the code.

- An abstract class or method is defined with the `abstract` keyword:

```php
<?php
abstract class ParentClass {
  abstract public function someMethod1();
  abstract public function someMethod2($name, $color);
  abstract public function someMethod3() : string;
}
?>
```

When inheriting from an abstract class, the child class method must be defined with the same name, and the same or a less restricted access modifier. So, if the abstract method is defined as protected, the child class method must be defined as either protected or public, but not private. Also, the type and number of required arguments must be the same. However, the child classes may have optional arguments in addition.

So, when a child class is inherited from an abstract class, we have the following rules:

- The child class method must be defined with the same name and it redeclares the parent abstract method
- The child class method must be defined with the same or a less restricted access modifier
- The number of required arguments must be the same. However, the child class may have optional arguments in addition

Let's look at an example:

Example

```php
<?php
// Parent class
abstract class Car {
  public $name;
  public function __construct($name) {
    $this->name = $name;
  }
  abstract public function intro() : string;
}

// Child classes
class Audi extends Car {
  public function intro() : string {
    return "Choose German quality! I'm an $this->name!";
  }
}

class Volvo extends Car {
  public function intro() : string {
    return "Proud to be Swedish! I'm a $this->name!";
  }
}

class Citroen extends Car {
  public function intro() : string {
    return "French extravagance! I'm a $this->name!";
  }
}

// Create objects from the child classes
$audi = new audi("Audi");
echo $audi->intro();
echo "<br>";

$volvo = new volvo("Volvo");
echo $volvo->intro();
echo "<br>";

$citroen = new citroen("Citroen");
echo $citroen->intro();
?>
```

Let's look at another example where the abstract method has an argument, and the child class has two optional arguments that are not defined in the parent's abstract method:

```php
<?php
abstract class ParentClass {
  // Abstract method with an argument
  abstract protected function prefixName($name);
}

class ChildClass extends ParentClass {
  // The child class may define optional arguments that are not in the parent's abstract method
  public function prefixName($name, $separator = ".", $greet = "Dear") {
    if ($name == "John Doe") {
      $prefix = "Mr";
    } elseif ($name == "Jane Doe") {
      $prefix = "Mrs";
    } else {
      $prefix = "";
    }
    return "{$greet} {$prefix}{$separator} {$name}";
  }
}

$class = new ChildClass;
echo $class->prefixName("John Doe");
echo "<br>";
echo $class->prefixName("Jane Doe");
?>
```

## PHP OOP - Interfaces

Interfaces are declared with the `interface` keyword:

```php
<?php
interface InterfaceName {
  public function someMethod1();
  public function someMethod2($name, $color);
  public function someMethod3() : string;
}
?>
```

### PHP - Interfaces vs. Abstract Classes

Interface are similar to abstract classes. The difference between interfaces and abstract classes are:

- Interfaces cannot have properties, while abstract classes can
- All interface methods must be public, while abstract class methods is public or protected
- All methods in an interface are abstract, so they cannot be implemented in code and the abstract keyword is not necessary
- Classes can implement an interface while inheriting from another class at the same time

### PHP - Using Interfaces

To implement an interface, a class must use the `implements` keyword.

```php
<?php
interface Animal {
  public function makeSound();
}

class Cat implements Animal {
  public function makeSound() {
    echo "Meow";
  }
}

$animal = new Cat();
$animal->makeSound();
?>
```

## PHP OOP - Traits

PHP - What are Traits?
PHP only **supports** `single inheritance`: a child class can inherit only from one single parent.

- So, what if a class needs to inherit multiple behaviors? OOP traits solve this problem.

- Traits are used to declare methods that can be used in multiple classes. Traits can have methods and abstract methods that can be used in multiple classes, and the methods can have any access modifier (public, private, or protected).

- Traits are declared with the `trait` keyword:

Syntax

```php
<?php
trait TraitName {
  // some code...
}
?>
```

To use a trait in a class, use the `use` keyword:

```php
<?php
class MyClass {
  use TraitName;
}
?>
```

example

```php
<?php
trait message1 {
public function msg1() {
    echo "OOP is fun! ";
  }
}

class Welcome {
  use message1;
}

$obj = new Welcome();
$obj->msg1();
?>
```

Using Multiple Traits

```php
<?php
trait message1 {
  public function msg1() {
    echo "OOP is fun! ";
  }
}

trait message2 {
  public function msg2() {
    echo "OOP reduces code duplication!";
  }
}

class Welcome {
  use message1;
}

class Welcome2 {
  use message1, message2;
}

$obj = new Welcome();
$obj->msg1();
echo "<br>";

$obj2 = new Welcome2();
$obj2->msg1();
$obj2->msg2();
?>
```

## Static Methods

Static methods can be called directly - without creating an instance of the class first.

Static methods are declared with the `static` keyword:

Syntax

```php
<?php
class ClassName {
  public static function staticMethod() {
    echo "Hello World!";
  }
}
?>
```

To access a static method use the class name, double colon (`::`), and the method name:
Syntax

```php
ClassName::staticMethod();
```

Example

```php
<?php
class greeting {
  public static function welcome() {
    echo "Hello World!";
  }
}

// Call static method
greeting::welcome();
?>
```

A class can have both static and non-static methods. A static method can be accessed from a method in the same class using the `self` keyword and double colon (::):

```php
Example
<?php
class greeting {
  public static function welcome() {
    echo "Hello World!";
  }

  public function __construct() {
    self::welcome();
  }
}

new greeting();
?>
```

Static methods can also be called from methods in other classes. To do this, the static method should be `public`:

Example

```php
<?php
class greeting {
  public static function welcome() {
    echo "Hello World!";
  }
}

class SomeOtherClass {
  public function message() {
    greeting::welcome();
  }
}
?>
```

To call a static method from a child class, use the `parent` keyword inside the child class. Here, the static method can be `public` or `protected`.

Example

```php
<?php
class domain {
  protected static function getWebsiteName() {
    return "W3Schools.com";
  }
}

class domainW3 extends domain {
  public $websiteName;
  public function __construct() {
    $this->websiteName = parent::getWebsiteName();
  }
}

$domainW3 = new domainW3;
echo $domainW3 -> websiteName;
?>
```

## PHP - Static Properties

Static properties can be called directly - without creating an instance of a class.

Static properties are declared with the `static` keyword:

Syntax

```php
<?php
class ClassName {
  public static $staticProp = "W3Schools";
}
?>
```

To access a static property use the class name, double colon (::), and the property name:

Syntax

```php
ClassName::staticProp;
```

Example

```php
<?php
class pi {
  public static $value = 3.14159;
}

// Get static property
echo pi::$value;
?>
```

A class can have both static and non-static properties. A static property can be accessed from a method in the same class using the `self` keyword and double colon (`::`):

Example

```php
<?php
class pi {
  public static $value=3.14159;
  public function staticValue() {
    return self::$value;
  }
}

$pi = new pi();
echo $pi->staticValue();
?>
```

To call a static property from a child class, use the `parent` keyword inside the child class:

Example

```php
<?php
class pi {
  public static $value=3.14159;
}

class x extends pi {
  public function xStatic() {
    return parent::$value;
  }
}

// Get value of static property directly via child class
echo x::$value;

// or get value of static property via xStatic() method
$x = new x();
echo $x->xStatic();
?>
```

## PHP Namespaces
Namespaces are qualifiers that solve two different problems:

1. They allow for better organization by grouping classes that work together to perform a task.
2. They allow the same name to be used for more than one class.

* For example, you may have a set of classes which describe an HTML table, such as Table, Row and Cell while also having another set of classes to describe furniture, such as Table, Chair and Bed. Namespaces can be used to organize the classes into two different groups while also preventing the two classes Table and Table from being mixed up.
### Declaring a Namespace
Namespaces are declared at the beginning of a file using the `namespace` keyword:

Syntax
Declare a namespace called Html:
```php
namespace Html;
```
> Note: Note: A `namespace` declaration must be the first thing in the PHP file. The following code would be invalid:

Constants, classes and functions declared in this file will belong to the Html namespace:

Example
Create a Table class in the Html namespace:
```php
<?php
namespace Html;
class Table {
  public $title = "";
  public $numRows = 0;
  public function message() {
    echo "<p>Table '{$this->title}' has {$this->numRows} rows.</p>";
  }
}
$table = new Table();
$table->title = "My table";
$table->numRows = 5;
?>

<!DOCTYPE html>
<html>
<body>

<?php
$table->message();
?>

</body>
</html>
```
For further organization, it is possible to have nested namespaces:

Syntax
Declare a namespace called Html inside a namespace called Code:
```php
namespace Code\Html;
```
### Using Namespaces
Any code that follows a `namespace` declaration is operating inside the namespace, so classes that belong to the namespace can be instantiated without any qualifiers. To access classes from outside a namespace, the class needs to have the namespace attached to it.

Example
Use classes from the Html namespace:
```php
$table = new Html\Table()
$row = new Html\Row();
```
When many classes from the same namespace are being used at the same time, it is easier to use the namespace keyword:

