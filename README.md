# is-valid-path [![NPM version](https://badge.fury.io/js/is-valid-path.svg)](http://badge.fury.io/js/is-valid-path)

> Returns true if a file path does not contain any invalid characters.

Install with [npm](https://www.npmjs.com/)

```bash
npm i is-valid-path --save
```

## Usage

```js
var isValid = require('is-valid-path');

/**
 * Valid
 */

isValid('abc.js');
//=> 'true'
isValid('abc/def/ghi.js');
//=> 'true'
isValid('foo.js');
//=> 'true'

/**
 * Invalid
 */

isValid();
//=> 'false'
isValid(null);
//=> 'false'
isValid('!foo.js');
//=> 'false'
isValid('*.js');
//=> 'false'
isValid('**/abc.js');
//=> 'false'
isValid('abc/*.js');
//=> 'false'
isValid('abc/(aaa|bbb).js');
//=> 'false'
isValid('abc/[a-z].js');
//=> 'false'
isValid('abc/{a,b}.js');
//=> 'false'
isValid('abc/?.js');
//=> 'false'
```

## Related

* [is-glob](https://github.com/jonschlinkert/is-glob): Returns `true` if the given string looks like a glob pattern.
* [is-invalid-path](https://github.com/jonschlinkert/is-invalid-path): Returns true if a file path has invalid characters.
* [is-git-url](https://github.com/jonschlinkert/is-git-url): Regex to validate that a URL is a git url.
* [micromatch](https://github.com/jonschlinkert/micromatch): Glob matching for javascript/node.js. A drop-in replacement and faster alternative to minimatch and multimatch. Just… [more](https://github.com/jonschlinkert/micromatch)
* [parse-glob](https://github.com/jonschlinkert/parse-glob): Parse a glob pattern into an object of tokens.

## Run tests

Install dev dependencies:

```bash
npm i -d && npm test
```

## Contributing

Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](https://github.com/jonschlinkert/is-valid-path/issues)

## Author

**Jon Schlinkert**

+ [github/jonschlinkert](https://github.com/jonschlinkert)
+ [twitter/jonschlinkert](http://twitter.com/jonschlinkert)

## License

Copyright (c) 2015 Jon Schlinkert
Released under the MIT license.

***

_This file was generated by [verb-cli](https://github.com/assemble/verb-cli) on May 06, 2015._
