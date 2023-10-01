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


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# toUint32

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Convert a signed 32-bit integer to an unsigned 32-bit integer.



<section class="usage">

## Usage

To use in Observable,

```javascript
int32ToUint32 = require( 'https://cdn.jsdelivr.net/gh/stdlib-js/number-int32-base-to-uint32@umd/browser.js' )
```

To vendor stdlib functionality and avoid installing dependency trees for Node.js, you can use the UMD server build:

```javascript
var int32ToUint32 = require( 'path/to/vendor/umd/number-int32-base-to-uint32/index.js' )
```

To include the bundle in a webpage,

```html
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/number-int32-base-to-uint32@umd/browser.js"></script>
```

If no recognized module system is present, access bundle contents via the global scope:

```html
<script type="text/javascript">
(function () {
    window.int32ToUint32;
})();
</script>
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

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/random-base-randu@umd/browser.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/constants-int32-max@umd/browser.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/number-float64-base-to-int32@umd/browser.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/number-int32-base-to-uint32@umd/browser.js"></script>
<script type="text/javascript">
(function () {

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

})();
</script>
</body>
</html>
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

Copyright &copy; 2016-2023. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/number-int32-base-to-uint32.svg
[npm-url]: https://npmjs.org/package/@stdlib/number-int32-base-to-uint32

[test-image]: https://github.com/stdlib-js/number-int32-base-to-uint32/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/number-int32-base-to-uint32/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/number-int32-base-to-uint32/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/number-int32-base-to-uint32?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/number-int32-base-to-uint32.svg
[dependencies-url]: https://david-dm.org/stdlib-js/number-int32-base-to-uint32/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/number-int32-base-to-uint32/tree/deno
[umd-url]: https://github.com/stdlib-js/number-int32-base-to-uint32/tree/umd
[esm-url]: https://github.com/stdlib-js/number-int32-base-to-uint32/tree/esm
[branches-url]: https://github.com/stdlib-js/number-int32-base-to-uint32/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/number-int32-base-to-uint32/main/LICENSE

</section>

<!-- /.links -->
