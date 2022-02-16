<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->

# toUint32

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Convert a signed 32-bit integer to an unsigned 32-bit integer.

<section class="installation">

## Installation

```bash
npm install @stdlib/number-int32-base-to-uint32
```

Alternatively,

-   To load the package in a website via a `script` tag without installation and bundlers, use the [ES Module][es-module] available on the [`esm` branch][esm-url].
-   If you are using Deno, visit the [`deno` branch][deno-url].
-   For use in Observable, or in browser/node environments, use the [Universal Module Definition (UMD)][umd] build available on the [`umd` branch][umd-url].

</section>

<section class="usage">

## Usage

```javascript
var int32ToUint32 = require( '@stdlib/number-int32-base-to-uint32' );
```

#### int32ToUint32( x )

Converts a signed 32-bit integer to an unsigned 32-bit integer.

```javascript
var float64ToInt32 = require( '@stdlib/number-float64-base-to-int32' );

var y = int32ToUint32( float64ToInt32( -1 ) );
// returns 4294967295

y = int32ToUint32( float64ToInt32( 3 ) );
// returns 3
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
var randu = require( '@stdlib/random-base-randu' );
var MAX_INT32 = require( '@stdlib/constants-int32-max' );
var float64ToInt32 = require( '@stdlib/number-float64-base-to-int32' );
var int32ToUint32 = require( '@stdlib/number-int32-base-to-uint32' );

var uint32;
var int32;
var sign;
var i;

for ( i = 0; i < 100; i++ ) {
    if ( randu() < 0.5 ) {
        sign = -1.0;
    } else {
        sign = 1.0;
    }
    // Generate a random signed 32-bit integer:
    int32 = float64ToInt32( sign*randu()*MAX_INT32 );

    // Convert the signed integer to an unsigned 32-bit integer:
    uint32 = int32ToUint32( int32 );

    console.log( 'int32: %d => uint32: %d', int32, uint32 );
}
```

</section>

<!-- /.examples -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2022. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/number-int32-base-to-uint32.svg
[npm-url]: https://npmjs.org/package/@stdlib/number-int32-base-to-uint32

[test-image]: https://github.com/stdlib-js/number-int32-base-to-uint32/actions/workflows/test.yml/badge.svg
[test-url]: https://github.com/stdlib-js/number-int32-base-to-uint32/actions/workflows/test.yml

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/number-int32-base-to-uint32/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/number-int32-base-to-uint32?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/number-int32-base-to-uint32.svg
[dependencies-url]: https://david-dm.org/stdlib-js/number-int32-base-to-uint32/main

-->

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/number-int32-base-to-uint32/tree/deno
[umd-url]: https://github.com/stdlib-js/number-int32-base-to-uint32/tree/umd
[esm-url]: https://github.com/stdlib-js/number-int32-base-to-uint32/tree/esm

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/number-int32-base-to-uint32/main/LICENSE

</section>

<!-- /.links -->
