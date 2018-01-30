# Modules

The [`import`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import) and [`export`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/export) statements have been standardized in [ES2015](https://babeljs.io/learn-es2015/). Although they are not supported in most browsers yet, webpack does support them out of the box.

Behind the scenes, webpack actually "transpiles" the code so that older browsers can also run it. If you inspect `dist/bundle.js`, you might be able to see how webpack does this, it's quite ingenious! Besides `import` and `export`, webpack supports various other module syntaxes as well, see [Module API](https://webpack.js.org/api/module-methods) for more information.

Note that webpack will not alter any code other than `import` and `export` statements. If you are using other [ES2015 features](http://es6-features.org/), make sure to [use a transpiler](https://webpack.js.org/loaders/#transpiling) such as [Babel](https://babeljs.io/) or [Bublé](https://buble.surge.sh/guide/) via webpack's [loader system](https://webpack.js.org/concepts/loaders/).

## How to use
This section is merely informative. Nothing to do here, just learn. Have fun!
