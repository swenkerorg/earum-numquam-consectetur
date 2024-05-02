# @swenkerorg/earum-numquam-consectetur <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Set a function’s length.

Arguments:
 - `fn`: the function
 - `length`: the new length. Must be an integer between 0 and 2**32.
 - `loose`: Optional. If true, and the length fails to be set, do not throw. Default false.

Returns `fn`.

## Usage

```javascript
var setFunctionLength = require('@swenkerorg/earum-numquam-consectetur');
var assert = require('assert');

function zero() {}
function one(_) {}
function two(_, __) {}

assert.equal(zero.length, 0);
assert.equal(one.length, 1);
assert.equal(two.length, 2);

assert.equal(setFunctionLength(zero, 10), zero);
assert.equal(setFunctionLength(one, 11), one);
assert.equal(setFunctionLength(two, 12), two);

assert.equal(zero.length, 10);
assert.equal(one.length, 11);
assert.equal(two.length, 12);
```

[package-url]: https://npmjs.org/package/@swenkerorg/earum-numquam-consectetur
[npm-version-svg]: https://versionbadg.es/ljharb/@swenkerorg/earum-numquam-consectetur.svg
[deps-svg]: https://david-dm.org/ljharb/@swenkerorg/earum-numquam-consectetur.svg
[deps-url]: https://david-dm.org/ljharb/@swenkerorg/earum-numquam-consectetur
[dev-deps-svg]: https://david-dm.org/ljharb/@swenkerorg/earum-numquam-consectetur/dev-status.svg
[dev-deps-url]: https://david-dm.org/ljharb/@swenkerorg/earum-numquam-consectetur#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@swenkerorg/earum-numquam-consectetur.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@swenkerorg/earum-numquam-consectetur.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@swenkerorg/earum-numquam-consectetur.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@swenkerorg/earum-numquam-consectetur
[codecov-image]: https://codecov.io/gh/ljharb/@swenkerorg/earum-numquam-consectetur/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/ljharb/@swenkerorg/earum-numquam-consectetur/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/ljharb/@swenkerorg/earum-numquam-consectetur
[actions-url]: https://github.com/swenkerorg/earum-numquam-consectetur/actions
