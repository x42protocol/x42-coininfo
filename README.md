coininfo
========

[![build status](https://api.travis-ci.org/cryptocoinjs/coininfo.svg)](http://travis-ci.org/cryptocoinjs/coininfo)

JavaScript component for crypto currency specific information such as version numbers, DNS seeds, etc.
Works in Node.js and the browser.


Fork
----

This library is a fork of the original [coininfo](https://github.com/cryptocoinjs/coininfo) with support added for x42.


Installation
------------

    npm i x42-coininfo


Usage
-----

```js
var coininfo = require('x42-coininfo')

console.dir(coininfo('LTC')) //use LTC-TEST for testnet
// =>
/*
{ versions:
   { public: 48,
     private: 176,
     scripthash: 5,
     bip32: { public: 27108450, private: 27106558 } } }
*/
```

Could also:

```js
var litecoin = coininfo.litecoin.main
var litecoinTest = coininfo.litecoin.test
```

Useful to use in conjunction with [coinkey](https://github.com/cryptocoinjs/coinkey) and [coinstring](https://github.com/cryptocoinjs/coinstring).


Want to Use With Bitcore or bitcoinjs-lib?
-----------------------------------------

**bitcoinjs-lib example:**

```js
var coininfo = require('x42-coininfo')
var bitcoin = coininfo.bitcoin.main
var bitcoinBitcoinJSLib = bitcoin.toBitcoinJS()
```

**Bitcore example:**

```js
var coininfo = require('coininfo')
var bitcoin = coininfo.bitcoin.main
var bitcoinBitcoreLib = bitcoin.toBitcore()
```


Pull requests?
--------------

Follow the canonical example:

https://github.com/x42protocol/x42-coininfo/blob/master/lib/coins/x42.js


License
-------

MIT
