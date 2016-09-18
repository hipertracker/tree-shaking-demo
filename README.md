# Demo: tree-shaking

This project demonstrates how to do tree-shaking (removal of unused exports) with webpack 2 and Babel 6.

Installation:

```
cd tree-shaking-demo/
npm install
```

There are two ways in which you can build and run the web app:

* Build once:
    * `npm run build`
    * Open `build/index.html`
* Watch files continuously, rebuild incrementally, whenever one of them changes:
    * `npm run watch`
    * Open `build/index.html`, manually reload page in browser whenever there was a change

## Webpack2 tree shaking 

There is something wrong with

```
  presets: ['es2015', {modules: false}],
```  


```
npm run build

> @ build /Users/hipertracker/Development/github/hipertracker/tree-shaking-demo
> webpack --optimize-minimize

Hash: 3aea6d8a27453c0be041
Version: webpack 2.0.7-beta
Time: 538ms
   + 1 hidden modules

ERROR in ./js/main.js
Module build failed: ReferenceError: [BABEL] /Users/hipertracker/Development/github/hipertracker/tree-shaking-demo/js/main.js: Using removed Babel 5 option: foreign.modules - Use the corresponding module transform plugin in the `plugins` option. Check out http://babeljs.io/docs/plugins/#modules
   at Logger.error (/Users/hipertracker/Development/github/hipertracker/tree-shaking-demo/node_modules/babel-core/lib/transformation/file/logger.js:41:11)
   at OptionManager.mergeOptions (/Users/hipertracker/Development/github/hipertracker/tree-shaking-demo/node_modules/babel-core/lib/transformation/file/options/option-manager.js:214:20)
   at /Users/hipertracker/Development/github/hipertracker/tree-shaking-demo/node_modules/babel-core/lib/transformation/file/options/option-manager.js:255:14
   at /Users/hipertracker/Development/github/hipertracker/tree-shaking-demo/node_modules/babel-core/lib/transformation/file/options/option-manager.js:299:20
   at Array.map (native)
   at OptionManager.resolvePresets (/Users/hipertracker/Development/github/hipertracker/tree-shaking-demo/node_modules/babel-core/lib/transformation/file/options/option-manager.js:265:20)
   at OptionManager.mergePresets (/Users/hipertracker/Development/github/hipertracker/tree-shaking-demo/node_modules/babel-core/lib/transformation/file/options/option-manager.js:254:10)
   at OptionManager.mergeOptions (/Users/hipertracker/Development/github/hipertracker/tree-shaking-demo/node_modules/babel-core/lib/transformation/file/options/option-manager.js:239:14)
   at OptionManager.init (/Users/hipertracker/Development/github/hipertracker/tree-shaking-demo/node_modules/babel-core/lib/transformation/file/options/option-manager.js:338:12)
   at File.initOptions (/Users/hipertracker/Development/github/hipertracker/tree-shaking-demo/node_modules/babel-core/lib/transformation/file/index.js:216:65)
   at new File (/Users/hipertracker/Development/github/hipertracker/tree-shaking-demo/node_modules/babel-core/lib/transformation/file/index.js:137:24)
   at Pipeline.transform (/Users/hipertracker/Development/github/hipertracker/tree-shaking-demo/node_modules/babel-core/lib/transformation/pipeline.js:46:16)
   at transpile (/Users/hipertracker/Development/github/hipertracker/tree-shaking-demo/node_modules/babel-loader/index.js:38:20)
   at Object.module.exports (/Users/hipertracker/Development/github/hipertracker/tree-shaking-demo/node_modules/babel-loader/index.js:131:12)
```   
