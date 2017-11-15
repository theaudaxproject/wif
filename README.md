# WIF
[![NPM](http://img.shields.io/npm/v/wif-smart.svg)](https://www.npmjs.org/package/wif-smart)


SmartCash Wallet Import Format encoding/decoding module.


## Example

``` javascript
var wifsmart = require('wif-smart')
var privateKey = new Buffer('0000000000000000000000000000000000000000000000000000000000000001', 'hex')
var key = wifsmart.encode(191, privateKey, true)
// => VFkSCpppSMzG7qXidUPa4F52XzNbSvnr6NytsmB5nPwwnj37EbQ1

var obj = wifsmart.decode(key)
// => {
//	version: 191,
//	privateKey: <Buffer 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 01>,
//	compressed: true
//}

wifsmart.encode(obj)
// => VFkSCpppSMzG7qXidUPa4F52XzNbSvnr6NytsmB5nPwwnj37EbQ1
```

## LICENSE [MIT](LICENSE)
