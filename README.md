# Trivechain Message Verification and Signing for bitcore-trvc


[![NPM Package](https://img.shields.io/npm/v/bitcore-node-trvc.svg?style=flat-square)](https://www.npmjs.org/package/bitcore-node-trvc)
[![Build Status](https://img.shields.io/travis/trivechain/bitcore-node-trvc.svg?branch=master&style=flat-square)](https://travis-ci.org/trivechain/bitcore-node-trvc)
[![Coverage Status](https://img.shields.io/coveralls/bitpay/bitcore-node-trvc.svg?style=flat-square)](https://coveralls.io/r/trivechain/bitcore-node-trvc?branch=master)

bitcore-message-trvc adds support for verifying and signing trivechain messages in [Node.js](http://nodejs.org/) and web browsers.

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
var signature = Message('Hello TRVC').sign(privateKey);
```

To verify a message:

```javascript
var address = 'TGLAxSQJeyVZ54iTAwqzEDChTV7ogbysax';
var signature = 'H46/yKryIw1lJbYNCzCSzl+5WfV1sVHG2h0mFU9JmC1kQ44jTR07qEON9aJk0cD5gc4XUaTHNNrh4ax9ynEvqwo=';
var verified = Message('Hello TRVC').verify(address, signature);
```

## Contributing

See [CONTRIBUTING.md](https://github.com/trivechain/bitcore-trvc/blob/master/CONTRIBUTING.md) on the main bitcore-trvc repo for information about how to contribute.

## License

Code released under [the MIT license](https://github.com/bitpay/bitcore/blob/master/LICENSE).

Copyright 2013-2015 BitPay, Inc. Bitcore is a trademark maintained by BitPay, Inc.

