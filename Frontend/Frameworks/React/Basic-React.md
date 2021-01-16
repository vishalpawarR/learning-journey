# React

- React combines `HTML` with `JavaScript` to create it own markup language `JSX`.
- React uses the syntax extension of JavaScript called as `JSX`.This allows us to write `HTML` inside JavaScript.

* We can write the JavaScript inside the `JSX` directly just include it in the curly braces `{}`.

```jsx
{
  ("code inside this treated as the javascript");
}
```

- JSX is not a valid JS. JSX need to be compiled into JS.We can do this using the transpiler `Babel` is the most popular one you can use.

- It's worth noting that under the hood the challenges are calling `ReactDOM.render(JSX, document.getElementById('root'))`. This function call is what places your JSX into React's own lightweight representation of the DOM. React then uses snapshots of its own DOM to optimize updating only specific parts of the actual DOM.

## Nested JSX

- The nested JSX must return only one element.
  Invalid JSX:

```JSX
<p>Paragraph One</p>
<p>Paragraph Two</p>
<p>Paragraph Three</p>
```

The above code should be wrapped under one single parent.

```JSX
<div>
    <p>One</p>
    <p>Two</p>
    <p>There</p>
</div>
```

## Comment in JSX :

The comment in JSX are written in curly braces `{/* */}`

```jsx
{
  /*This is an comment */
}
```

## Render HTML Elements to the DOM

- We have learnt that using JSX we can write readable code inside the JavaScript. With react We can render the HTML this JSX directly to the HTML DOM using the React's rendering API Known as `ReactDOM`.

- `ReactDOM` offers a simple method to render react element to the DOM which look like this `ReactDOM.render(componentToRender, targetNode)` here the first argument is the react element or component you want to render and second argument is DOM node we want to render the component to.

## Defining class in HTML

- The key difference between HTML and JSX is that we can no longer use the `class` to define the HTML classes because in the `JS` the `class` is a reserved keyword.

- In JSX we use the `className` to declare the class.

* The naming convention for all HTML attributes and event reference in the `JSX` became camelCase like `onclick` as `onClick` and `onchange` as `onChange` in JSX.

## Learn About Self-Closing JSX Tags

In html we have most tags have closing tag and some of them are self closing in JSX we can write them as follows to make them self closing like this `<div></div>` as `<div />`. In this JSX self closing JSX tags we can write anything like the html tags like `<p>writing</p>`.

> Note: The HTML self closing tags need to have the forward slash `/` in JSX otherwise it will throw error.

Invalid :

```jsx
<br>
<hr>
```

Valid :

```jsx
<br />
<hr />
```

## Create a Stateless Functional Component

Component is the core of React.Everything in react is component.

### Creating the component

There are 2 ways to do so

1. Using JavaScript function.

   Defining the component this way create a _Stateless functional component_

   To create the react component create an JS function which returns `JSX` or `null`.

   > Note: If we create a react component like this React needs the function name should start with the `capital letter`.

```jsx
// After being transpiled, the <div> will have a CSS class of 'customClass'
const DemoComponent = function () {
  return <div className="customClass" />;
};
```

Example :

```jsx
const MyComponent = function () {
  return <div>VLV</div>;
};
```

> Note: we can't use the self closing tag of the JSX because the string above is considered as the child of the div tag. 2. Using ES6 `class` :
> To crete a react component the `class` should extend the `React.component`

```jsx
class Kitten extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
        return <h1>Hi</h1>;
    );
  }
}
```

Example :

```jsx
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h1>Hello V</h1>
      </div>
    );
  }
}
```

## Create a component with the composition

Example :

```jsx
const ChildComponent = () => {
  return (
    <div>
      <p>I am the child</p>
    </div>
  );
};

class ParentComponent extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h1>I am the parent</h1>
        {/* Change code below this line */}
        <ChildComponent />

        {/* Change code above this line */}
      </div>
    );
  }
}
```

## [Use React to Render Nested Components](https://www.freecodecamp.org/learn/front-end-libraries/react/use-react-to-render-nested-components)

> Note: We can pass methods component inside the class component inside the another component as an JSX self closing tag.

## [Compose React Components](https://www.freecodecamp.org/learn/front-end-libraries/react/compose-react-components)

## [React: Render a Class Component to the DOM](https://www.freecodecamp.org/learn/front-end-libraries/react/render-a-class-component-to-the-dom)

React components are passed into `ReactDOM.render()` a little differently than JSX elements. For JSX elements, you pass in the name of the element that you want to render. However, for React components, you need to use the same syntax as if you were rendering a nested component, for example `ReactDOM.render(<ComponentToRender />, targetNode)`. You use this syntax for both ES6 class components and functional components.

## [React: Write a React Component from Scratch](https://www.freecodecamp.org/learn/front-end-libraries/react/write-a-react-component-from-scratch)

```jsx
class NameOFClass extends React.Component {
    constructor(props) {
        super(props);
    }
    render() {
        return (
            // The JSX code you put here is what your component will render
        );
    }
}
```

## [React: Pass Props to a Stateless Functional Component](https://www.freecodecamp.org/learn/front-end-libraries/react/pass-props-to-a-stateless-functional-component)

```jsx
<App>
  <Welcome user="Mark" />
</App>
```

The welcome is the stateless functional component it has access to the value like so :

```jsx
const Welcome = (props) => <h1>Hello, {props.user}!</h1>;
```
