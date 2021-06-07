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

# uimul

> Perform C-like multiplication of two unsigned 32-bit integers.

<section class="intro">

</section>

<!-- /.intro -->

<section class="installation">

## Installation

```bash
npm install @stdlib/math-base-special-uimul
```

</section>

<section class="usage">

## Usage

```javascript
var uimul = require( '@stdlib/math-base-special-uimul' );
```

#### uimul( a, b )

Performs C-like multiplication of two unsigned 32-bit integers.

```javascript
var v = uimul( 10>>>0, 4>>>0 );
// returns 40

v = uimul( 2147483648>>>0, 5>>>0 ); // 2^31 * 5 = 10737418240 => 32-bit integer overflow
// returns 2147483648
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

## Notes

-   The function emulates C-like multiplication of two unsigned 32-bit integers.

</section>

<!-- /.notes -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
var discreteUniform = require( '@stdlib/random-base-discrete-uniform' ).factory;
var UINT32_MAX = require( '@stdlib/constants-uint32-max' );
var uimul = require( '@stdlib/math-base-special-uimul' );

var randi;
var a;
var b;
var y;
var i;

randi = discreteUniform( 0, UINT32_MAX );

for ( i = 0; i < 100; i++ ) {
    a = randi()>>>0;
    b = randi()>>>0;
    y = uimul( a, b );
    console.log( '%d x %d = %d', a, b, y );
}
```

</section>

<!-- /.examples -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2021. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/math-base-special-uimul/main/LICENSE

</section>

<!-- /.links -->
