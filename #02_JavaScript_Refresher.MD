<h1 align="center">JavaScript Refresher</h1>

### Overview of the Section
* **[Adding JavaScript To A Page & How React Projects Differ](#script-js)**
* **[](#)**

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

![Js Script]()


**[Back To The Top](#Overview-of-the-Section)**
#

