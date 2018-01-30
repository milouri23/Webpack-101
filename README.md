# Using a Configuration

Most projects will need a more complex setup, which is why webpack supports a [configuration file](https://webpack.js.org/concepts/configuration). This is much more efficient than having to type in a lot of commands in the terminal, so let's create one to replace the CLI options used above:

## How to use
Now, let's run the build again but instead using our new configuration:

```console
npx webpack --config webpack.config.js

Hash: 857f878815ce63ad5b4f
Version: webpack 3.9.1
Time: 298ms
    Asset    Size  Chunks                    Chunk Names
bundle.js  544 kB       0  [emitted]  [big]  main
   [0] ./src/index.js 222 bytes {0} [built]
   [2] (webpack)/buildin/global.js 509 bytes {0} [built]
   [3] (webpack)/buildin/module.js 517 bytes {0} [built]
    + 1 hidden module
```

> Note that when calling `webpack` via its path on windows, you must use backslashes instead, e.g. `node_modules\.bin\webpack --config webpack.config.js`.

A configuration file allows far more flexibility than simple CLI usage. We can specify loader rules, plugins, resolve options and many other enhancements this way. See the [configuration documentation](https://webpack.js.org/configuration) to learn more.
