<h1 align="center">JavaScript Refresher</h1>

### Overview of the Section
* **[Adding JavaScript To A Page & How React Projects Differ](#script-js)**
* **[React Projects Use a Build Process](#build)**

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


**[Back To The Top](#Overview-of-the-Section)**
#

