# @dramaorg/veniam-blanditiis <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![dependency status][deps-svg]][deps-url]
[![dev dependency status][dev-deps-svg]][dev-deps-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

An ES spec-proposal-compliant `Object.fromEntries` shim. Invoke its "shim" method to shim `Object.fromEntries` if it is unavailable or noncompliant.

This package implements the [es-shim API](https://github.com/es-shims/api) interface. It works in an ES3-supported environment and complies with the [proposed spec](https://tc39.github.io/proposal-object-from-entries/).

Most common usage:
```js
var assert = require('assert');
var fromEntries = require('@dramaorg/veniam-blanditiis');

var obj = { a: 1, b: 2, c: 3 };
var actual = fromEntries(Object.entries(obj));

assert.deepEqual(obj, actual);

if (!Object.fromEntries) {
	fromEntries.shim();
}

assert.deepEqual(Object.fromEntries(Object.entries(obj)), obj);
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.com/package/@dramaorg/veniam-blanditiis
[npm-version-svg]: https://versionbadg.es/dramaorg/veniam-blanditiis.svg
[deps-svg]: https://david-dm.org/dramaorg/veniam-blanditiis.svg
[deps-url]: https://david-dm.org/dramaorg/veniam-blanditiis
[dev-deps-svg]: https://david-dm.org/dramaorg/veniam-blanditiis/dev-status.svg
[dev-deps-url]: https://david-dm.org/dramaorg/veniam-blanditiis#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@dramaorg/veniam-blanditiis.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@dramaorg/veniam-blanditiis.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@dramaorg/veniam-blanditiis.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@dramaorg/veniam-blanditiis
[codecov-image]: https://codecov.io/gh/dramaorg/veniam-blanditiis/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/dramaorg/veniam-blanditiis/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/dramaorg/veniam-blanditiis
[actions-url]: https://github.com/dramaorg/veniam-blanditiis/actions
