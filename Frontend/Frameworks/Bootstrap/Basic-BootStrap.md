# [Bootstrap](https://www.freecodecamp.org/learn/front-end-libraries/bootstrap/) :

To add bootstrap to any project add this meta tag :

```html
<link
  rel="stylesheet"
  href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css"
  integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u"
  crossorigin="anonymous"
/>
```

> Note: The `bootstrap` predefined classes are need to be used in the `div` tag.

## Bootstrap classes :

- `container-fluid` - All the tags that is inside body should be wrapped inside the `div` and `container-fluid` should be applied.

* `img-responsive` : To make image responsive we can use this class inside the `img` tag.

* `text-center` : TO make get the text in center.

### Buttons :

- `btn` and `btn-default` : To make the normal button with padding.

* `btn-block` : To make the button block level.

* `btn-primary` : To give the primary color which we are using in app.

* `btn-info`: To create a info button.

* `btn-danger` : T0 create a button of different color or danger.

Bootstrap uses a responsive 12-column grid system, which makes it easy to put elements into rows and specify each element's relative width. Most of Bootstrap's classes can be applied to a `div` element.

- `col-md-*` : Here `md` means the medium and `*` is how many column wide.

- `col-xs-*` : Here `xs` means `extra small` and `*` is column size.

* `row` : this is to make a row.

* `text-primary` : This will give the primary color to the text.

* `text-danger` : This will give the text red color.

* [Create a Custom HeadingPassed](https://www.freecodecamp.org/learn/front-end-libraries/bootstrap/create-a-custom-heading)

## Adding [Font awesome icons](<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.8.1/css/all.css" integrity="sha384-50oBUHEmvpQ+1lW4y57PTFmhCaXp0ML5d60M1M7uH2+nqUivzIebhndOJK28anvf" crossorigin="anonymous">) :

`<i class="fas fa-thumbs-up"></i>`

`<i class="fas fa-info-circle"></i>`

`<i class="fas fa-trash"></i>`

- [Responsively Style Radio Buttons](https://www.freecodecamp.org/learn/front-end-libraries/bootstrap/responsively-style-radio-buttons)

* [Style Text Inputs as Form Controls](https://www.freecodecamp.org/learn/front-end-libraries/bootstrap/style-text-inputs-as-form-controls)

* `form-control` : All textual <input>, <textarea>, and <select> elements with the class .form-control have a width of 100%.

* [Line up Form Elements Responsively with Bootstrap](https://www.freecodecamp.org/learn/front-end-libraries/bootstrap/line-up-form-elements-responsively-with-bootstrap).

* `well` : Bootstrap has a class called well that can create a visual sense of depth for your columns.

> Note: Not every class needs to have corresponding CSS. Sometimes we create classes just for the purpose of selecting these elements more easily using jQuery.
