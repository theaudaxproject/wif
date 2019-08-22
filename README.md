# WIF
[![NPM](http://img.shields.io/npm/v/wif-audax.svg)](https://www.npmjs.org/package/wif-audax)


Audax Wallet Import Format encoding/decoding module.


## Example

``` javascript
var wifaudax = require('wif-audax')
var privateKey = new Buffer('0000000000000000000000000000000000000000000000000000000000000001', 'hex')
var key = wifaudax.encode(142, privateKey, true)
// => VFkSCpppSMzG7qXidUPa4F52XzNbSvnr6NytsmB5nPwwnj37EbQ1

var obj = wifaudax.decode(key)
// => {
//	version: 142,
//	privateKey: <Buffer 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 01>,
//	compressed: true
//}

wifaudax.encode(obj)
// => VFkSCpppSMzG7qXidUPa4F52XzNbSvnr6NytsmB5nPwwnj37EbQ1
```

## LICENSE [MIT](LICENSE)
