# Reproduction repo for deepmerge bug /w webpack

For context, see [KyleAMathews/deepmerge/issues/97](https://github.com/KyleAMathews/deepmerge/issues/97) and [KyleAMathews/deepmerge/issues/87](https://github.com/KyleAMathews/deepmerge/issues/87).

## To reproduce

```sh
npm install
npm test
```

## Further detail

If you change the first line of `index.js` to

```js
import merge from "deepmerge"
```

then Webpack correctly returns the function.

If you do a CommonJS import:

```js
const merge = require("deepmerge")
```

then Webpack returns the `exports` property on whatever was exported by deepmerge, which is `undefined`.
