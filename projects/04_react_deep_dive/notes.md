# React - Deep Dive notes

---

## Essential Concepts

- Components - Reusable building blocks which are used to build the overall app UI
- Props - Component "attributes" (input data) used to configure components
- JSX - JS Syntax extension to describe HTML in JavaScript
- State - React-managed data which, when changed, causes React to re-execute the related component function.

---

## The react build process

1) The react code you write and test
2) Build process
    - Changes and optimises your code
    - Transforms it such that it runs in the browser
    - Also potentially optimises other assets like CSS and image files
3) Deployable files
   A collection of generated files that include your optimised code and any other extra assets (e.g CSS code files, optimsied images etc)

---

## Don't need JSX but is more convenient

```html

<div id="content">
    <p>Hello world!<p>
</div>

```

^^^^ Requires build process and code transformation
-- Easy to read and understand


```javascript

React.createElement(
    'div', //Component type - identifies the to-be-rendered component
    { id : 'content'}, // Props object - sets component props
React.createElement(
    'p',
    null,
    'Hello World' // Child content - the content passed between the component tags
)
);

```

^^^ Works without special build process and transformation

---

## Additional Key Component and Props Concepts

- Forwarded props
- Multiple component slots
- Elements identifiers as Props
- Default prop values