<h1 align="center">React: Getting Started</h1>


#

![]()

## [Create Project React Docs](https://reactjs.org/)


## [React](https://reactjs.org/) - Create Project

### System Requirements:
* [Node.js 14.6.0](https://nodejs.org/en/) or newer
* MacOS, Windows (including WSL), and Linux are supported

### Setup
* In the command line check the Node version:

    ```node --version```
* You’ll need to have Node 14.0.0 or later version on your local development machine.
* If Node is not installed download the installer from **[HERE](https://nodejs.org/en/)**
* To create a new app, you may choose one of the following methods:

The following command will create a new folder with the "Your app name"
### npx
```npx create-react-app my-app```
### npm
```npm init react-app my-app```
#### npm start - Run the app in development mode with 
``npm start``

```
    Compiled successfully!
    You can now view my-app in the browser.
    Local:            http://localhost:3000
    On Your Network:  http://192.168.0.228:3000
    Note that the development build is not optimized.
    To create a production build, use npm run build.

    webpack compiled successfully
```
* Open http://localhost:3000 to view it in the browser.
#
## [NEXT.js](https://nextjs.org/docs/getting-started) - Create Project

### System Requirements:
* [Node.js 14.6.0](https://nodejs.org/en/) or newer
* MacOS, Windows (including WSL), and Linux are supported

### Setup

* Creating a new Next.js app using create-next-app, which sets up everything automatically for you.

```npx create-next-app@latest .```
* If you want to start with a TypeScript project you can use the ```--typescript flag```

```npx create-next-app@latest --typescript .```
* After the installation is complete run

* NOTE: ``` . ``` a the end of the command avoids creating an app sub-folder.

```npm run dev``` 
* Development server will start on http://localhost:3000
* Edit pages/index.js and see the updated result in your browser

# Additional React npm packages
#### [React Icons](https://react-icons.github.io/react-icons)
``npm install react-icons --save``

#### [Lodash](https://lodash.com/)
``npm i --save lodash``

#### [Redux ](https://redux.js.org/introduction/getting-started)
``npm install @reduxjs/toolkit``

#### [Formik](https://formik.org/)
``npm install formik --save``