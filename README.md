# npm-spof-test

> npm's [single point of failure](https://resir014.github.io/2016/03/23/npms-single-point-of-failure/) - illustrated.

## Installation

```bash
$ npm install --save npm-spof-test
```

## Usage

Prints an arbitrary 'Hello, world!' message.

```js
var spof = require('npm-spof-test')

spof.print()
```

## Testing procedure

1. I'll publish this package into the npm registry.
2. I'll make a small app which depends on this package, and made a quick script which runs the print function.
3. I'll unpublish it, and make sure that the package is no longer downloadable after unpublishing.
4. Someone else will then fork the package, changes what prints out, and republishes it with the patch version incremented.
5. I'll try redownloading the package into the app and see if it affects the print function.

## License

[WTFPL.](https://github.com/resir014/npm-spof-test/blob/master/LICENSE)
