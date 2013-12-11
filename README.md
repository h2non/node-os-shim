# os-shim [![Build Status](https://secure.travis-ci.org/AdesisNetlife/node-os-shim.png?branch=master)](http://travis-ci.org/AdesisNetlife/node-os-shim)

> Native OS module API shim for older node.js versions

## About 

Node.js team was frozen the [OS module API][1] in 0.10.x version, however the API differs a bit in lower node.js versions

This shim just provides the missing OS API that exist on the latest node.js native [implementation][2], so you can use it in lower node.js versions and it feels like you are in latest versions

## Installation

```
$ npm install os-shim --save[-dev]
```

## Usage

You simply should use the `os-shim` module instead of the `os` native node.js module

```js
var os = require('os-shim')
os.tmpdir()
```
You can mutate the `os-shim` module object without worring about it can create side effects in the native `os` module object

## The missing API

#### os.tmpdir()
Returns the operating system's default directory for temp files

#### os.endianness()
Returns the endianness of the CPU. Possible values are "BE" or "LE"

#### os.EOL
A constant defining the appropriate End-of-line marker for the operating system

## Contributing

Instead of a formal styleguide, take care to maintain the existing coding style.

Add unit tests for any new or changed functionality

### Development

Clone the repository
```shell
$ git clone https://github.com/adesisnetlife/node-os-shim.git && cd node-os-shim
```

Install dependencies
```shell
$ npm install
```

Run tests
```shell
$ make test
```

## Release History

- **0.1.0** `2013-12-11`
    - Initial release

## To Do

Do you miss something? Open an issue or make a PR!

## Contributors

* [Tomas Aparicio](http://github.com/h2non)

## License

Copyright (c) 2013 Adesis Netlife S.L and contributors

Released under MIT license

[1]: http://nodejs.org/api/os.html
[2]: https://github.com/joyent/node/blob/master/lib/os.js
