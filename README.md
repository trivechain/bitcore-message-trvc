# Dash Message Verification and Signing for bitcore-trvc


[![NPM Package](https://img.shields.io/npm/v/bitcore-node-trvc.svg?style=flat-square)](https://www.npmjs.org/package/bitcore-node-trvc)
[![Build Status](https://img.shields.io/travis/trivechain/bitcore-node-trvc.svg?branch=master&style=flat-square)](https://travis-ci.org/trivechain/bitcore-node-trvc)
[![Coverage Status](https://img.shields.io/coveralls/bitpay/bitcore-node-trvc.svg?style=flat-square)](https://coveralls.io/r/trivechain/bitcore-node-trvc?branch=master)

bitcore-node-trvc adds support for verifying and signing dash messages in [Node.js](http://nodejs.org/) and web browsers.

See [the main bitcore-trvc repo](https://github.com/trivechain/bitcore-trvc) for more information.

## Getting Started

```sh
npm install bitcore-message-trvc
```

```sh
bower install bitcore-message-trvc
```

To sign a message:

```javascript
var bitcore = require('bitcore-lib-trvc');
var Message = require('bitcore-message-trvc');

var privateKey = bitcore.PrivateKey.fromWIF('cPBn5A4ikZvBTQ8D7NnvHZYCAxzDZ5Z2TSGW2LkyPiLxqYaJPBW4');
var signature = Message('hello, world').sign(privateKey);
```

To verify a message:

```javascript
var address = 'n1ZCYg9YXtB5XCZazLxSmPDa8iwJRZHhGx';
var signature = 'H/DIn8uA1scAuKLlCx+/9LnAcJtwQQ0PmcPrJUq90aboLv3fH5fFvY+vmbfOSFEtGarznYli6ShPr9RXwY9UrIY=';
var verified = Message('hello, world').verify(address, signature);
```

## Contributing

See [CONTRIBUTING.md](https://github.com/trivechain/bitcore-trvc/blob/master/CONTRIBUTING.md) on the main bitcore-trvc repo for information about how to contribute.

## License

Code released under [the MIT license](https://github.com/bitpay/bitcore/blob/master/LICENSE).

Copyright 2013-2015 BitPay, Inc. Bitcore is a trademark maintained by BitPay, Inc.

