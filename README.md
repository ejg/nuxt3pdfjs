# Nuxt 3 - pdfjs express viewer problems

Nuxt 3.9.1
PDF JS 8.7.4

The only thing added to Nuxt is the pdf js files.

I used the files from:
https://pdfjs.express/documentation/get-started-viewer/vue
https://apryse.com/blog/webviewer/how-to-build-a-nuxt-pdf-viewer-with-nuxtjs

## Setup

npm install

## Dev

npm run dev

see the code in http://localhost:3000/

open Dev tools and everythings loads correctly

files are at
http://localhost:3000/lib/ui/style.css
http://localhost:3000/lib/core/webviewer-core.min.js
http://localhost:3000/lib/core/pdfjs/PDFJSDocumentType.js
http://localhost:3000/lib/core/pdfjs/UIConfig.js
http://localhost:3000/lib/ui/webviewer-ui.min.js

## Build

npx nuxi build

node .output/server/index.mjs

see the code in http://localhost:3000/

open Dev tools and everythings loads correctly

same file paths as above

## Build

npx nuxi generate

npx serve .output/public

see the code in http://localhost:3000/

open Dev tools

the files not found but linked from /lib/ui/index.html

http://localhost:3000/lib/style.css
http://localhost:3000/core/webviewer-core.min.js
http://localhost:3000/core/pdfjs/PDFJSDocumentType.js
http://localhost:3000/core/pdfjs/UIConfig.js
http://localhost:3000/lib/webviewer-ui.min.js

If I copy the

public/webviewer/core folder to
public/core and the
public/webviewer/ui files to
public/webviewer and run npx nuxi generate the pdf viewer works.

Note: if the WebViewer component is not wrapped in the import/then, the npm nuxi generate fails with a "window not defined message"
You can see that if, in App.vue, you comment out the WebViewer component and uncomment out WebViewerNoWindow
