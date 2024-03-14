<h1 align="center">JavaScript Refresher</h1>

### Overview of the Section
* **[Adding JavaScript To A Page & How React Projects Differ](#script-js)**
* **[React Projects Use a Build Process](#build)**
* **["import" & "export"](#i-e)**
* **[Revisiting Variables & Values](#values-v)**
* **[Operators](#o)**

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


**[Back To The Top](#Overview-of-the-Section)**
#

