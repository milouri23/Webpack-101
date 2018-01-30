# Creating a bundle

In this setup, `index.js` explicitly requires `lodash` to be present, and bind it as `_` (no global scope pollution). By stating what dependencies a module needs, webpack can use this information to build a dependency graph. It then uses the graph to generate an optimized bundle where scripts will be executed in the correct order.

## How to use
With that said, let's run `npx webpack` with our script as the [entry point](https://webpack.js.org/concepts/entry-points/) and `bundle.js` as the [output](https://webpack.js.org/concepts/output). The `npx` command, which ships with Node 8.2 or higher, runs the webpack binary (`./node_modules/.bin/webpack`) of the webpack package we installed in the beginning.

```console
npx webpack src/index.js dist/bundle.js

Hash: 857f878815ce63ad5b4f
Version: webpack 3.9.1
Time: 332ms
    Asset    Size  Chunks                    Chunk Names
bundle.js  544 kB       0  [emitted]  [big]  main
   [0] ./src/index.js 222 bytes {0} [built]
   [2] (webpack)/buildin/global.js 509 bytes {0} [built]
   [3] (webpack)/buildin/module.js 517 bytes {0} [built]
    + 1 hidden module
```

Open `index.html` in your browser and, if everything went right, you should see the following: 'Hello webpack'.
