# Refs and portals notes

---

## React Fragments

- Important rule - When writing JSX code, a JSX value must have only one root component

```javascript

    return (
      <h2>Welcome!</h2>
      <p>React is awesome!</p>
    );

    const content = (
      <h2>Welcome!</h2>
      <p>React is awesome!</p>
    );

    // ^^^ Both snippets have two sibling root elements and this is not allowed
    
```

### Solution

- Wrap `<div>` tags - this leads to extra 'div' in the DOM
- In react
  - Use `<Fragment>`
  - Can also use '<>'

```javascript

// Using Divs
    return (
      <div>
        <h2>Welcome!</h2>
        <p>React is awesome!</p>
      </div>
    );

    import { Fragment } from 'react';
     
//Using Fragements
    return (
      <Fragment>
        <h2>Welcome!</h2>
        <p>React is awesome!</p>
      </Fragment>
    );
    
// using <>
     
    return (
      <>
        <h2>Welcome!</h2>
        <p>React is awesome!</p>
      </>
    );

```

---

## State vs Refs

- State
  - Causes component re-evaluation (re-execution) when changed
  - Should be used for values that are directly reflected in the UI
  - Should not be used for "behind the scenes" values that have no direct UI impact
- Refs
  - Do not cause component re-evaluation when changed
  - Can be used to gain direct DOM element access (good for reading values or accessing certain browser APIs)