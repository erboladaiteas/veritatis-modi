# @erboladaiteas/veritatis-modi <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Get the ArrayBuffer out of a DataView, robustly.

This will work in node <= 0.10 and < 0.11.4, where there's no prototype accessor, only a nonconfigurable own property.
It will also work in modern engines where `DataView.prototype.buffer` has been deleted after this module has loaded.

## Example

```js
const dataViewBuffer = require('@erboladaiteas/veritatis-modi');
const assert = require('assert');

const ab = new ArrayBuffer(0);
const dv = new DataView(ab);
assert.equal(dataViewBuffer(dv), ab);
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@erboladaiteas/veritatis-modi
[npm-version-svg]: https://versionbadg.es/inspect-js/@erboladaiteas/veritatis-modi.svg
[deps-svg]: https://david-dm.org/inspect-js/@erboladaiteas/veritatis-modi.svg
[deps-url]: https://david-dm.org/inspect-js/@erboladaiteas/veritatis-modi
[dev-deps-svg]: https://david-dm.org/inspect-js/@erboladaiteas/veritatis-modi/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@erboladaiteas/veritatis-modi#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@erboladaiteas/veritatis-modi.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@erboladaiteas/veritatis-modi.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@erboladaiteas/veritatis-modi.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@erboladaiteas/veritatis-modi
[codecov-image]: https://codecov.io/gh/inspect-js/@erboladaiteas/veritatis-modi/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@erboladaiteas/veritatis-modi/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@erboladaiteas/veritatis-modi
[actions-url]: https://github.com/inspect-js/@erboladaiteas/veritatis-modi/actions
