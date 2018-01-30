# Basic Setup

In this example, there are implicit dependencies between the `<script>` tags. Our `index.js` file depends on lodash being included in the page before it runs. This is because `index.js` never declared a need for lodash; it just assumes that the global variable `_` exists.

There are problems with managing JavaScript projects this way:

* It is not inmediately apparent that the script depends on a external library.
* If a dependency is missing, or included in the wrong order, the application will not function properly.
* If a dependency is included but not used, the browser will be forced to download unnecesary code.

Let's use webpack to manage these scripts instead.