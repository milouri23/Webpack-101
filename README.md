# NPM Scripts

Given it's not particularly fun to run a local copy of webpack from the CLI, we can set up a little shortcut. Let's adjust our package.json by adding an [npm script](https://docs.npmjs.com/misc/scripts).

## How to use
Now the `npm run build` command can be used in place of the `npx` command we used earlier. Note that within `scripts` we can reference locally installed npm packages by name the same way we did with `npx`. This convention is the standard in most npm-based projects because it allows all contributors to use the same set of common scripts (each with flags like `--config` if necessary).

Now run the following command and see if your script alias works:

```console
npm run build

Hash: 857f878815ce63ad5b4f
Version: webpack 3.9.1
Time: 294ms
    Asset    Size  Chunks                    Chunk Names
bundle.js  544 kB       0  [emitted]  [big]  main
   [0] ./src/index.js 222 bytes {0} [built]
   [2] (webpack)/buildin/global.js 509 bytes {0} [built]
   [3] (webpack)/buildin/module.js 517 bytes {0} [built]
    + 1 hidden module
```

> Custom parameters can be passed to webpack by adding two dashes between the npm run build command and your parameters, e.g. `npm run build -- --colors`.
