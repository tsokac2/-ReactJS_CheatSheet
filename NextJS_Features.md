## [NEXT.js](https://nextjs.org/docs/getting-started) - Create Project

### System Requirements:
* [Node.js 14.6.0](https://nodejs.org/en/) or newer
* MacOS, Windows (including WSL), and Linux are supported

### Google Fonts Implementation - Custom Document

A custom Document can update the ```<html>``` and ```<body>``` tags used to render a Page.

This file is only rendered on the server, so event handlers like onClick cannot be used in _document.

To override the default Document, create the file ```pages/_document.js``` as shown below:

```
import { Html, Head, Main, NextScript } from 'next/document'

export default function Document() {
  return (
    <Html>
      <Head />
      <body>
        <Main />
        <NextScript />
      </body>
    </Html>
  )
}
```