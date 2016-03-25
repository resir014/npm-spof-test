# npm-spof-test

> npm's single point of failure - illustrated.

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

1. I publish this package into the npm registry under version 0.0.3.
2. I make a small app which depends on this package, and made a quick script which runs the print function.
3. I unpublish it, and make sure that the package is no longer downloadable after unpublishing.
4. Someone else forks the package, changes what prints out, and republishes it under version 0.0.4.
5. I'll try redownloading the package into the app and see if it affects.

## License

WTFPL.
