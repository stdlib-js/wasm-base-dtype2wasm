<!--

@license Apache-2.0

Copyright (c) 2024 The Stdlib Authors.

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

# dtype2wasm

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Return the WebAssembly data type associated with a provided array [data type][@stdlib/array/dtypes] value.

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->



<section class="usage">

## Usage

To use in Observable,

```javascript
dtype2wasm = require( 'https://cdn.jsdelivr.net/gh/stdlib-js/wasm-base-dtype2wasm@umd/browser.js' )
```
The previous example will load the latest bundled code from the umd branch. Alternatively, you may load a specific version by loading the file from one of the [tagged bundles](https://github.com/stdlib-js/wasm-base-dtype2wasm/tags). For example,

```javascript
dtype2wasm = require( 'https://cdn.jsdelivr.net/gh/stdlib-js/wasm-base-dtype2wasm@v0.1.1-umd/browser.js' )
```

To vendor stdlib functionality and avoid installing dependency trees for Node.js, you can use the UMD server build:

```javascript
var dtype2wasm = require( 'path/to/vendor/umd/wasm-base-dtype2wasm/index.js' )
```

To include the bundle in a webpage,

```html
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/wasm-base-dtype2wasm@umd/browser.js"></script>
```

If no recognized module system is present, access bundle contents via the global scope:

```html
<script type="text/javascript">
(function () {
    window.dtype2wasm;
})();
</script>
```

#### dtype2wasm( dtype )

Returns the WebAssembly data type associated with a provided array [data type][@stdlib/array/dtypes] value.

```javascript
var out = dtype2wasm( 'float64' );
// returns 'float64'

out = dtype2wasm( 'int8' );
// returns 'int8'
```

If provided an unknown or unsupported array data type, the function **assumes** that associated values can be stored as double-precision floating-point numbers and returns `'float64'`.

```javascript
var out = dtype2wasm( 'foobar' );
// returns 'float64'
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/wasm-base-dtype2wasm@umd/browser.js"></script>
<script type="text/javascript">
(function () {

var dtypes = [
    'float64',
    'float32',
    'int8',
    'uint8',
    'uint8c',
    'int16',
    'uint16',
    'int32',
    'uint32',
    'generic'
];

var i;
for ( i = 0; i < dtypes.length; i++ ) {
    console.log( '%s => %s', dtypes[ i ], dtype2wasm( dtypes[ i ] ) );
}

})();
</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

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

Copyright &copy; 2016-2026. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/wasm-base-dtype2wasm.svg
[npm-url]: https://npmjs.org/package/@stdlib/wasm-base-dtype2wasm

[test-image]: https://github.com/stdlib-js/wasm-base-dtype2wasm/actions/workflows/test.yml/badge.svg?branch=v0.1.1
[test-url]: https://github.com/stdlib-js/wasm-base-dtype2wasm/actions/workflows/test.yml?query=branch:v0.1.1

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/wasm-base-dtype2wasm/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/wasm-base-dtype2wasm?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/wasm-base-dtype2wasm.svg
[dependencies-url]: https://david-dm.org/stdlib-js/wasm-base-dtype2wasm/main

-->

[chat-image]: https://img.shields.io/badge/zulip-join_chat-brightgreen.svg
[chat-url]: https://stdlib.zulipchat.com

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/wasm-base-dtype2wasm/tree/deno
[deno-readme]: https://github.com/stdlib-js/wasm-base-dtype2wasm/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/wasm-base-dtype2wasm/tree/umd
[umd-readme]: https://github.com/stdlib-js/wasm-base-dtype2wasm/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/wasm-base-dtype2wasm/tree/esm
[esm-readme]: https://github.com/stdlib-js/wasm-base-dtype2wasm/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/wasm-base-dtype2wasm/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/wasm-base-dtype2wasm/main/LICENSE

[@stdlib/array/dtypes]: https://github.com/stdlib-js/array-dtypes/tree/umd

</section>

<!-- /.links -->
