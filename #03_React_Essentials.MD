<h1 align="center">React Essentials - Components, JSX, Props, State...</h1>

### Overview of the Section
* **[About Components!](#components)**
* **[JSX & React Components](#jsx-com)**


#
### <a name="components">About Components!</a>

In React, components are the building blocks of user interfaces. They are reusable pieces of code that can be combined to create complex UIs.

Here are the key points about components:

- Components are created by developers.
- They can wrap HTML, CSS, and JavaScript code.
- They allow you to split complex UIs into smaller, more manageable parts.
- Components can be reused in different places of the UI.
- Related code can be stored together within components.
- Components promote separation of concerns, where different components handle different parts of the UI.

**Note**: This concept of components is also used in other popular front-end frameworks and even in mobile development frameworks.

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="jsx-com">JSX & React Components</a>

The important code snippet is related to creating a React Component:

```js
function MyComponent() {
  // JSX code describing the UI for this component
  return (
    <div>
      {/* Your HTML here */}
    </div>
  );
}
```
**Key points**:
- **JSX extension**: Files using JSX syntax have the ``.jsx`` extension (e.g., ``index.jsx``, ``App.jsx``).
- **Component as a Function**: A React component is a JavaScript function starting with an uppercase letter (e.g., ``MyComponent``).
- **Returning JSX**: The component function must return JSX code that describes the UI elements for that component.

**[Back To The Top](#Overview-of-the-Section)**
#


**[Back To The Top](#Overview-of-the-Section)**
#