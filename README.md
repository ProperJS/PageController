ProperJS // PageController
==========================

> Lightweight, event driven JS router with History.



### Installation

```shell
npm i properjs-pagecontroller --save-dev
```



### Usage
```javascript
import PageController from "properjs-pagecontroller";

const pageController = new PageController({
    transitionTime: 0, // Default
    routerOptions: { // Default
        historyOptions: {},
    },
    routes: ["*"], // Default
});

pageController.on( "samepage", ( data ) => {
    console.log( "samepage", data );
});

pageController.on( "document", ( data ) => {
    console.log( "document", data );
});

pageController.on( "transition-out", ( data ) => {
    console.log( "transition-out", data );
});

pageController.on( "transition-in", ( data ) => {
    console.log( "transition-in", data );
});

pageController.on( "initialized", ( data ) => {
    console.log( "initialized", data );
});

pageController.bind(); // Your webapp is now bound and using ProperJS/Router

setTimeout(() => {
    pageController.routeSilently( "http://localhost:9999/another/route" );

}, 2000 );
```
