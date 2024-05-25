# Understanding JSX and JavaScript Expressions in Depth: 


<br>


## JSX Return Statements: 

In JSX, we use curly braces `{}` to embed JavaScript expressions within the markup. This differentiation allows JSX to mix HTML-like syntax with JavaScript code seamlessly.

**Example:**

```js 
function Greeting() {
  const name = "Alice";
  return (
    <div>
      <h1>Hello, {name}!</h1>
    </div>
  );
}
```

In the above example, `{name}` is a JavaScript expression that gets evaluated and embedded within the HTML-like JSX.


<br>


## Writing CSS in JSX: 

When writing CSS in JSX, there are two primary approaches: inline styles and styled-components. Here, we'll focus on inline styles.

### Inline CSS Properties: 

Inline CSS properties in JSX are written in camelCase and enclosed within a JavaScript object, using curly braces `{}` to differentiate the JS expression from plain text.

**Example:**

```js
function StyledDiv() {
  return (
    <div style={{ backgroundColor: 'lightblue', color: 'darkblue' }}>
      This is a styled div.
    </div>
  );
}
```

In this example, `{ backgroundColor: 'lightblue', color: 'darkblue' }` is a JavaScript object defining the inline styles for the `div`.


<br> 


## CamelCase vs. Kebab-Case: 

Another key difference is that CSS properties in the JavaScript object are written in camelCase instead of kebab-case. This is because JavaScript doesn't allow hyphens in variable names, so we have to use camelCase instead.

**Example:**

- CSS (kebab-case): `background-color`
- JSX (camelCase): `backgroundColor`

**Example Usage:**

```js
function StyledParagraph() {
  return (
    <p style={{ fontSize: '16px', textAlign: 'center' }}>
      This is a styled paragraph.
    </p>
  );
}
```

In the example above, `fontSize` and `textAlign` are written in camelCase as per JavaScript conventions. 


<br> 


## In-depth Explanation of Why Inline CSS Requires Two Curly Braces: 


In JSX, when you're adding inline styles, you enclose the styles within double curly braces `{{}}` for a specific reason.

1. **Outer Curly Braces**: The outer pair of curly braces indicates that you're embedding a JavaScript expression within JSX. This is necessary because you're providing a JavaScript object that contains the CSS styles.

2. **Inner Curly Braces**: The inner pair of curly braces is used to define an object literal in JavaScript. This means you're creating a JavaScript object to hold the CSS properties and their values.

So, the outer curly braces signify JSX interpreting a JavaScript expression, while the inner curly braces create a JavaScript object literal for defining CSS styles. This structure allows you to seamlessly integrate JavaScript and CSS within JSX syntax. 



## You can write above written CSS like this also, it means the same thing: 

```js 
function StyledParagraph() {
  
  const paragraphCSSObj1 = { 
    fontSize: '16px', 
    textAlign: 'center' 
  };

  return (
    <p style={paragraphCSSObj1}>
      This is a styled paragraph.
    </p>
  );
}
```


<br>


## Even HTML Attributes are Written in camelCase in JSX: 

- In JSX, HTML attributes such as `onclick`, `onchange`, `onmouseover`, etc., are written in camelCase, just like JavaScript event handler names. This is because JSX is closer to JavaScript syntax rather than HTML. 

Here's an example to illustrate this: 

```jsx
function MyComponent() {
  
  const handleClick = () => {
    console.log('Button clicked!');
  };

  return (
    <button onClick={handleClick}>Click Me</button>
  );
}
```

### In the above code:

- The `onClick` attribute in JSX corresponds to the `onclick` attribute in HTML.
- `handleClick` is a JavaScript function that gets executed when the button is clicked.
- The event handler `handleClick` is passed as a prop to the `<button>` element using camelCase syntax.
