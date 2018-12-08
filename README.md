# WIF
[![NPM](http://img.shields.io/npm/v/wif-swift.svg)](https://www.npmjs.org/package/wif-swift)


SwiftCash Wallet Import Format encoding/decoding module.


## Example

``` javascript
var wifswift = require('wif-swift')
var privateKey = new Buffer('0000000000000000000000000000000000000000000000000000000000000001', 'hex')
var key = wifswift.encode(191, privateKey, true)
// => VFkSCpppSMzG7qXidUPa4F52XzNbSvnr6NytsmB5nPwwnj37EbQ1

var obj = wifswift.decode(key)
// => {
//	version: 191,
//	privateKey: <Buffer 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 01>,
//	compressed: true
//}

wifswift.encode(obj)
// => VFkSCpppSMzG7qXidUPa4F52XzNbSvnr6NytsmB5nPwwnj37EbQ1
```

## LICENSE [MIT](LICENSE)
