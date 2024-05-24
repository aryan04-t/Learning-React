# What is CSS?

> CSS (Cascading Style Sheets) is a styling language used to describe the style of HTML documents. It controls the layout, colors, fonts, and overall appearance of web pages.


### Who Built CSS?

CSS was developed by `Håkon Wium Lie` and `Bert Bos`, and it was first proposed by the World Wide Web Consortium (W3C) in 1996. 


### Why is CSS Used? 

CSS is used to separate content from design, making web pages more flexible and easier to maintain. It allows web developers to apply consistent styles across multiple pages and adapt the layout for different devices.  


<br> 


# What is TailWind CSS then: 


Tailwind CSS is a utility-first `CSS framework` that provides low-level, reusable style classes. It allows developers to build custom designs directly in their HTML by applying pre-defined utility classes.

### Key Features of Tailwind CSS

- **Utility-First**: Focuses on small, single-purpose classes that you can combine to create complex designs.
- **Customizable**: Highly configurable with a configuration file to adapt styles according to project needs.
- **Responsive**: Offers responsive design utilities to easily create mobile-friendly layouts.
- **Performance**: Encourages the use of minimal CSS, which can reduce file sizes and improve load times.

### Why Use Tailwind CSS?

Tailwind CSS simplifies the design process by eliminating the need for custom CSS. It speeds up development, ensures consistency, and allows for rapid prototyping without leaving the HTML file. 

### Official Documentation of Tailwind CSS: https://tailwindcss.com/docs 


<br> 


# Why Do we Need Daisy UI then? 

- Daisy UI is a `Component Library` which adds component class names to Tailwind CSS so you can make beautiful websites faster than ever.

- Daisy UI is a plugin for the Tailwind CSS framework that offers a collection of pre-designed components, including buttons, cards, forms, and navigation elements. It simplifies front-end development by providing ready-made components that can be easily customized and integrated into web projects.



### Key Features of Daisy UI:

- **Pre-designed Components**: Offers a variety of UI components that can be used out-of-the-box.
- **Customizable**: Allows developers to customize the appearance of components to fit their project's design.
- **Integration with Tailwind CSS**: Seamlessly integrates with Tailwind CSS, leveraging its utility-first approach for styling.
- **Time-saving**: Speeds up development by providing pre-built components, reducing the need for manual styling and layout, it also makes the inline written tailwind css look a lot less bulkier.

### Why Use Daisy UI?

Daisy UI simplifies the process of building user interfaces by offering a library of components that adhere to best design practices. It helps developers create consistent and visually appealing UIs while saving time and effort in front-end development.

### Official Documentation of Daisy UI: https://daisyui.com/ 


<br> 


# Let's see Difference between the bulkiness of code when we use "Tailwind CSS" and "Tailwind with Daisy UI Plugin" for designing a Button: 


### Defining a Blue Button with Tailwind CSS:

```jsx 
<button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
  Click me
</button>
```

### Using Daisy UI Plugin with Tailwind CSS for the Same Blue Button: 

```jsx 
<button class="btn btn-blue">
  Click me
</button>
```


<br> 


# What is PostCSS: 

- PostCSS is a JavaScript tool that transforms CSS code into an abstract syntax tree (AST). It can then use JavaScript plugins to analyze and modify the AST. 

- PostCSS can transpile future CSS syntax, which allows users to use modern and future CSS features today. 

- Despite its name, it is neither a post-processor nor a pre-processor, it is just a transpiler that turns a special PostCSS plugin syntax into a Vanilla CSS. You can think of it as the Babel tool for CSS. 



## Let's Understand What does "PostCSS can transpile future CSS syntax" Means: 


- We understood that PostCSS is a tool for transforming CSS with JavaScript plugins. 

- But when we say "PostCSS can transpile future CSS syntax," we mean that PostCSS can take CSS written using syntax or features that are proposed for future versions of CSS (but are not yet supported by current browsers) and convert it into CSS that is compatible with today's browsers. 


### Here's a breakdown of what this means:

  1. __Future CSS Syntax:__ This refers to features and syntax that are part of the CSS specifications but not yet widely supported by browsers. Examples include CSS custom properties, nested rules, and other experimental features.

  2. __Transpile:__ Transpiling means converting code from one language or syntax to another. In this case, it means converting future CSS syntax into a form of CSS that current browsers can understand.

  3. __PostCSS:__ PostCSS is a flexible tool that uses plugins to process CSS. These plugins can transform CSS in various ways, including transpiling future syntax.


## Example: 

### Let's say you want to use a future CSS feature like custom media queries, which might look like this: 

```css 
@custom-media --small-viewport (max-width: 30em);

.element {
  @media (--small-viewport) {
    color: blue;
  }
}
```

- This syntax is not yet supported by most browsers. However, with PostCSS and the right plugins (e.g., postcss-custom-media), you can write your CSS using this future syntax. PostCSS will then transpile it to something like this:

``` css 
@media (max-width: 30em) {
  .element {
    color: blue;
  }
}
```


## Benefits of using PostCSS: 

1. __Future-Proofing:__ You can write CSS using the latest features and syntax, ensuring your stylesheets are future-proof.
2. __Browser Compatibility:__ PostCSS will handle the conversion to ensure compatibility with current browsers.
3. __Modularity:__ By using plugins, you can tailor PostCSS to your specific needs and easily extend its functionality.


<br> 


# References Cited: 

* __freeCodeCamp__ (What is PostCSS? How to Use Plugins to Automate CSS Tasks)__:__ 
https://www.freecodecamp.org/news/what-is-postcss/ 

* __ChatGPT:__ https://chatgpt.com 