# X25519 2020 Crypto Suite Context Repository _(x25519-key-agreement-2020-context)_

<!-- [![NPM Version](https://img.shields.io/npm/v/x25519-key-agreement-2020-context.svg?style=flat-square)](https://npm.im/x25519-key-agreement-2020-context) -->

> JSON-LD Context for the X25519 2020 Crypto suite.

## Table of Contents

- [Background](#background)
- [Install](#install)
- [Usage](#usage)
- [Commercial Support](#commercial-support)
- [License](#license)

## Background

See also (related specs):

* [Multibase](https://github.com/multiformats/multibase) (for `proofValue` and `publicKeyMultibase` encoding)

## Install

Requires Node.js 12+

To install via NPM:

```
npm install x25519-key-agreement-2020-context
```

## Usage

```js
const {
  contexts, constants, appContextMap, documentLoader
} = require('x25519-key-agreement-2020-context');

// use URL in a JSON-LD context
const obj = {
  "@context": [
    constants.CONTEXT_URL,
    // ...
  ],
  // ...
};

// Codec term map value for CBOR-LD
constants.CBORLD_CODEC_VALUE
// 0x17

// get context data for a specific context
const data = contexts.get('https://w3id.org/security/suites/x25519-2020/v1');
// ...
```

This package can be used with bundlers, such as [webpack][], in browser
applications.

## API

The library exports the following properties:
- `constants`: A Object that maps constants to well-known context URLs. The
  main constant `CONTEXT_URL` may be updated from time to time to the
  latest context location.
- `contexts`: A `Map` that maps URLs to full context data.
- `appContextMap`: For use with `cborld` library.
- `documentLoader`


## Commercial Support

Commercial support for this library is available upon request from
Digital Bazaar: support@digitalbazaar.com

## License

- BSD 3-Clause © Digital Bazaar
- See the [LICENSE](./LICENSE) file for details.
