# ES6 Module Import and Export: 


<br>


## Exporting: 


### Named Exports: 
- Named exports allow you to export multiple values. You can export variables, functions, or classes using the `export` keyword.

```js
// file: math.mjs

export const pi = 3.14159;

export function square(x) {
  return x * x;
}

export class Circle {
  constructor(radius) {
    this.radius = radius;
  }
}

// Here above done all exports are shipped in an object 
// That's why using the same names of these exports you can also destructure all these exports from the object while importing them 
```


```js
// file: math.mjs 

// Same above code can also be written like this, it is the same thing 

const pi = 3.14159; 

function square(x) {
  return x * x;
}

class Circle {
  constructor(radius) {
    this.radius = radius;
  }
}

export {pi, square, Circle}; 
```


### Default Exports: 
- Default exports are used to export a single value or to have a fallback export for a module.
- A module can only have one `export default` statement, either export one function, variable, class or an object, it doesn't matter, but you can write export default statement only once in a module. 

```js
// file: person.mjs

export default class Person {
  constructor(name) {
    this.name = name;
  }
}

// Above is example of exporting while declaring and defining something 

/*

// Instead of writing above piece of code, you can also export default like this after you declared and defined that thing  

export default Person; 

*/
```



<br>



## Importing: 


### Named Imports: 
- Named imports allow you to import specific variables, functions, or classes from a module.

```js
// file: main.mjs

import { pi, square, Circle } from './math.mjs';         // Here we're importing all the exports in individual variables using the object destructuring property of JS 

console.log(pi); // 3.14159
console.log(square(4)); // 16

const circle = new Circle(5);

console.log(circle.radius); // 5
```


### Importing with Aliases
- You can rename imports using the `as` keyword.

```js
// file: main.mjs
import { pi as PI, square as sq, Circle as Circ } from './math.mjs';

console.log(PI); // 3.14159
console.log(sq(4)); // 16

const circ = new Circ(5);
console.log(circ.radius); // 5
```


### Default Imports: 
- Default imports are used to import the default export from a module.

```js
// file: main.mjs

import Person from './person.mjs';

const person = new Person('John Doe');

console.log(person.name); // John Doe
```


### Importing All Exports: 
- You can import all exports from a module as an object.

```js
// file: main.mjs

import * as math from './math.mjs';

console.log(math.pi); // 3.14159
console.log(math.square(4)); // 16

const circle = new math.Circle(5);

console.log(circle.radius); // 5

// But above you can notice that math.mjs don't have a 'export default', but if it had an export default, then in this case when we're importing from a module as an object, then even the default export would be present in the object, and you can access it by typing 'math.default' here in this main.mjs file 
```


<br>



## Exporting and Importing with "as" Keyword: 

- The `as` keyword is used to rename exports or imports. This is useful to avoid naming conflicts or to give more meaningful names.


### Exporting with Aliases: 

```js
// file: constants.mjs

const pi = 3.14159;
const e = 2.71828;

export { pi as PI, e as E };
```


### Importing with Aliases: 

```js
// file: main.mjs

import { PI, E } from './constants.mjs';

console.log(PI); // 3.14159
console.log(E); // 2.71828
```