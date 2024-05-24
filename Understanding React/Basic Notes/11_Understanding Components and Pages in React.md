# Components in React

> In React, components are the building blocks of user interfaces. They encapsulate reusable pieces of code, each responsible for rendering a part of the UI. Components can be composed together to create complex UIs, making them modular, maintainable, and easy to understand. 


## Types of Components in React: 

> Components can be categorized into a lot of types based on how they function, but these are the major types of components based on their nature: 

### 1. Functional Components

- Also known as stateless components or presentational components.
- Defined as JavaScript functions that accept props as arguments and return JSX elements.
- Used for simpler UI elements that do not manage state or lifecycle methods.
- Preferred for their simplicity and performance optimizations.

### 2. Class Components

- Also known as stateful components or container components.
- Defined as ES6 classes that extend the React.Component class.
- Used for more complex UI elements that require state management or lifecycle methods.
- Maintain their own state and can access lifecycle methods like componentDidMount, componentDidUpdate, etc.

### 3. Pure Components

- A type of class component optimized for performance.
- Automatically perform a shallow comparison of props and state to determine if the component needs to re-render.
- Re-renders only when changes occur in props or state, improving performance by avoiding unnecessary renders.

### 4. Higher-Order Components (HOC)

- A pattern in React where a function takes a component as an argument and returns a new component.
- Used for code reuse, logic abstraction, and adding additional functionality to components.
- Commonly used for implementing features like authentication, routing, and data fetching.



# Pages in React

In React applications, pages represent different views or routes of the application. Each page typically corresponds to a specific URL route and contains one or more components that make up the UI for that route.

- `Pages represent routes`: Each page in a React application corresponds to a specific route or URL. For example, `/home`, `/about`, `/contact`, etc.
- `Pages organize components`: Pages serve as containers for organizing and composing components that make up the UI for a specific route.
- `Pages may have additional logic`: Pages may contain additional logic related to routing, data fetching, or state management specific to that route.
- `Pages are typically top-level components`: Pages are often rendered at the top level of the application's component hierarchy and are responsible for rendering the layout and structure of the entire page 