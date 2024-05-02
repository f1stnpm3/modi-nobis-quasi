# @f1stnpm3/modi-nobis-quasi <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![dependency status][deps-svg]][deps-url]
[![dev dependency status][dev-deps-svg]][dev-deps-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

An ES-spec-compliant shim/polyfill/replacement for the `.cause` property on all Error types that works as far down as ES3

This package implements the [es-shim API](https://github.com/es-shims/api) “multi” interface. It works in an ES3-supported environment and complies with the proposed [spec](https://tc39.es/proposal-@f1stnpm3/modi-nobis-quasi/).

## Getting started

```sh
npm install --save @f1stnpm3/modi-nobis-quasi
```

## Usage/Examples

```js
const assert = require('assert');

require('@f1stnpm3/modi-nobis-quasi/auto');

try {
		x();
} catch (e) {
		const actual = new Error('a better message!', { cause: e });
		assert(actual instanceof Error);
		assert(actual.cause === e);
}
```

## Tests

Clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@f1stnpm3/modi-nobis-quasi
[npm-version-svg]: https://versionbadg.es/es-shims/@f1stnpm3/modi-nobis-quasi.svg
[deps-svg]: https://david-dm.org/es-shims/@f1stnpm3/modi-nobis-quasi.svg
[deps-url]: https://david-dm.org/es-shims/@f1stnpm3/modi-nobis-quasi
[dev-deps-svg]: https://david-dm.org/es-shims/@f1stnpm3/modi-nobis-quasi/dev-status.svg
[dev-deps-url]: https://david-dm.org/es-shims/@f1stnpm3/modi-nobis-quasi#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@f1stnpm3/modi-nobis-quasi.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@f1stnpm3/modi-nobis-quasi.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@f1stnpm3/modi-nobis-quasi.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@f1stnpm3/modi-nobis-quasi
[codecov-image]: https://codecov.io/gh/es-shims/@f1stnpm3/modi-nobis-quasi/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/es-shims/@f1stnpm3/modi-nobis-quasi/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/es-shims/@f1stnpm3/modi-nobis-quasi
[actions-url]: https://github.com/f1stnpm3/modi-nobis-quasi/actions
