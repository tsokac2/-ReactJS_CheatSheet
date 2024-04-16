<h1 align="center">JavaScript Refresher</h1>

### Overview of the Section
* **[Adding JavaScript To A Page & How React Projects Differ](#script-js)**
* **[React Projects Use a Build Process](#build)**
* **["import" & "export"](#i-e)**
* **[Revisiting Variables & Values](#values-v)**
* **[Operators](#o)**
* **[Functions & Parameters](#f-p)**
* **[Arrow Functions](#arrow-functions)**
* **[Objects & Classes](#o-c)**
* **[Arrays & Array Methods like map()](#array-methods)**

#
### <a name="script-js">Adding JavaScript To A Page & How React Projects Differ</a>
**There are two main ways to add JavaScript code to a website**:- **
- **Inline**: Wrap your code between <script> tags in the HTML. (Not recommended for large codebases)
- **External Files**: Create separate JavaScript files (e.g. ``.js`` extension) and import them using ``<script>`` tags with a src attribute pointing to the file location.

**Importing JavaScript Files**:
- ``<script``> tag with src attribute: ``<script src="./assets/scripts/app.js"></script>``
- Script can be placed anywhere in the ``<head>`` or ``<body>`` section of the HTML.
- Optional ``defer`` attribute: Ensures the script executes **_after_** the HTML is parsed (recommended if your script relies on HTML elements).
- Modern approach: Use ``type="module"`` attribute on the ``<script>`` tag. This enables importing code between JavaScript files using the import syntax.

**Note:** When building React applications, a build process typically injects these script tags into the HTML automatically.

![Js Script](https://github.com/tsokac2/-_-_ReactJS_CheatSheet/blob/main/src/01.JPG)

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="build">React Projects Use a Build Process</a>
- React projects use a build process to transform code before it's delivered to the browser.
- Look for the ``package.json`` file to see the libraries used in a project, including React Scripts.
- Build process is typically run in the background by a development server.
- There are two main reasons for using a build process:
    - Transform JSX code (special syntax combining HTML and JavaScript) into regular JavaScript that browsers understand.
    - Minify code (optimize and shorten) for production to reduce file size.
- Tools like Create React App or Vite come with a built-in build process.
- NodeJS is required to run the build process tools.
- Command: ``npm`` (Node Package Manager) - used to install dependencies.
- Command: ``npx`` (included with npm) - used to create projects.

![Build Process by React](https://github.com/tsokac2/-_-_ReactJS_CheatSheet/blob/main/src/02.JPG)

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="i-e">"import" & "export"</a>
#### Exporting:
- Use the export keyword before a variable or function to make it available for import in other files.
- You can export multiple named exports using curly braces ``{}``.
**Example**:
```js
export const apiKey = "your_api_key_here";
```
- To create a default export, use the ``export default`` keyword before the value. You can only have one default export per file.

**Example**:
```js 
export default function sayHi(name) {
  console.log("Hi, " + name);
}
```
#### Importing:
- Use the ``import`` keyword to import something from another file.
- For named exports, specify the names of the things you want to import inside curly braces ``{}`` after the ``from`` keyword.

**Example**:
```js
import { apiKey } from "./util.js";
```
- To import the default export, you don't need curly braces. Assign any name you want to the imported value after the ``from`` keyword.

**Example**:
```js
import someName from "./util.js"; // someName can be any name
```
- You can import all named exports from a file using ``import * as namespace`` syntax.

**Example**:
```js
import * as utils from "./util.js";
console.log(utils.apiKey); // Accessing apiKey from util.js
```
- You can group multiple named exports and the default export into an object using import * as namespace syntax.
**Example**:
```js
import * as utils from "./util.js";
console.log(utils.apiKey); // Accessing apiKey
console.log(utils.default); // Accessing default export
```

- Use the ``as`` keyword to assign an alias to an imported variable or function.
- **Example**:
```js
import { abc as content } from "./util.js";
console.log(content); // This will log the value of abc from util.js
```

In React projects, you might not see the type="module" attribute explicitly mentioned because the build process handles imports and exports differently.

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="values-v">Revisiting Variables & Values</a>
#### Commands:
-  ``let``: This keyword is used to create a variable in JavaScript.
-  ``const``: This keyword is used to create a constant in JavaScript.
-  ``console.log``: This is a built-in function in JavaScript that is used to output a value to the console.

#### Important concepts:
- **Variables**: Variables are used to store data. You can give them a name and use that name to refer to the data throughout your code.
- **Values**: Values are the actual data that is stored in variables. In JavaScript, there are different types of values, including strings, numbers, booleans, and null/undefined.
- **Constants**: Constants are similar to variables, but the value cannot be changed after it is assigned.
- **Camel Case Notation**: This is a naming convention for variables where the first word starts with a lowercase letter and subsequent words start with uppercase letters (e.g., userName).
- **Code Readability**: Using variables can improve the readability of your code by making it easier to understand what the code is doing.

![Revisiting Variables & Values](https://github.com/tsokac2/-_-_ReactJS_CheatSheet/blob/main/src/03.JPG)

```js
let userMessage = "Hello World";
console.log(userMessage); // This will output "Hello World" to the console.
```

**Additional Notes**:
- Variable names can contain numbers, but not at the beginning.
- Variable names cannot contain special characters (except for ``$`` and ``_``).
- There are different philosophies about using ``let`` vs. ``const``. The author recommends using ``const`` as often as possible to be clear about your intentions.

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="o">Operators</a>

#### Variables:
- ``const`` and ``let`` are important for declaring variables.
#### Operators:
- Math operators: ``+``, ``-``, ``*``, ``/``(division)
- String concatenation: ``+`` (combines text)
- Comparison operators: ``===`` (equal to), ``!==`` (not equal to), ``>`` (greater than), ``<`` (less than), ``>=`` (greater than or equal to), ``<=`` (less than or equal to)

#### Conditional statements:
- ``if`` statement: executes code only if a certain condition is true. (We'll learn more about this later)

#### Important code to remember:
- ``const`` or ``let`` followed by a variable name and an equal sign (used to assign a value to the variable).
- Math operators used with numbers (e.g., ``10 / 5``).
- ``+`` used to concatenate strings (e.g., ``"hello" + "world"``).
- Comparison operators used with values (e.g., ``10 === 10``).
- ``if`` statement followed by a condition in parentheses and curly braces containing the code to execute if the condition is true (e.g., ``if (10 === 10) { ... }``).

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="f-p">Functions & Parameters</a>

#### Defining a function:
- Use the ``function`` keyword followed by a name (follows variable naming rules).
- Define parameters (optional) in parenthesis after the name, separated by commas.
- Enclose the function body (the code to be executed) in curly braces ``{}``.

#### Calling a function:
- Use the function name followed by parenthesis ``()``.
- Provide values for the parameters (in the same order they are defined) inside the parenthesis when calling the function.

#### Important concepts:
- Functions are reusable blocks of code.
- Parameters allow functions to accept input values.
- The ``return`` keyword allows functions to return a value.
- Functions can be named descriptively to improve readability.

#### Code Examples:
Defining a function with a parameter and console logging it:

```js
function greet(username) {
  console.log(username);
}
```

Calling the function with a value for the parameter:
```js
greet("Tomislav");
```
Defining a function with multiple parameters and a return statement:
```js
function createGreeting(username, message) {
  return "Hi, I am " + username + ". " + message;
}
```
Calling the function and storing the returned value in a variable:
```js
const greeting = createGreeting("Tomislav", "Hello!");
console.log(greeting);
```
**[Back To The Top](#Overview-of-the-Section)**
#

### Arrow Functions

When working with Arrow Functions, you have a couple of "syntax shortcuts" available.

**Most importantly, you should know about the following alternatives**:

1. **Omitting parameter list parentheses**
If your arrow functions takes **exactly one parameter**, you may **omit** the wrapping parentheses.

Instead of

```js
(userName) => { ... }
```
you could write

```js
userName => { ... }
```
**Please note**: 
- If your function takes **no parameters**, parentheses **must not be omitted** - ``() => { ... }`` is the **only correct form** in that case.
- If your function takes **more than one parameter**, you also **must not omit** parentheses - ``userName, userAge => { ... }`` would be invalid (``((userName, userAge) => { ... }`` is correct)!

2. **Omitting function body curly braces**
If your arrow function contains **no other logic** but a ``return`` statement, you may **omit the curly** braces and the ``return`` keyword.

Instead of

```js
number => { 
  return number * 3;
}
```
you could write
```js
number => number * 3;
```

**The following code would be invalid**:
```js
number => return number * 3; // invalid because return keyword must also be omitted!
number => if (number === 2) { return 5 }; // invalid because if statements can't be returned
```

3. **Special case: Just returning an object**

If you go for the shorter alternative explained in **2.** and you're trying to return a **JavaScript object**, you may end up with the following, **invalid** code:

```js
number => { age: number }; // trying to return an object
```
This code would be invalid because JavaScript treats the curly braces as **function body wrappers** (not as code that creates a JS object)
To _"tell"_ JavaScript that an object should be created (and returned) instead, the code would need to be adjusted like this:

```js
number => ({ age: number }); // wrapping the object in extra parentheses
```
By wrapping the object and its curly braces with an **extra pair of parentheses**, 
JavaScript understands that the curly braces are not there to define a function body but instead to create an object. Hence that object then gets returned.

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="o-c">Objects & Classes</a>

**Creating Objects**:

- Use curly braces {} to create an object.
- Inside the curly braces, define key-value pairs separated by colons :.
  - Keys are property names (strings).
  - Values can be any data type including other objects and functions.
- Access object properties using dot notation object.propertyName.

**Example**:
```
const user = {
  name: "Max",
  age: 34
}
console.log(user.name); // Output: "Max"
```

**Object Methods**:
  - Objects can store functions as properties, called methods.
  - Access methods using dot notation and call them with parentheses ``object.methodName()``.

**Example**:
```
const user = {
  name: "Max",
  age: 34,
  greet() {
    console.log("Hello!");
  }
}
user.greet(); // Output: "Hello!"
```
- The ```this`` Keyword:
- Inside an object method, ``this`` refers to the current object.
- Use ``this`` to access other properties and methods of the object.

**Example**:
```
const user = {
  name: "Max",
  age: 34,
  greet() {
    console.log("Hello, my name is", this.name);
  }
}
user.greet(); // Output: "Hello, my name is Max"
```
**Classes (briefly mentioned)**:
- A blueprint for creating objects.
- Use the class keyword to define a class.
- A class can have methods and a constructor function.
- Use the new keyword to create objects (instances) from a class.

**Code to Remember**:
- Creating objects with curly braces: ``{ key1: value1, key2: value2 }``
- Accessing object properties: ``object.propertyName``
- Calling object methods: ``object.methodName()``
- Using ``this`` inside object methods: ``this.propertyName`` or ``this.methodName()``

**[Back To The Top](#Overview-of-the-Section)**
#
### <a name="array-methods">Arrays & Array Methods like map()</a>

**Arrays**:

- Created using square brackets [].
- Store ordered lists of values.
- Accessed by index starting at 0 (first item).

**Important Array Methods**:

- ``.push(item)`` - Adds a new item to the end of the array.
- ``.findIndex(callbackFunction)`` - Finds the index of the first item where the callback function returns true.
  - The callback function takes an item as input and should return true if the item matches the search criteria.
  - Shorter Arrow Function version for findIndex:

```js
(item) => item === 'searched_value'
```

- ``.map(callbackFunction)`` - Creates a new array with the results of calling the callback function on every item in the original array.
  - The callback function takes an item as input and should return the transformed item.
  - Shorter Arrow Function version for map:

```js
(item) => item + '!' // Example: adding exclamation mark
```
**Important Notes**:
- Both ``.findIndex`` and ``.map`` create new arrays and do not modify the original array.
- ``.map`` allows you to transform items into any kind of value (strings, objects, etc.).

**[Back To The Top](#Overview-of-the-Section)**
#