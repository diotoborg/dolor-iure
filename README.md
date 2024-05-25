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

# Assert

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Assertion utilities.

<section class="installation">

## Installation

```bash
npm install @diotoborg/dolor-iure
```

Alternatively,

-   To load the package in a website via a `script` tag without installation and bundlers, use the [ES Module][es-module] available on the [`esm`][esm-url] branch (see [README][esm-readme]).
-   If you are using Deno, visit the [`deno`][deno-url] branch (see [README][deno-readme] for usage intructions).
-   For use in Observable, or in browser/node environments, use the [Universal Module Definition (UMD)][umd] build available on the [`umd`][umd-url] branch (see [README][umd-readme]).

The [branches.md][branches-url] file summarizes the available branches and displays a diagram illustrating their relationships.

To view installation and usage instructions specific to each branch build, be sure to explicitly navigate to the respective README files on each branch, as linked to above.

</section>

<section class="usage">

## Usage

```javascript
var assert = require( '@diotoborg/dolor-iure' );
```

#### assert

Namespace providing utilities for data type testing and feature detection.

```javascript
var o = assert;
// returns {...}
```

To validate the built-in JavaScript data types, the namespace includes the following assertion utilities:

<!-- <toc pattern="is-+(array|boolean|date-object|function|string|symbol|nan|null|number|object|regexp|symbol|undefined)" > -->

<div class="namespace-toc">

-   <span class="signature">[`isArray( value )`][@diotoborg/dolor-iure/is-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array.</span>
-   <span class="signature">[`isBoolean( value )`][@diotoborg/dolor-iure/is-boolean]</span><span class="delimiter">: </span><span class="description">test if a value is a boolean.</span>
-   <span class="signature">[`isDateObject( value )`][@diotoborg/dolor-iure/is-date-object]</span><span class="delimiter">: </span><span class="description">test if a value is a Date object.</span>
-   <span class="signature">[`isFunction( value )`][@diotoborg/dolor-iure/is-function]</span><span class="delimiter">: </span><span class="description">test if a value is a function.</span>
-   <span class="signature">[`isnan( value )`][@diotoborg/dolor-iure/is-nan]</span><span class="delimiter">: </span><span class="description">test if a value is NaN.</span>
-   <span class="signature">[`isNull( value )`][@diotoborg/dolor-iure/is-null]</span><span class="delimiter">: </span><span class="description">test if a value is null.</span>
-   <span class="signature">[`isNumber( value )`][@diotoborg/dolor-iure/is-number]</span><span class="delimiter">: </span><span class="description">test if a value is a number.</span>
-   <span class="signature">[`isObject( value )`][@diotoborg/dolor-iure/is-object]</span><span class="delimiter">: </span><span class="description">test if a value is an object.</span>
-   <span class="signature">[`isRegExp( value )`][@diotoborg/dolor-iure/is-regexp]</span><span class="delimiter">: </span><span class="description">test if a value is a regular expression.</span>
-   <span class="signature">[`isString( value )`][@diotoborg/dolor-iure/is-string]</span><span class="delimiter">: </span><span class="description">test if a value is a string.</span>
-   <span class="signature">[`isSymbol( value )`][@diotoborg/dolor-iure/is-symbol]</span><span class="delimiter">: </span><span class="description">test if a value is a symbol.</span>
-   <span class="signature">[`isUndefined( value )`][@diotoborg/dolor-iure/is-undefined]</span><span class="delimiter">: </span><span class="description">test if a value is undefined.</span>

</div>

<!-- </toc> -->

For primitive types having corresponding object wrappers, assertion utilities provide `isObject` and `isPrimitive` methods to test for either objects or primitives, respectively.

<!-- eslint-disable no-new-wrappers -->

```javascript
var Boolean = require( '@stdlib/boolean/ctor' );
var isBoolean = require( '@diotoborg/dolor-iure/is-boolean' );

var bool = isBoolean.isObject( new Boolean( false ) );
// returns true

bool = isBoolean.isObject( false );
// returns false

bool = isBoolean.isPrimitive( false );
// returns true
```

Many of the assertion utilities have corresponding packages that test whether array elements are of the given data type:

<!-- <toc pattern="is-+(array|boolean|date-object|function|string|nan|number|object|regexp|symbol|null|undefined)-array" > -->

<div class="namespace-toc">

-   <span class="signature">[`isArrayArray( value )`][@diotoborg/dolor-iure/is-array-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array of arrays.</span>
-   <span class="signature">[`isBooleanArray( value )`][@diotoborg/dolor-iure/is-boolean-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object of booleans.</span>
-   <span class="signature">[`isDateObjectArray( value )`][@diotoborg/dolor-iure/is-date-object-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only Date objects.</span>
-   <span class="signature">[`isFunctionArray( value )`][@diotoborg/dolor-iure/is-function-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only functions.</span>
-   <span class="signature">[`isNaNArray( value )`][@diotoborg/dolor-iure/is-nan-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only NaN values.</span>
-   <span class="signature">[`isNullArray( value )`][@diotoborg/dolor-iure/is-null-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only null values.</span>
-   <span class="signature">[`isNumberArray( value )`][@diotoborg/dolor-iure/is-number-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object of numbers.</span>
-   <span class="signature">[`isObjectArray( value )`][@diotoborg/dolor-iure/is-object-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only objects.</span>
-   <span class="signature">[`isStringArray( value )`][@diotoborg/dolor-iure/is-string-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array of strings.</span>
-   <span class="signature">[`isSymbolArray( value )`][@diotoborg/dolor-iure/is-symbol-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only symbols.</span>

</div>

<!-- </toc> -->

Where applicable, similar to the assertion utilities for built-in data types, array assertion utilities provides methods for testing for an array of primitives or objects.

<!-- eslint-disable no-new-wrappers -->

```javascript
var isStringArray = require( '@diotoborg/dolor-iure/is-string-array' );

var bool = isStringArray( [ 'hello', 'world' ] );
// returns true

bool = isStringArray.primitives( [ 'hello', 'world' ] );
// returns true

bool = isStringArray.objects( [ 'hello', 'world' ] );
// returns false

bool = isStringArray.objects( [ new String( 'hello' ), new String( 'world' ) ] );
// returns true
```

The namespace also contains utilities to test for numbers within a certain range or for numbers satisfying a particular "type":

<!-- <toc pattern="is-*+(number|integer)*" ignore="is-number-array" ignore="is-number" > -->

<div class="namespace-toc">

-   <span class="signature">[`isCubeNumber( value )`][@diotoborg/dolor-iure/is-cube-number]</span><span class="delimiter">: </span><span class="description">test if a value is a cube number.</span>
-   <span class="signature">[`isIntegerArray( value )`][@diotoborg/dolor-iure/is-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only integers.</span>
-   <span class="signature">[`isInteger( value )`][@diotoborg/dolor-iure/is-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having an integer value.</span>
-   <span class="signature">[`isNegativeIntegerArray( value )`][@diotoborg/dolor-iure/is-negative-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only negative integers.</span>
-   <span class="signature">[`isNegativeInteger( value )`][@diotoborg/dolor-iure/is-negative-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a negative integer value.</span>
-   <span class="signature">[`isNegativeNumberArray( value )`][@diotoborg/dolor-iure/is-negative-number-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only negative numbers.</span>
-   <span class="signature">[`isNegativeNumber( value )`][@diotoborg/dolor-iure/is-negative-number]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a negative value.</span>
-   <span class="signature">[`isNonNegativeIntegerArray( value )`][@diotoborg/dolor-iure/is-nonnegative-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only nonnegative integers.</span>
-   <span class="signature">[`isNonNegativeInteger( value )`][@diotoborg/dolor-iure/is-nonnegative-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a nonnegative integer value.</span>
-   <span class="signature">[`isNonNegativeNumberArray( value )`][@diotoborg/dolor-iure/is-nonnegative-number-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only nonnegative numbers.</span>
-   <span class="signature">[`isNonNegativeNumber( value )`][@diotoborg/dolor-iure/is-nonnegative-number]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a nonnegative value.</span>
-   <span class="signature">[`isNonPositiveIntegerArray( value )`][@diotoborg/dolor-iure/is-nonpositive-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only nonpositive integers.</span>
-   <span class="signature">[`isNonPositiveInteger( value )`][@diotoborg/dolor-iure/is-nonpositive-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a nonpositive integer value.</span>
-   <span class="signature">[`isNonPositiveNumberArray( value )`][@diotoborg/dolor-iure/is-nonpositive-number-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only nonpositive numbers.</span>
-   <span class="signature">[`isNonPositiveNumber( value )`][@diotoborg/dolor-iure/is-nonpositive-number]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a nonpositive value.</span>
-   <span class="signature">[`isPositiveIntegerArray( value )`][@diotoborg/dolor-iure/is-positive-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only positive integers.</span>
-   <span class="signature">[`isPositiveInteger( value )`][@diotoborg/dolor-iure/is-positive-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a positive integer value.</span>
-   <span class="signature">[`isPositiveNumberArray( value )`][@diotoborg/dolor-iure/is-positive-number-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only positive numbers.</span>
-   <span class="signature">[`isPositiveNumber( value )`][@diotoborg/dolor-iure/is-positive-number]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a positive value.</span>
-   <span class="signature">[`isSafeIntegerArray( value )`][@diotoborg/dolor-iure/is-safe-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only safe integers.</span>
-   <span class="signature">[`isSafeInteger( value )`][@diotoborg/dolor-iure/is-safe-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a safe integer value.</span>
-   <span class="signature">[`isSquareNumber( value )`][@diotoborg/dolor-iure/is-square-number]</span><span class="delimiter">: </span><span class="description">test if a value is a square number.</span>
-   <span class="signature">[`isSquareTriangularNumber( value )`][@diotoborg/dolor-iure/is-square-triangular-number]</span><span class="delimiter">: </span><span class="description">test if a value is a square triangular number.</span>
-   <span class="signature">[`isTriangularNumber( value )`][@diotoborg/dolor-iure/is-triangular-number]</span><span class="delimiter">: </span><span class="description">test if a value is a triangular number.</span>

</div>

<!-- </toc> -->

The namespace provides utilities for validating typed arrays:

<!-- <toc pattern="is-+(int8|int16|int32|uint8clamped|uint8|uint16|uint32|float32|float64)array"> -->

<div class="namespace-toc">

-   <span class="signature">[`isFloat32Array( value )`][@diotoborg/dolor-iure/is-float32array]</span><span class="delimiter">: </span><span class="description">test if a value is a Float32Array.</span>
-   <span class="signature">[`isFloat64Array( value )`][@diotoborg/dolor-iure/is-float64array]</span><span class="delimiter">: </span><span class="description">test if a value is a Float64Array.</span>
-   <span class="signature">[`isInt16Array( value )`][@diotoborg/dolor-iure/is-int16array]</span><span class="delimiter">: </span><span class="description">test if a value is an Int16Array.</span>
-   <span class="signature">[`isInt32Array( value )`][@diotoborg/dolor-iure/is-int32array]</span><span class="delimiter">: </span><span class="description">test if a value is an Int32Array.</span>
-   <span class="signature">[`isInt8Array( value )`][@diotoborg/dolor-iure/is-int8array]</span><span class="delimiter">: </span><span class="description">test if a value is an Int8Array.</span>
-   <span class="signature">[`isUint16Array( value )`][@diotoborg/dolor-iure/is-uint16array]</span><span class="delimiter">: </span><span class="description">test if a value is a Uint16Array.</span>
-   <span class="signature">[`isUint32Array( value )`][@diotoborg/dolor-iure/is-uint32array]</span><span class="delimiter">: </span><span class="description">test if a value is a Uint32Array.</span>
-   <span class="signature">[`isUint8Array( value )`][@diotoborg/dolor-iure/is-uint8array]</span><span class="delimiter">: </span><span class="description">test if a value is a Uint8Array.</span>
-   <span class="signature">[`isUint8ClampedArray( value )`][@diotoborg/dolor-iure/is-uint8clampedarray]</span><span class="delimiter">: </span><span class="description">test if a value is a Uint8ClampedArray.</span>

</div>

<!-- </toc> -->

The namespace includes utilities for validating `ndarray`s (n-dimensional arrays).

<!-- <toc keywords="+ndarray" > -->

<div class="namespace-toc">

-   <span class="signature">[`isCentrosymmetricMatrix( value )`][@diotoborg/dolor-iure/is-centrosymmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a centrosymmetric matrix.</span>
-   <span class="signature">[`isComplex128MatrixLike( value )`][@diotoborg/dolor-iure/is-complex128matrix-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 2-dimensional ndarray-like object containing double-precision complex floating-point numbers.</span>
-   <span class="signature">[`isComplex128ndarrayLike( value )`][@diotoborg/dolor-iure/is-complex128ndarray-like]</span><span class="delimiter">: </span><span class="description">test if a value is an ndarray-like object containing double-precision complex floating-point numbers.</span>
-   <span class="signature">[`isComplex128VectorLike( value )`][@diotoborg/dolor-iure/is-complex128vector-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 1-dimensional ndarray-like object containing double-precision complex floating-point numbers.</span>
-   <span class="signature">[`isComplex64MatrixLike( value )`][@diotoborg/dolor-iure/is-complex64matrix-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 2-dimensional ndarray-like object containing single-precision complex floating-point numbers.</span>
-   <span class="signature">[`isComplex64ndarrayLike( value )`][@diotoborg/dolor-iure/is-complex64ndarray-like]</span><span class="delimiter">: </span><span class="description">test if a value is an ndarray-like object containing single-precision complex floating-point numbers.</span>
-   <span class="signature">[`isComplex64VectorLike( value )`][@diotoborg/dolor-iure/is-complex64vector-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 1-dimensional ndarray-like object containing single-precision complex floating-point numbers.</span>
-   <span class="signature">[`isFloat32MatrixLike( value )`][@diotoborg/dolor-iure/is-float32matrix-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 2-dimensional ndarray-like object containing single-precision floating-point numbers.</span>
-   <span class="signature">[`isFloat32ndarrayLike( value )`][@diotoborg/dolor-iure/is-float32ndarray-like]</span><span class="delimiter">: </span><span class="description">test if a value is an ndarray-like object containing single-precision floating-point numbers.</span>
-   <span class="signature">[`isFloat32VectorLike( value )`][@diotoborg/dolor-iure/is-float32vector-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 1-dimensional ndarray-like object containing single-precision floating-point numbers.</span>
-   <span class="signature">[`isFloat64MatrixLike( value )`][@diotoborg/dolor-iure/is-float64matrix-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 2-dimensional ndarray-like object containing double-precision floating-point numbers.</span>
-   <span class="signature">[`isFloat64ndarrayLike( value )`][@diotoborg/dolor-iure/is-float64ndarray-like]</span><span class="delimiter">: </span><span class="description">test if a value is an ndarray-like object containing double-precision floating-point numbers.</span>
-   <span class="signature">[`isFloat64VectorLike( value )`][@diotoborg/dolor-iure/is-float64vector-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 1-dimensional ndarray-like object containing double-precision floating-point numbers.</span>
-   <span class="signature">[`isMatrixLike( value )`][@diotoborg/dolor-iure/is-matrix-like]</span><span class="delimiter">: </span><span class="description">test if a value is 2-dimensional ndarray-like object.</span>
-   <span class="signature">[`isndarrayLike( value )`][@diotoborg/dolor-iure/is-ndarray-like]</span><span class="delimiter">: </span><span class="description">test if a value is ndarray-like.</span>
-   <span class="signature">[`isNonSymmetricMatrix( value )`][@diotoborg/dolor-iure/is-nonsymmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a non-symmetric matrix.</span>
-   <span class="signature">[`isPersymmetricMatrix( value )`][@diotoborg/dolor-iure/is-persymmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a persymmetric matrix.</span>
-   <span class="signature">[`isSkewCentrosymmetricMatrix( value )`][@diotoborg/dolor-iure/is-skew-centrosymmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a skew-centrosymmetric matrix.</span>
-   <span class="signature">[`isSkewPersymmetricMatrix( value )`][@diotoborg/dolor-iure/is-skew-persymmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a skew-persymmetric matrix.</span>
-   <span class="signature">[`isSkewSymmetricMatrix( value )`][@diotoborg/dolor-iure/is-skew-symmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a skew-symmetric matrix.</span>
-   <span class="signature">[`isSquareMatrix( value )`][@diotoborg/dolor-iure/is-square-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a 2-dimensional ndarray-like object having equal dimensions.</span>
-   <span class="signature">[`isSymmetricMatrix( value )`][@diotoborg/dolor-iure/is-symmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a symmetric matrix.</span>
-   <span class="signature">[`isVectorLike( value )`][@diotoborg/dolor-iure/is-vector-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 1-dimensional ndarray-like object.</span>

</div>

<!-- </toc> -->

The namespace includes utilities for validating complex numbers and arrays of complex numbers:

<!-- <toc pattern="is-complex*" > -->

<div class="namespace-toc">

-   <span class="signature">[`isComplexLike( value )`][@diotoborg/dolor-iure/is-complex-like]</span><span class="delimiter">: </span><span class="description">test if a value is a complex number-like object.</span>
-   <span class="signature">[`isComplexTypedArrayLike( value )`][@diotoborg/dolor-iure/is-complex-typed-array-like]</span><span class="delimiter">: </span><span class="description">test if a value is complex-typed-array-like.</span>
-   <span class="signature">[`isComplexTypedArray( value )`][@diotoborg/dolor-iure/is-complex-typed-array]</span><span class="delimiter">: </span><span class="description">test if a value is a complex typed array.</span>
-   <span class="signature">[`isComplex( value )`][@diotoborg/dolor-iure/is-complex]</span><span class="delimiter">: </span><span class="description">test if a value is a 64-bit or 128-bit complex number.</span>
-   <span class="signature">[`isComplex128( value )`][@diotoborg/dolor-iure/is-complex128]</span><span class="delimiter">: </span><span class="description">test if a value is a 128-bit complex number.</span>
-   <span class="signature">[`isComplex128Array( value )`][@diotoborg/dolor-iure/is-complex128array]</span><span class="delimiter">: </span><span class="description">test if a value is a Complex128Array.</span>
-   <span class="signature">[`isComplex64( value )`][@diotoborg/dolor-iure/is-complex64]</span><span class="delimiter">: </span><span class="description">test if a value is a 64-bit complex number.</span>
-   <span class="signature">[`isComplex64Array( value )`][@diotoborg/dolor-iure/is-complex64array]</span><span class="delimiter">: </span><span class="description">test if a value is a Complex64Array.</span>

</div>

<!-- </toc> -->

The namespace includes utilities for validating other special arrays or buffers:

<!-- <toc pattern="is-*array*" ignore="is-+(int8|int16|int32|uint8clamped|uint8|uint16|uint32|float32|float64)array" ignore="is-*+(number|integer)*" ignore="is-+(array|boolean|date-object|function|string|nan|number|object|primitive|regexp|symbol|null|undefined)-array" ignore="is-array" keywords="-ndarray" > -->

<div class="namespace-toc">

-   <span class="signature">[`isAccessorArray( value )`][@diotoborg/dolor-iure/is-accessor-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object supporting the accessor (get/set) protocol.</span>
-   <span class="signature">[`isArrayLength( value )`][@diotoborg/dolor-iure/is-array-length]</span><span class="delimiter">: </span><span class="description">test if a value is a valid array length.</span>
-   <span class="signature">[`isArrayLikeObject( value )`][@diotoborg/dolor-iure/is-array-like-object]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object.</span>
-   <span class="signature">[`isArrayLike( value )`][@diotoborg/dolor-iure/is-array-like]</span><span class="delimiter">: </span><span class="description">test if a value is array-like.</span>
-   <span class="signature">[`isArrayBufferView( value )`][@diotoborg/dolor-iure/is-arraybuffer-view]</span><span class="delimiter">: </span><span class="description">test if a value is an ArrayBuffer view.</span>
-   <span class="signature">[`isArrayBuffer( value )`][@diotoborg/dolor-iure/is-arraybuffer]</span><span class="delimiter">: </span><span class="description">test if a value is an ArrayBuffer.</span>
-   <span class="signature">[`isBetweenArray( value, a, b[, left, right] )`][@diotoborg/dolor-iure/is-between-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object where every element is between two values.</span>
-   <span class="signature">[`isBigInt64Array( value )`][@diotoborg/dolor-iure/is-bigint64array]</span><span class="delimiter">: </span><span class="description">test if a value is a BigInt64Array.</span>
-   <span class="signature">[`isBigUint64Array( value )`][@diotoborg/dolor-iure/is-biguint64array]</span><span class="delimiter">: </span><span class="description">test if a value is a BigUint64Array.</span>
-   <span class="signature">[`isCircularArray( value )`][@diotoborg/dolor-iure/is-circular-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array containing a circular reference.</span>
-   <span class="signature">[`isEmptyArrayLikeObject( value )`][@diotoborg/dolor-iure/is-empty-array-like-object]</span><span class="delimiter">: </span><span class="description">test if a value is an empty array-like object.</span>
-   <span class="signature">[`isEmptyArray( value )`][@diotoborg/dolor-iure/is-empty-array]</span><span class="delimiter">: </span><span class="description">test if a value is an empty array.</span>
-   <span class="signature">[`isFalsyArray( value )`][@diotoborg/dolor-iure/is-falsy-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only falsy values.</span>
-   <span class="signature">[`isFiniteArray( value )`][@diotoborg/dolor-iure/is-finite-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only finite numbers.</span>
-   <span class="signature">[`isNumericArray( value )`][@diotoborg/dolor-iure/is-numeric-array]</span><span class="delimiter">: </span><span class="description">test if a value is a numeric array.</span>
-   <span class="signature">[`isPlainObjectArray( value )`][@diotoborg/dolor-iure/is-plain-object-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only plain objects.</span>
-   <span class="signature">[`isProbabilityArray( value )`][@diotoborg/dolor-iure/is-probability-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only probabilities.</span>
-   <span class="signature">[`isSameArray( v1, v2 )`][@diotoborg/dolor-iure/is-same-array]</span><span class="delimiter">: </span><span class="description">test if two arguments are both generic arrays and have the same values.</span>
-   <span class="signature">[`isSameComplex128Array( v1, v2 )`][@diotoborg/dolor-iure/is-same-complex128array]</span><span class="delimiter">: </span><span class="description">test if two arguments are both Complex128Arrays and have the same values.</span>
-   <span class="signature">[`isSameComplex64Array( v1, v2 )`][@diotoborg/dolor-iure/is-same-complex64array]</span><span class="delimiter">: </span><span class="description">test if two arguments are both Complex64Arrays and have the same values.</span>
-   <span class="signature">[`isSameFloat32Array( v1, v2 )`][@diotoborg/dolor-iure/is-same-float32array]</span><span class="delimiter">: </span><span class="description">test if two arguments are both Float32Arrays and have the same values.</span>
-   <span class="signature">[`isSameFloat64Array( v1, v2 )`][@diotoborg/dolor-iure/is-same-float64array]</span><span class="delimiter">: </span><span class="description">test if two arguments are both Float64Arrays and have the same values.</span>
-   <span class="signature">[`isSharedArrayBuffer( value )`][@diotoborg/dolor-iure/is-sharedarraybuffer]</span><span class="delimiter">: </span><span class="description">test if a value is a SharedArrayBuffer.</span>
-   <span class="signature">[`isTruthyArray( value )`][@diotoborg/dolor-iure/is-truthy-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only truthy values.</span>
-   <span class="signature">[`isTypedArrayLength( value )`][@diotoborg/dolor-iure/is-typed-array-length]</span><span class="delimiter">: </span><span class="description">test if a value is a valid typed array length.</span>
-   <span class="signature">[`isTypedArrayLike( value )`][@diotoborg/dolor-iure/is-typed-array-like]</span><span class="delimiter">: </span><span class="description">test if a value is typed-array-like.</span>
-   <span class="signature">[`isTypedArray( value )`][@diotoborg/dolor-iure/is-typed-array]</span><span class="delimiter">: </span><span class="description">test if a value is a typed array.</span>
-   <span class="signature">[`isUnityProbabilityArray( value )`][@diotoborg/dolor-iure/is-unity-probability-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array of probabilities that sum to one.</span>

</div>

<!-- </toc> -->

To test for error objects, the namespace includes the following utilities:

<!-- <toc pattern="is-*error*" > -->

<div class="namespace-toc">

-   <span class="signature">[`isError( value )`][@diotoborg/dolor-iure/is-error]</span><span class="delimiter">: </span><span class="description">test if a value is an Error object.</span>
-   <span class="signature">[`isEvalError( value )`][@diotoborg/dolor-iure/is-eval-error]</span><span class="delimiter">: </span><span class="description">test if a value is an EvalError object.</span>
-   <span class="signature">[`isRangeError( value )`][@diotoborg/dolor-iure/is-range-error]</span><span class="delimiter">: </span><span class="description">test if a value is a RangeError object.</span>
-   <span class="signature">[`isReferenceError( value )`][@diotoborg/dolor-iure/is-reference-error]</span><span class="delimiter">: </span><span class="description">test if a value is a ReferenceError object.</span>
-   <span class="signature">[`isSyntaxError( value )`][@diotoborg/dolor-iure/is-syntax-error]</span><span class="delimiter">: </span><span class="description">test if a value is a SyntaxError object.</span>
-   <span class="signature">[`isTypeError( value )`][@diotoborg/dolor-iure/is-type-error]</span><span class="delimiter">: </span><span class="description">test if a value is a TypeError object.</span>
-   <span class="signature">[`isURIError( value )`][@diotoborg/dolor-iure/is-uri-error]</span><span class="delimiter">: </span><span class="description">test if a value is a URIError object.</span>

</div>

<!-- </toc> -->

The namespace exposes the following constants concerning the current running process:

<!-- <toc pattern="is-+(browser|darwin|electron|electron-main|electron-renderer|little-endian|big-endian|node|web-worker|windows|docker|mobile|touch-device)" > -->

<div class="namespace-toc">

-   <span class="signature">[`IS_BIG_ENDIAN`][@diotoborg/dolor-iure/is-big-endian]</span><span class="delimiter">: </span><span class="description">check if an environment is big endian.</span>
-   <span class="signature">[`IS_BROWSER`][@diotoborg/dolor-iure/is-browser]</span><span class="delimiter">: </span><span class="description">check if the runtime is a web browser.</span>
-   <span class="signature">[`IS_DARWIN`][@diotoborg/dolor-iure/is-darwin]</span><span class="delimiter">: </span><span class="description">boolean indicating if the current process is running on Darwin.</span>
-   <span class="signature">[`IS_DOCKER`][@diotoborg/dolor-iure/is-docker]</span><span class="delimiter">: </span><span class="description">check if the process is running in a Docker container.</span>
-   <span class="signature">[`IS_ELECTRON_MAIN`][@diotoborg/dolor-iure/is-electron-main]</span><span class="delimiter">: </span><span class="description">check if the runtime is the main Electron process.</span>
-   <span class="signature">[`IS_ELECTRON_RENDERER`][@diotoborg/dolor-iure/is-electron-renderer]</span><span class="delimiter">: </span><span class="description">check if the runtime is the Electron renderer process.</span>
-   <span class="signature">[`IS_ELECTRON`][@diotoborg/dolor-iure/is-electron]</span><span class="delimiter">: </span><span class="description">check if the runtime is Electron.</span>
-   <span class="signature">[`IS_LITTLE_ENDIAN`][@diotoborg/dolor-iure/is-little-endian]</span><span class="delimiter">: </span><span class="description">check if an environment is little endian.</span>
-   <span class="signature">[`IS_MOBILE`][@diotoborg/dolor-iure/is-mobile]</span><span class="delimiter">: </span><span class="description">check if the current environment is a mobile device.</span>
-   <span class="signature">[`IS_NODE`][@diotoborg/dolor-iure/is-node]</span><span class="delimiter">: </span><span class="description">check if the runtime is Node.js.</span>
-   <span class="signature">[`IS_TOUCH_DEVICE`][@diotoborg/dolor-iure/is-touch-device]</span><span class="delimiter">: </span><span class="description">check if the current environment is a touch device.</span>
-   <span class="signature">[`IS_WEB_WORKER`][@diotoborg/dolor-iure/is-web-worker]</span><span class="delimiter">: </span><span class="description">check if the runtime is a web worker.</span>
-   <span class="signature">[`IS_WINDOWS`][@diotoborg/dolor-iure/is-windows]</span><span class="delimiter">: </span><span class="description">boolean indicating if the current process is running on Windows.</span>

</div>

<!-- </toc> -->

To test whether a runtime environment supports certain features, the namespace includes the following utilities:

<!-- <toc pattern="has-*-support" > -->

<div class="namespace-toc">

-   <span class="signature">[`hasArrayBufferSupport()`][@diotoborg/dolor-iure/has-arraybuffer-support]</span><span class="delimiter">: </span><span class="description">detect native `ArrayBuffer` support.</span>
-   <span class="signature">[`hasArrowFunctionSupport()`][@diotoborg/dolor-iure/has-arrow-function-support]</span><span class="delimiter">: </span><span class="description">detect native `arrow function` support.</span>
-   <span class="signature">[`hasAsyncAwaitSupport()`][@diotoborg/dolor-iure/has-async-await-support]</span><span class="delimiter">: </span><span class="description">detect native `async`/`await` support.</span>
-   <span class="signature">[`hasAsyncIteratorSymbolSupport()`][@diotoborg/dolor-iure/has-async-iterator-symbol-support]</span><span class="delimiter">: </span><span class="description">detect native `Symbol.asyncIterator` support.</span>
-   <span class="signature">[`hasBigIntSupport()`][@diotoborg/dolor-iure/has-bigint-support]</span><span class="delimiter">: </span><span class="description">detect native `BigInt` support.</span>
-   <span class="signature">[`hasBigInt64ArraySupport()`][@diotoborg/dolor-iure/has-bigint64array-support]</span><span class="delimiter">: </span><span class="description">detect native `BigInt64Array` support.</span>
-   <span class="signature">[`hasBigUint64ArraySupport()`][@diotoborg/dolor-iure/has-biguint64array-support]</span><span class="delimiter">: </span><span class="description">detect native `BigUint64Array` support.</span>
-   <span class="signature">[`hasClassSupport()`][@diotoborg/dolor-iure/has-class-support]</span><span class="delimiter">: </span><span class="description">detect native `class` support.</span>
-   <span class="signature">[`hasDataViewSupport()`][@diotoborg/dolor-iure/has-dataview-support]</span><span class="delimiter">: </span><span class="description">detect native `DataView` support.</span>
-   <span class="signature">[`hasDefinePropertiesSupport()`][@diotoborg/dolor-iure/has-define-properties-support]</span><span class="delimiter">: </span><span class="description">detect `Object.defineProperties` support.</span>
-   <span class="signature">[`hasDefinePropertySupport()`][@diotoborg/dolor-iure/has-define-property-support]</span><span class="delimiter">: </span><span class="description">detect `Object.defineProperty` support.</span>
-   <span class="signature">[`hasFloat32ArraySupport()`][@diotoborg/dolor-iure/has-float32array-support]</span><span class="delimiter">: </span><span class="description">detect native `Float32Array` support.</span>
-   <span class="signature">[`hasFloat64ArraySupport()`][@diotoborg/dolor-iure/has-float64array-support]</span><span class="delimiter">: </span><span class="description">detect native `Float64Array` support.</span>
-   <span class="signature">[`hasFunctionNameSupport()`][@diotoborg/dolor-iure/has-function-name-support]</span><span class="delimiter">: </span><span class="description">detect native function `name` support.</span>
-   <span class="signature">[`hasGeneratorSupport()`][@diotoborg/dolor-iure/has-generator-support]</span><span class="delimiter">: </span><span class="description">detect native `generator function` support.</span>
-   <span class="signature">[`hasGlobalThisSupport()`][@diotoborg/dolor-iure/has-globalthis-support]</span><span class="delimiter">: </span><span class="description">detect `globalThis` support.</span>
-   <span class="signature">[`hasInt16ArraySupport()`][@diotoborg/dolor-iure/has-int16array-support]</span><span class="delimiter">: </span><span class="description">detect native `Int16Array` support.</span>
-   <span class="signature">[`hasInt32ArraySupport()`][@diotoborg/dolor-iure/has-int32array-support]</span><span class="delimiter">: </span><span class="description">detect native `Int32Array` support.</span>
-   <span class="signature">[`hasInt8ArraySupport()`][@diotoborg/dolor-iure/has-int8array-support]</span><span class="delimiter">: </span><span class="description">detect native `Int8Array` support.</span>
-   <span class="signature">[`hasIteratorSymbolSupport()`][@diotoborg/dolor-iure/has-iterator-symbol-support]</span><span class="delimiter">: </span><span class="description">detect native `Symbol.iterator` support.</span>
-   <span class="signature">[`hasMapSupport()`][@diotoborg/dolor-iure/has-map-support]</span><span class="delimiter">: </span><span class="description">detect native `Map` support.</span>
-   <span class="signature">[`hasNodeBufferSupport()`][@diotoborg/dolor-iure/has-node-buffer-support]</span><span class="delimiter">: </span><span class="description">detect native `Buffer` support.</span>
-   <span class="signature">[`hasProxySupport()`][@diotoborg/dolor-iure/has-proxy-support]</span><span class="delimiter">: </span><span class="description">detect native `Proxy` support.</span>
-   <span class="signature">[`hasSetSupport()`][@diotoborg/dolor-iure/has-set-support]</span><span class="delimiter">: </span><span class="description">detect native `Set` support.</span>
-   <span class="signature">[`hasSharedArrayBufferSupport()`][@diotoborg/dolor-iure/has-sharedarraybuffer-support]</span><span class="delimiter">: </span><span class="description">detect native `SharedArrayBuffer` support.</span>
-   <span class="signature">[`hasSymbolSupport()`][@diotoborg/dolor-iure/has-symbol-support]</span><span class="delimiter">: </span><span class="description">detect native `Symbol` support.</span>
-   <span class="signature">[`hasToStringTagSupport()`][@diotoborg/dolor-iure/has-tostringtag-support]</span><span class="delimiter">: </span><span class="description">detect native `Symbol.toStringTag` support.</span>
-   <span class="signature">[`hasUint16ArraySupport()`][@diotoborg/dolor-iure/has-uint16array-support]</span><span class="delimiter">: </span><span class="description">detect native `Uint16Array` support.</span>
-   <span class="signature">[`hasUint32ArraySupport()`][@diotoborg/dolor-iure/has-uint32array-support]</span><span class="delimiter">: </span><span class="description">detect native `Uint32Array` support.</span>
-   <span class="signature">[`hasUint8ArraySupport()`][@diotoborg/dolor-iure/has-uint8array-support]</span><span class="delimiter">: </span><span class="description">detect native `Uint8Array` support.</span>
-   <span class="signature">[`hasUint8ClampedArraySupport()`][@diotoborg/dolor-iure/has-uint8clampedarray-support]</span><span class="delimiter">: </span><span class="description">detect native `Uint8ClampedArray` support.</span>
-   <span class="signature">[`hasWebAssemblySupport()`][@diotoborg/dolor-iure/has-wasm-support]</span><span class="delimiter">: </span><span class="description">detect native WebAssembly support.</span>
-   <span class="signature">[`hasWeakMapSupport()`][@diotoborg/dolor-iure/has-weakmap-support]</span><span class="delimiter">: </span><span class="description">detect native `WeakMap` support.</span>
-   <span class="signature">[`hasWeakSetSupport()`][@diotoborg/dolor-iure/has-weakset-support]</span><span class="delimiter">: </span><span class="description">detect native `WeakSet` support.</span>

</div>

<!-- </toc> -->

The remaining namespace utilities are as follows:

<!-- <toc ignore="is-+(array|boolean|date-object|function|string|symbol|nan|null|number|object|regexp|symbol|undefined)" ignore="is-*+(number|integer)*" ignore="is-*array*" ignore="is-*error*" ignore="is-+(browser|darwin|electron|electron-main|electron-renderer|little-endian|node|web-worker|windows)" ignore="has-*-support" keywords="-ndarray" > -->

<div class="namespace-toc">

-   <span class="signature">[`contains( val, searchValue[, position] )`][@diotoborg/dolor-iure/contains]</span><span class="delimiter">: </span><span class="description">test if an array-like value contains a search value.</span>
-   <span class="signature">[`deepEqual( a, b )`][@diotoborg/dolor-iure/deep-equal]</span><span class="delimiter">: </span><span class="description">test for deep equality between two values.</span>
-   <span class="signature">[`deepHasOwnProp( value, path[, options] )`][@diotoborg/dolor-iure/deep-has-own-property]</span><span class="delimiter">: </span><span class="description">test whether an object contains a nested key path.</span>
-   <span class="signature">[`deepHasProp( value, path[, options] )`][@diotoborg/dolor-iure/deep-has-property]</span><span class="delimiter">: </span><span class="description">test whether an object contains a nested key path, either own or inherited.</span>
-   <span class="signature">[`hasOwnProp( value, property )`][@diotoborg/dolor-iure/has-own-property]</span><span class="delimiter">: </span><span class="description">test if an object has a specified property.</span>
-   <span class="signature">[`hasProp( value, property )`][@diotoborg/dolor-iure/has-property]</span><span class="delimiter">: </span><span class="description">test if an object has a specified property, either own or inherited.</span>
-   <span class="signature">[`hasUTF16SurrogatePairAt( string, position )`][@diotoborg/dolor-iure/has-utf16-surrogate-pair-at]</span><span class="delimiter">: </span><span class="description">test if a position in a string marks the start of a UTF-16 surrogate pair.</span>
-   <span class="signature">[`instanceOf( value, constructor )`][@diotoborg/dolor-iure/instance-of]</span><span class="delimiter">: </span><span class="description">test whether a value has in its prototype chain a specified constructor as a prototype property.</span>
-   <span class="signature">[`isAbsoluteHttpURI( value )`][@diotoborg/dolor-iure/is-absolute-http-uri]</span><span class="delimiter">: </span><span class="description">test whether a value is an absolute HTTP(S) URI.</span>
-   <span class="signature">[`isAbsolutePath( value )`][@diotoborg/dolor-iure/is-absolute-path]</span><span class="delimiter">: </span><span class="description">test if a value is an absolute path.</span>
-   <span class="signature">[`isAbsoluteURI( value )`][@diotoborg/dolor-iure/is-absolute-uri]</span><span class="delimiter">: </span><span class="description">test whether a value is an absolute URI.</span>
-   <span class="signature">[`isAccessorPropertyIn( value, property )`][@diotoborg/dolor-iure/is-accessor-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property has an accessor descriptor.</span>
-   <span class="signature">[`isAccessorProperty( value, property )`][@diotoborg/dolor-iure/is-accessor-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property has an accessor descriptor.</span>
-   <span class="signature">[`isAlphagram( value )`][@diotoborg/dolor-iure/is-alphagram]</span><span class="delimiter">: </span><span class="description">test if a value is an alphagram.</span>
-   <span class="signature">[`isAlphaNumeric( value )`][@diotoborg/dolor-iure/is-alphanumeric]</span><span class="delimiter">: </span><span class="description">test whether a string contains only alphanumeric characters.</span>
-   <span class="signature">[`isAnagram( str, value )`][@diotoborg/dolor-iure/is-anagram]</span><span class="delimiter">: </span><span class="description">test if a value is an anagram.</span>
-   <span class="signature">[`isArguments( value )`][@diotoborg/dolor-iure/is-arguments]</span><span class="delimiter">: </span><span class="description">test if a value is an arguments object.</span>
-   <span class="signature">[`isArrowFunction( value )`][@diotoborg/dolor-iure/is-arrow-function]</span><span class="delimiter">: </span><span class="description">test if a value is an `arrow function`.</span>
-   <span class="signature">[`isASCII( value )`][@diotoborg/dolor-iure/is-ascii]</span><span class="delimiter">: </span><span class="description">test whether a character belongs to the ASCII character set and whether this is true for all characters in a provided string.</span>
-   <span class="signature">[`isBetween( value, a, b[, left, right] )`][@diotoborg/dolor-iure/is-between]</span><span class="delimiter">: </span><span class="description">test if a value is between two values.</span>
-   <span class="signature">[`isBigInt( value )`][@diotoborg/dolor-iure/is-bigint]</span><span class="delimiter">: </span><span class="description">test if a value is a BigInt.</span>
-   <span class="signature">[`isBinaryString( value )`][@diotoborg/dolor-iure/is-binary-string]</span><span class="delimiter">: </span><span class="description">test if a value is a binary string.</span>
-   <span class="signature">[`isBlankString( value )`][@diotoborg/dolor-iure/is-blank-string]</span><span class="delimiter">: </span><span class="description">test if a value is a blank string.</span>
-   <span class="signature">[`isBoxedPrimitive( value )`][@diotoborg/dolor-iure/is-boxed-primitive]</span><span class="delimiter">: </span><span class="description">test if a value is a JavaScript boxed primitive.</span>
-   <span class="signature">[`isBuffer( value )`][@diotoborg/dolor-iure/is-buffer]</span><span class="delimiter">: </span><span class="description">test if a value is a Buffer object.</span>
-   <span class="signature">[`isCamelcase( value )`][@diotoborg/dolor-iure/is-camelcase]</span><span class="delimiter">: </span><span class="description">test if a value is a camelcase string.</span>
-   <span class="signature">[`isCapitalized( value )`][@diotoborg/dolor-iure/is-capitalized]</span><span class="delimiter">: </span><span class="description">test if a value is a string having an uppercase first character.</span>
-   <span class="signature">[`isCircular( value )`][@diotoborg/dolor-iure/is-circular]</span><span class="delimiter">: </span><span class="description">test if a value is a plain object containing a circular reference.</span>
-   <span class="signature">[`isCircular( value )`][@diotoborg/dolor-iure/is-circular]</span><span class="delimiter">: </span><span class="description">test if an object-like value contains a circular reference.</span>
-   <span class="signature">[`isClass( value )`][@diotoborg/dolor-iure/is-class]</span><span class="delimiter">: </span><span class="description">test if a value is a class.</span>
-   <span class="signature">[`isCollection( value )`][@diotoborg/dolor-iure/is-collection]</span><span class="delimiter">: </span><span class="description">test if a value is a collection.</span>
-   <span class="signature">[`isComposite( value )`][@diotoborg/dolor-iure/is-composite]</span><span class="delimiter">: </span><span class="description">test if a value is a composite number.</span>
-   <span class="signature">[`isConfigurablePropertyIn( value, property )`][@diotoborg/dolor-iure/is-configurable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is configurable.</span>
-   <span class="signature">[`isConfigurableProperty( value, property )`][@diotoborg/dolor-iure/is-configurable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is configurable.</span>
-   <span class="signature">[`isConstantcase( value )`][@diotoborg/dolor-iure/is-constantcase]</span><span class="delimiter">: </span><span class="description">test if a value is a constantcase string.</span>
-   <span class="signature">[`isCurrentYear( value )`][@diotoborg/dolor-iure/is-current-year]</span><span class="delimiter">: </span><span class="description">test if a value is the current year.</span>
-   <span class="signature">[`isDataPropertyIn( value, property )`][@diotoborg/dolor-iure/is-data-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property has a data descriptor.</span>
-   <span class="signature">[`isDataProperty( value, property )`][@diotoborg/dolor-iure/is-data-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property has a data descriptor.</span>
-   <span class="signature">[`isDataView( value )`][@diotoborg/dolor-iure/is-dataview]</span><span class="delimiter">: </span><span class="description">test if a value is a DataView.</span>
-   <span class="signature">[`isDigitString( value )`][@diotoborg/dolor-iure/is-digit-string]</span><span class="delimiter">: </span><span class="description">test whether a string contains only numeric digits.</span>
-   <span class="signature">[`isDomainName( value )`][@diotoborg/dolor-iure/is-domain-name]</span><span class="delimiter">: </span><span class="description">test if a value is a domain name.</span>
-   <span class="signature">[`isDurationString( value )`][@diotoborg/dolor-iure/is-duration-string]</span><span class="delimiter">: </span><span class="description">test if a value is a duration string.</span>
-   <span class="signature">[`isEmailAddress( value )`][@diotoborg/dolor-iure/is-email-address]</span><span class="delimiter">: </span><span class="description">test if a value is an email address.</span>
-   <span class="signature">[`isEmptyCollection( value )`][@diotoborg/dolor-iure/is-empty-collection]</span><span class="delimiter">: </span><span class="description">test if a value is an empty collection.</span>
-   <span class="signature">[`isEmptyObject( value )`][@diotoborg/dolor-iure/is-empty-object]</span><span class="delimiter">: </span><span class="description">test if a value is an empty object.</span>
-   <span class="signature">[`isEmptyString( value )`][@diotoborg/dolor-iure/is-empty-string]</span><span class="delimiter">: </span><span class="description">test if a value is an empty string.</span>
-   <span class="signature">[`isEnumerablePropertyIn( value, property )`][@diotoborg/dolor-iure/is-enumerable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is enumerable.</span>
-   <span class="signature">[`isEnumerableProperty( value, property )`][@diotoborg/dolor-iure/is-enumerable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is enumerable.</span>
-   <span class="signature">[`isEven( value )`][@diotoborg/dolor-iure/is-even]</span><span class="delimiter">: </span><span class="description">test if a value is an even number.</span>
-   <span class="signature">[`isFalsy( value )`][@diotoborg/dolor-iure/is-falsy]</span><span class="delimiter">: </span><span class="description">test if a value is falsy.</span>
-   <span class="signature">[`isFinite( value )`][@diotoborg/dolor-iure/is-finite]</span><span class="delimiter">: </span><span class="description">test if a value is a finite number.</span>
-   <span class="signature">[`isGeneratorObjectLike( value )`][@diotoborg/dolor-iure/is-generator-object-like]</span><span class="delimiter">: </span><span class="description">test if a value is `generator` object-like.</span>
-   <span class="signature">[`isGeneratorObject( value )`][@diotoborg/dolor-iure/is-generator-object]</span><span class="delimiter">: </span><span class="description">test if a value is a `generator` object.</span>
-   <span class="signature">[`isgzipBuffer( value )`][@diotoborg/dolor-iure/is-gzip-buffer]</span><span class="delimiter">: </span><span class="description">test if a value is a gzip buffer.</span>
-   <span class="signature">[`isHexString( value )`][@diotoborg/dolor-iure/is-hex-string]</span><span class="delimiter">: </span><span class="description">test whether a string contains only hexadecimal digits.</span>
-   <span class="signature">[`isInfinite( value )`][@diotoborg/dolor-iure/is-infinite]</span><span class="delimiter">: </span><span class="description">test if a value is an infinite number.</span>
-   <span class="signature">[`isInheritedProperty( value, property )`][@diotoborg/dolor-iure/is-inherited-property]</span><span class="delimiter">: </span><span class="description">test if an object has an inherited property.</span>
-   <span class="signature">[`isIterableLike( value )`][@diotoborg/dolor-iure/is-iterable-like]</span><span class="delimiter">: </span><span class="description">test if a value is `iterable`-like.</span>
-   <span class="signature">[`isIteratorLike( value )`][@diotoborg/dolor-iure/is-iterator-like]</span><span class="delimiter">: </span><span class="description">test if a value is `iterator`-like.</span>
-   <span class="signature">[`isJSON( value )`][@diotoborg/dolor-iure/is-json]</span><span class="delimiter">: </span><span class="description">test if a value is a parseable JSON string.</span>
-   <span class="signature">[`isKebabcase( value )`][@diotoborg/dolor-iure/is-kebabcase]</span><span class="delimiter">: </span><span class="description">test if a value is a string in kebab case.</span>
-   <span class="signature">[`isLeapYear( [value] )`][@diotoborg/dolor-iure/is-leap-year]</span><span class="delimiter">: </span><span class="description">test if a value corresponds to a leap year in the Gregorian calendar.</span>
-   <span class="signature">[`isLocalhost( value )`][@diotoborg/dolor-iure/is-localhost]</span><span class="delimiter">: </span><span class="description">test whether a value is a localhost hostname.</span>
-   <span class="signature">[`isLowercase( value )`][@diotoborg/dolor-iure/is-lowercase]</span><span class="delimiter">: </span><span class="description">test if a value is a lowercase string.</span>
-   <span class="signature">[`isMethodIn( value, property )`][@diotoborg/dolor-iure/is-method-in]</span><span class="delimiter">: </span><span class="description">test if an object has a specified method name, either own or inherited.</span>
-   <span class="signature">[`isMethod( value, property )`][@diotoborg/dolor-iure/is-method]</span><span class="delimiter">: </span><span class="description">test if an object has a specified method name.</span>
-   <span class="signature">[`isMultiSlice( value )`][@diotoborg/dolor-iure/is-multi-slice]</span><span class="delimiter">: </span><span class="description">test if a value is a `MultiSlice`.</span>
-   <span class="signature">[`isNamedTypedTupleLike( value )`][@diotoborg/dolor-iure/is-named-typed-tuple-like]</span><span class="delimiter">: </span><span class="description">test if a value is named typed tuple-like.</span>
-   <span class="signature">[`isNativeFunction( value )`][@diotoborg/dolor-iure/is-native-function]</span><span class="delimiter">: </span><span class="description">test if a value is a native function.</span>
-   <span class="signature">[`isNegativeZero( value )`][@diotoborg/dolor-iure/is-negative-zero]</span><span class="delimiter">: </span><span class="description">test if a value is a number equal to negative zero.</span>
-   <span class="signature">[`isNodeBuiltin( value )`][@diotoborg/dolor-iure/is-node-builtin]</span><span class="delimiter">: </span><span class="description">test whether a string matches a Node.js built-in module name.</span>
-   <span class="signature">[`isNodeDuplexStreamLike( value )`][@diotoborg/dolor-iure/is-node-duplex-stream-like]</span><span class="delimiter">: </span><span class="description">test if a value is Node duplex stream-like.</span>
-   <span class="signature">[`isNodeReadableStreamLike( value )`][@diotoborg/dolor-iure/is-node-readable-stream-like]</span><span class="delimiter">: </span><span class="description">test if a value is Node readable stream-like.</span>
-   <span class="signature">[`isNodeREPL()`][@diotoborg/dolor-iure/is-node-repl]</span><span class="delimiter">: </span><span class="description">check if running in a Node.js REPL environment.</span>
-   <span class="signature">[`isNodeStreamLike( value )`][@diotoborg/dolor-iure/is-node-stream-like]</span><span class="delimiter">: </span><span class="description">test if a value is Node stream-like.</span>
-   <span class="signature">[`isNodeTransformStreamLike( value )`][@diotoborg/dolor-iure/is-node-transform-stream-like]</span><span class="delimiter">: </span><span class="description">test if a value is Node transform stream-like.</span>
-   <span class="signature">[`isNodeWritableStreamLike( value )`][@diotoborg/dolor-iure/is-node-writable-stream-like]</span><span class="delimiter">: </span><span class="description">test if a value is Node writable stream-like.</span>
-   <span class="signature">[`isNonConfigurablePropertyIn( value, property )`][@diotoborg/dolor-iure/is-nonconfigurable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is non-configurable.</span>
-   <span class="signature">[`isNonConfigurableProperty( value, property )`][@diotoborg/dolor-iure/is-nonconfigurable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is non-configurable.</span>
-   <span class="signature">[`isNonEnumerablePropertyIn( value, property )`][@diotoborg/dolor-iure/is-nonenumerable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is non-enumerable.</span>
-   <span class="signature">[`isNonEnumerableProperty( value, property )`][@diotoborg/dolor-iure/is-nonenumerable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is non-enumerable.</span>
-   <span class="signature">[`isNonNegativeFinite( value )`][@diotoborg/dolor-iure/is-nonnegative-finite]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a nonnegative finite value.</span>
-   <span class="signature">[`isObjectLike( value )`][@diotoborg/dolor-iure/is-object-like]</span><span class="delimiter">: </span><span class="description">test if a value is object-like.</span>
-   <span class="signature">[`isOdd( value )`][@diotoborg/dolor-iure/is-odd]</span><span class="delimiter">: </span><span class="description">test if a value is an odd number.</span>
-   <span class="signature">[`isPascalcase( value )`][@diotoborg/dolor-iure/is-pascalcase]</span><span class="delimiter">: </span><span class="description">test if a value is a string in Pascal case.</span>
-   <span class="signature">[`isPlainObject( value )`][@diotoborg/dolor-iure/is-plain-object]</span><span class="delimiter">: </span><span class="description">test if a value is a plain object.</span>
-   <span class="signature">[`isPositiveZero( value )`][@diotoborg/dolor-iure/is-positive-zero]</span><span class="delimiter">: </span><span class="description">test if a value is a number equal to positive zero.</span>
-   <span class="signature">[`isPrime( value )`][@diotoborg/dolor-iure/is-prime]</span><span class="delimiter">: </span><span class="description">test if a value is a prime number.</span>
-   <span class="signature">[`isPrimitive( value )`][@diotoborg/dolor-iure/is-primitive]</span><span class="delimiter">: </span><span class="description">test if a value is a JavaScript primitive.</span>
-   <span class="signature">[`isPRNGLike( value )`][@diotoborg/dolor-iure/is-prng-like]</span><span class="delimiter">: </span><span class="description">test if a value is PRNG-like.</span>
-   <span class="signature">[`isProbability( value )`][@diotoborg/dolor-iure/is-probability]</span><span class="delimiter">: </span><span class="description">test if a value is a probability.</span>
-   <span class="signature">[`isPropertyKey( value )`][@diotoborg/dolor-iure/is-property-key]</span><span class="delimiter">: </span><span class="description">test whether a value is a property key.</span>
-   <span class="signature">[`isPrototypeOf( obj, prototype )`][@diotoborg/dolor-iure/is-prototype-of]</span><span class="delimiter">: </span><span class="description">test if an object's prototype chain contains a provided prototype.</span>
-   <span class="signature">[`isReadOnlyPropertyIn( value, property )`][@diotoborg/dolor-iure/is-read-only-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is read-only.</span>
-   <span class="signature">[`isReadOnlyProperty( value, property )`][@diotoborg/dolor-iure/is-read-only-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is read-only.</span>
-   <span class="signature">[`isReadWritePropertyIn( value, property )`][@diotoborg/dolor-iure/is-read-write-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is readable and writable.</span>
-   <span class="signature">[`isReadWriteProperty( value, property )`][@diotoborg/dolor-iure/is-read-write-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is readable and writable.</span>
-   <span class="signature">[`isReadablePropertyIn( value, property )`][@diotoborg/dolor-iure/is-readable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is readable.</span>
-   <span class="signature">[`isReadableProperty( value, property )`][@diotoborg/dolor-iure/is-readable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is readable.</span>
-   <span class="signature">[`isRegExpString( value )`][@diotoborg/dolor-iure/is-regexp-string]</span><span class="delimiter">: </span><span class="description">test if a value is a regular expression string.</span>
-   <span class="signature">[`isRelativePath( value )`][@diotoborg/dolor-iure/is-relative-path]</span><span class="delimiter">: </span><span class="description">test if a value is a relative path.</span>
-   <span class="signature">[`isRelativeURI( value )`][@diotoborg/dolor-iure/is-relative-uri]</span><span class="delimiter">: </span><span class="description">test whether a value is a relative URI.</span>
-   <span class="signature">[`isSameComplex128( v1, v2 )`][@diotoborg/dolor-iure/is-same-complex128]</span><span class="delimiter">: </span><span class="description">test if two arguments are both double-precision complex floating-point numbers and have the same value.</span>
-   <span class="signature">[`isSameComplex64( v1, v2 )`][@diotoborg/dolor-iure/is-same-complex64]</span><span class="delimiter">: </span><span class="description">test if two arguments are both single-precision complex floating-point numbers and have the same value.</span>
-   <span class="signature">[`isSameNativeClass( a, b )`][@diotoborg/dolor-iure/is-same-native-class]</span><span class="delimiter">: </span><span class="description">test if two arguments have the same native class.</span>
-   <span class="signature">[`isSameType( a, b )`][@diotoborg/dolor-iure/is-same-type]</span><span class="delimiter">: </span><span class="description">test if two arguments have the same type.</span>
-   <span class="signature">[`isSameValueZero( a, b )`][@diotoborg/dolor-iure/is-same-value-zero]</span><span class="delimiter">: </span><span class="description">test if two arguments are the same value.</span>
-   <span class="signature">[`isSameValue( a, b )`][@diotoborg/dolor-iure/is-same-value]</span><span class="delimiter">: </span><span class="description">test if two arguments are the same value.</span>
-   <span class="signature">[`isSemVer( value )`][@diotoborg/dolor-iure/is-semver]</span><span class="delimiter">: </span><span class="description">test if a value is a semantic version string.</span>
-   <span class="signature">[`isSlice( value )`][@diotoborg/dolor-iure/is-slice]</span><span class="delimiter">: </span><span class="description">test if a value is a `Slice`.</span>
-   <span class="signature">[`isSnakecase( value )`][@diotoborg/dolor-iure/is-snakecase]</span><span class="delimiter">: </span><span class="description">test if a value is a string in snake case.</span>
-   <span class="signature">[`isStartcase( value )`][@diotoborg/dolor-iure/is-startcase]</span><span class="delimiter">: </span><span class="description">test if a value is a startcase string.</span>
-   <span class="signature">[`isStrictEqual( a, b )`][@diotoborg/dolor-iure/is-strict-equal]</span><span class="delimiter">: </span><span class="description">test if two arguments are strictly equal.</span>
-   <span class="signature">[`isTruthy( value )`][@diotoborg/dolor-iure/is-truthy]</span><span class="delimiter">: </span><span class="description">test if a value is truthy.</span>
-   <span class="signature">[`isUNCPath( value )`][@diotoborg/dolor-iure/is-unc-path]</span><span class="delimiter">: </span><span class="description">test if a value is a UNC path.</span>
-   <span class="signature">[`isUndefinedOrNull( value )`][@diotoborg/dolor-iure/is-undefined-or-null]</span><span class="delimiter">: </span><span class="description">test if a value is undefined or null.</span>
-   <span class="signature">[`isUppercase( value )`][@diotoborg/dolor-iure/is-uppercase]</span><span class="delimiter">: </span><span class="description">test if a value is an uppercase string.</span>
-   <span class="signature">[`isURI( value )`][@diotoborg/dolor-iure/is-uri]</span><span class="delimiter">: </span><span class="description">test if a value is a URI.</span>
-   <span class="signature">[`isWhitespace( value )`][@diotoborg/dolor-iure/is-whitespace]</span><span class="delimiter">: </span><span class="description">test whether a string contains only white space characters.</span>
-   <span class="signature">[`isWritablePropertyIn( value, property )`][@diotoborg/dolor-iure/is-writable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is writable.</span>
-   <span class="signature">[`isWritableProperty( value, property )`][@diotoborg/dolor-iure/is-writable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is writable.</span>
-   <span class="signature">[`isWriteOnlyPropertyIn( value, property )`][@diotoborg/dolor-iure/is-write-only-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is write-only.</span>
-   <span class="signature">[`isWriteOnlyProperty( value, property )`][@diotoborg/dolor-iure/is-write-only-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is write-only.</span>
-   <span class="signature">[`tools`][@diotoborg/dolor-iure/tools]</span><span class="delimiter">: </span><span class="description">assertion utility tools.</span>

</div>

<!-- </toc> -->

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- TODO: better examples -->

<!-- eslint no-undef: "error" -->

```javascript
var objectKeys = require( '@stdlib/utils/keys' );
var assert = require( '@diotoborg/dolor-iure' );

console.log( objectKeys( assert ) );
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

Copyright &copy; 2016-2024. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@diotoborg/dolor-iure.svg
[npm-url]: https://npmjs.org/package/@diotoborg/dolor-iure

[test-image]: https://github.com/diotoborg/dolor-iure/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/diotoborg/dolor-iure/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/diotoborg/dolor-iure/main.svg
[coverage-url]: https://codecov.io/github/diotoborg/dolor-iure?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/diotoborg/dolor-iure.svg
[dependencies-url]: https://david-dm.org/diotoborg/dolor-iure/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/diotoborg/dolor-iure/tree/deno
[deno-readme]: https://github.com/diotoborg/dolor-iure/blob/deno/README.md
[umd-url]: https://github.com/diotoborg/dolor-iure/tree/umd
[umd-readme]: https://github.com/diotoborg/dolor-iure/blob/umd/README.md
[esm-url]: https://github.com/diotoborg/dolor-iure/tree/esm
[esm-readme]: https://github.com/diotoborg/dolor-iure/blob/esm/README.md
[branches-url]: https://github.com/diotoborg/dolor-iure/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/diotoborg/dolor-iure/main/LICENSE

<!-- <toc-links> -->

[@diotoborg/dolor-iure/contains]: https://github.com/diotoborg/dolor-iure/tree/main/contains

[@diotoborg/dolor-iure/deep-equal]: https://github.com/diotoborg/dolor-iure/tree/main/deep-equal

[@diotoborg/dolor-iure/deep-has-own-property]: https://github.com/diotoborg/dolor-iure/tree/main/deep-has-own-property

[@diotoborg/dolor-iure/deep-has-property]: https://github.com/diotoborg/dolor-iure/tree/main/deep-has-property

[@diotoborg/dolor-iure/has-own-property]: https://github.com/diotoborg/dolor-iure/tree/main/has-own-property

[@diotoborg/dolor-iure/has-property]: https://github.com/diotoborg/dolor-iure/tree/main/has-property

[@diotoborg/dolor-iure/has-utf16-surrogate-pair-at]: https://github.com/diotoborg/dolor-iure/tree/main/has-utf16-surrogate-pair-at

[@diotoborg/dolor-iure/instance-of]: https://github.com/diotoborg/dolor-iure/tree/main/instance-of

[@diotoborg/dolor-iure/is-absolute-http-uri]: https://github.com/diotoborg/dolor-iure/tree/main/is-absolute-http-uri

[@diotoborg/dolor-iure/is-absolute-path]: https://github.com/diotoborg/dolor-iure/tree/main/is-absolute-path

[@diotoborg/dolor-iure/is-absolute-uri]: https://github.com/diotoborg/dolor-iure/tree/main/is-absolute-uri

[@diotoborg/dolor-iure/is-accessor-property-in]: https://github.com/diotoborg/dolor-iure/tree/main/is-accessor-property-in

[@diotoborg/dolor-iure/is-accessor-property]: https://github.com/diotoborg/dolor-iure/tree/main/is-accessor-property

[@diotoborg/dolor-iure/is-alphagram]: https://github.com/diotoborg/dolor-iure/tree/main/is-alphagram

[@diotoborg/dolor-iure/is-alphanumeric]: https://github.com/diotoborg/dolor-iure/tree/main/is-alphanumeric

[@diotoborg/dolor-iure/is-anagram]: https://github.com/diotoborg/dolor-iure/tree/main/is-anagram

[@diotoborg/dolor-iure/is-arguments]: https://github.com/diotoborg/dolor-iure/tree/main/is-arguments

[@diotoborg/dolor-iure/is-arrow-function]: https://github.com/diotoborg/dolor-iure/tree/main/is-arrow-function

[@diotoborg/dolor-iure/is-ascii]: https://github.com/diotoborg/dolor-iure/tree/main/is-ascii

[@diotoborg/dolor-iure/is-between]: https://github.com/diotoborg/dolor-iure/tree/main/is-between

[@diotoborg/dolor-iure/is-bigint]: https://github.com/diotoborg/dolor-iure/tree/main/is-bigint

[@diotoborg/dolor-iure/is-binary-string]: https://github.com/diotoborg/dolor-iure/tree/main/is-binary-string

[@diotoborg/dolor-iure/is-blank-string]: https://github.com/diotoborg/dolor-iure/tree/main/is-blank-string

[@diotoborg/dolor-iure/is-boxed-primitive]: https://github.com/diotoborg/dolor-iure/tree/main/is-boxed-primitive

[@diotoborg/dolor-iure/is-buffer]: https://github.com/diotoborg/dolor-iure/tree/main/is-buffer

[@diotoborg/dolor-iure/is-camelcase]: https://github.com/diotoborg/dolor-iure/tree/main/is-camelcase

[@diotoborg/dolor-iure/is-capitalized]: https://github.com/diotoborg/dolor-iure/tree/main/is-capitalized

[@diotoborg/dolor-iure/is-circular]: https://github.com/diotoborg/dolor-iure/tree/main/is-circular

[@diotoborg/dolor-iure/is-class]: https://github.com/diotoborg/dolor-iure/tree/main/is-class

[@diotoborg/dolor-iure/is-collection]: https://github.com/diotoborg/dolor-iure/tree/main/is-collection

[@diotoborg/dolor-iure/is-composite]: https://github.com/diotoborg/dolor-iure/tree/main/is-composite

[@diotoborg/dolor-iure/is-configurable-property-in]: https://github.com/diotoborg/dolor-iure/tree/main/is-configurable-property-in

[@diotoborg/dolor-iure/is-configurable-property]: https://github.com/diotoborg/dolor-iure/tree/main/is-configurable-property

[@diotoborg/dolor-iure/is-constantcase]: https://github.com/diotoborg/dolor-iure/tree/main/is-constantcase

[@diotoborg/dolor-iure/is-current-year]: https://github.com/diotoborg/dolor-iure/tree/main/is-current-year

[@diotoborg/dolor-iure/is-data-property-in]: https://github.com/diotoborg/dolor-iure/tree/main/is-data-property-in

[@diotoborg/dolor-iure/is-data-property]: https://github.com/diotoborg/dolor-iure/tree/main/is-data-property

[@diotoborg/dolor-iure/is-dataview]: https://github.com/diotoborg/dolor-iure/tree/main/is-dataview

[@diotoborg/dolor-iure/is-digit-string]: https://github.com/diotoborg/dolor-iure/tree/main/is-digit-string

[@diotoborg/dolor-iure/is-domain-name]: https://github.com/diotoborg/dolor-iure/tree/main/is-domain-name

[@diotoborg/dolor-iure/is-duration-string]: https://github.com/diotoborg/dolor-iure/tree/main/is-duration-string

[@diotoborg/dolor-iure/is-email-address]: https://github.com/diotoborg/dolor-iure/tree/main/is-email-address

[@diotoborg/dolor-iure/is-empty-collection]: https://github.com/diotoborg/dolor-iure/tree/main/is-empty-collection

[@diotoborg/dolor-iure/is-empty-object]: https://github.com/diotoborg/dolor-iure/tree/main/is-empty-object

[@diotoborg/dolor-iure/is-empty-string]: https://github.com/diotoborg/dolor-iure/tree/main/is-empty-string

[@diotoborg/dolor-iure/is-enumerable-property-in]: https://github.com/diotoborg/dolor-iure/tree/main/is-enumerable-property-in

[@diotoborg/dolor-iure/is-enumerable-property]: https://github.com/diotoborg/dolor-iure/tree/main/is-enumerable-property

[@diotoborg/dolor-iure/is-even]: https://github.com/diotoborg/dolor-iure/tree/main/is-even

[@diotoborg/dolor-iure/is-falsy]: https://github.com/diotoborg/dolor-iure/tree/main/is-falsy

[@diotoborg/dolor-iure/is-finite]: https://github.com/diotoborg/dolor-iure/tree/main/is-finite

[@diotoborg/dolor-iure/is-generator-object-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-generator-object-like

[@diotoborg/dolor-iure/is-generator-object]: https://github.com/diotoborg/dolor-iure/tree/main/is-generator-object

[@diotoborg/dolor-iure/is-gzip-buffer]: https://github.com/diotoborg/dolor-iure/tree/main/is-gzip-buffer

[@diotoborg/dolor-iure/is-hex-string]: https://github.com/diotoborg/dolor-iure/tree/main/is-hex-string

[@diotoborg/dolor-iure/is-infinite]: https://github.com/diotoborg/dolor-iure/tree/main/is-infinite

[@diotoborg/dolor-iure/is-inherited-property]: https://github.com/diotoborg/dolor-iure/tree/main/is-inherited-property

[@diotoborg/dolor-iure/is-iterable-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-iterable-like

[@diotoborg/dolor-iure/is-iterator-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-iterator-like

[@diotoborg/dolor-iure/is-json]: https://github.com/diotoborg/dolor-iure/tree/main/is-json

[@diotoborg/dolor-iure/is-kebabcase]: https://github.com/diotoborg/dolor-iure/tree/main/is-kebabcase

[@diotoborg/dolor-iure/is-leap-year]: https://github.com/diotoborg/dolor-iure/tree/main/is-leap-year

[@diotoborg/dolor-iure/is-localhost]: https://github.com/diotoborg/dolor-iure/tree/main/is-localhost

[@diotoborg/dolor-iure/is-lowercase]: https://github.com/diotoborg/dolor-iure/tree/main/is-lowercase

[@diotoborg/dolor-iure/is-method-in]: https://github.com/diotoborg/dolor-iure/tree/main/is-method-in

[@diotoborg/dolor-iure/is-method]: https://github.com/diotoborg/dolor-iure/tree/main/is-method

[@diotoborg/dolor-iure/is-multi-slice]: https://github.com/diotoborg/dolor-iure/tree/main/is-multi-slice

[@diotoborg/dolor-iure/is-named-typed-tuple-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-named-typed-tuple-like

[@diotoborg/dolor-iure/is-native-function]: https://github.com/diotoborg/dolor-iure/tree/main/is-native-function

[@diotoborg/dolor-iure/is-negative-zero]: https://github.com/diotoborg/dolor-iure/tree/main/is-negative-zero

[@diotoborg/dolor-iure/is-node-builtin]: https://github.com/diotoborg/dolor-iure/tree/main/is-node-builtin

[@diotoborg/dolor-iure/is-node-duplex-stream-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-node-duplex-stream-like

[@diotoborg/dolor-iure/is-node-readable-stream-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-node-readable-stream-like

[@diotoborg/dolor-iure/is-node-repl]: https://github.com/diotoborg/dolor-iure/tree/main/is-node-repl

[@diotoborg/dolor-iure/is-node-stream-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-node-stream-like

[@diotoborg/dolor-iure/is-node-transform-stream-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-node-transform-stream-like

[@diotoborg/dolor-iure/is-node-writable-stream-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-node-writable-stream-like

[@diotoborg/dolor-iure/is-nonconfigurable-property-in]: https://github.com/diotoborg/dolor-iure/tree/main/is-nonconfigurable-property-in

[@diotoborg/dolor-iure/is-nonconfigurable-property]: https://github.com/diotoborg/dolor-iure/tree/main/is-nonconfigurable-property

[@diotoborg/dolor-iure/is-nonenumerable-property-in]: https://github.com/diotoborg/dolor-iure/tree/main/is-nonenumerable-property-in

[@diotoborg/dolor-iure/is-nonenumerable-property]: https://github.com/diotoborg/dolor-iure/tree/main/is-nonenumerable-property

[@diotoborg/dolor-iure/is-nonnegative-finite]: https://github.com/diotoborg/dolor-iure/tree/main/is-nonnegative-finite

[@diotoborg/dolor-iure/is-object-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-object-like

[@diotoborg/dolor-iure/is-odd]: https://github.com/diotoborg/dolor-iure/tree/main/is-odd

[@diotoborg/dolor-iure/is-pascalcase]: https://github.com/diotoborg/dolor-iure/tree/main/is-pascalcase

[@diotoborg/dolor-iure/is-plain-object]: https://github.com/diotoborg/dolor-iure/tree/main/is-plain-object

[@diotoborg/dolor-iure/is-positive-zero]: https://github.com/diotoborg/dolor-iure/tree/main/is-positive-zero

[@diotoborg/dolor-iure/is-prime]: https://github.com/diotoborg/dolor-iure/tree/main/is-prime

[@diotoborg/dolor-iure/is-primitive]: https://github.com/diotoborg/dolor-iure/tree/main/is-primitive

[@diotoborg/dolor-iure/is-prng-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-prng-like

[@diotoborg/dolor-iure/is-probability]: https://github.com/diotoborg/dolor-iure/tree/main/is-probability

[@diotoborg/dolor-iure/is-property-key]: https://github.com/diotoborg/dolor-iure/tree/main/is-property-key

[@diotoborg/dolor-iure/is-prototype-of]: https://github.com/diotoborg/dolor-iure/tree/main/is-prototype-of

[@diotoborg/dolor-iure/is-read-only-property-in]: https://github.com/diotoborg/dolor-iure/tree/main/is-read-only-property-in

[@diotoborg/dolor-iure/is-read-only-property]: https://github.com/diotoborg/dolor-iure/tree/main/is-read-only-property

[@diotoborg/dolor-iure/is-read-write-property-in]: https://github.com/diotoborg/dolor-iure/tree/main/is-read-write-property-in

[@diotoborg/dolor-iure/is-read-write-property]: https://github.com/diotoborg/dolor-iure/tree/main/is-read-write-property

[@diotoborg/dolor-iure/is-readable-property-in]: https://github.com/diotoborg/dolor-iure/tree/main/is-readable-property-in

[@diotoborg/dolor-iure/is-readable-property]: https://github.com/diotoborg/dolor-iure/tree/main/is-readable-property

[@diotoborg/dolor-iure/is-regexp-string]: https://github.com/diotoborg/dolor-iure/tree/main/is-regexp-string

[@diotoborg/dolor-iure/is-relative-path]: https://github.com/diotoborg/dolor-iure/tree/main/is-relative-path

[@diotoborg/dolor-iure/is-relative-uri]: https://github.com/diotoborg/dolor-iure/tree/main/is-relative-uri

[@diotoborg/dolor-iure/is-same-complex128]: https://github.com/diotoborg/dolor-iure/tree/main/is-same-complex128

[@diotoborg/dolor-iure/is-same-complex64]: https://github.com/diotoborg/dolor-iure/tree/main/is-same-complex64

[@diotoborg/dolor-iure/is-same-native-class]: https://github.com/diotoborg/dolor-iure/tree/main/is-same-native-class

[@diotoborg/dolor-iure/is-same-type]: https://github.com/diotoborg/dolor-iure/tree/main/is-same-type

[@diotoborg/dolor-iure/is-same-value-zero]: https://github.com/diotoborg/dolor-iure/tree/main/is-same-value-zero

[@diotoborg/dolor-iure/is-same-value]: https://github.com/diotoborg/dolor-iure/tree/main/is-same-value

[@diotoborg/dolor-iure/is-semver]: https://github.com/diotoborg/dolor-iure/tree/main/is-semver

[@diotoborg/dolor-iure/is-slice]: https://github.com/diotoborg/dolor-iure/tree/main/is-slice

[@diotoborg/dolor-iure/is-snakecase]: https://github.com/diotoborg/dolor-iure/tree/main/is-snakecase

[@diotoborg/dolor-iure/is-startcase]: https://github.com/diotoborg/dolor-iure/tree/main/is-startcase

[@diotoborg/dolor-iure/is-strict-equal]: https://github.com/diotoborg/dolor-iure/tree/main/is-strict-equal

[@diotoborg/dolor-iure/is-truthy]: https://github.com/diotoborg/dolor-iure/tree/main/is-truthy

[@diotoborg/dolor-iure/is-unc-path]: https://github.com/diotoborg/dolor-iure/tree/main/is-unc-path

[@diotoborg/dolor-iure/is-undefined-or-null]: https://github.com/diotoborg/dolor-iure/tree/main/is-undefined-or-null

[@diotoborg/dolor-iure/is-uppercase]: https://github.com/diotoborg/dolor-iure/tree/main/is-uppercase

[@diotoborg/dolor-iure/is-uri]: https://github.com/diotoborg/dolor-iure/tree/main/is-uri

[@diotoborg/dolor-iure/is-whitespace]: https://github.com/diotoborg/dolor-iure/tree/main/is-whitespace

[@diotoborg/dolor-iure/is-writable-property-in]: https://github.com/diotoborg/dolor-iure/tree/main/is-writable-property-in

[@diotoborg/dolor-iure/is-writable-property]: https://github.com/diotoborg/dolor-iure/tree/main/is-writable-property

[@diotoborg/dolor-iure/is-write-only-property-in]: https://github.com/diotoborg/dolor-iure/tree/main/is-write-only-property-in

[@diotoborg/dolor-iure/is-write-only-property]: https://github.com/diotoborg/dolor-iure/tree/main/is-write-only-property

[@diotoborg/dolor-iure/tools]: https://github.com/diotoborg/dolor-iure/tree/main/tools

[@diotoborg/dolor-iure/has-arraybuffer-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-arraybuffer-support

[@diotoborg/dolor-iure/has-arrow-function-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-arrow-function-support

[@diotoborg/dolor-iure/has-async-await-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-async-await-support

[@diotoborg/dolor-iure/has-async-iterator-symbol-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-async-iterator-symbol-support

[@diotoborg/dolor-iure/has-bigint-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-bigint-support

[@diotoborg/dolor-iure/has-bigint64array-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-bigint64array-support

[@diotoborg/dolor-iure/has-biguint64array-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-biguint64array-support

[@diotoborg/dolor-iure/has-class-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-class-support

[@diotoborg/dolor-iure/has-dataview-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-dataview-support

[@diotoborg/dolor-iure/has-define-properties-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-define-properties-support

[@diotoborg/dolor-iure/has-define-property-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-define-property-support

[@diotoborg/dolor-iure/has-float32array-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-float32array-support

[@diotoborg/dolor-iure/has-float64array-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-float64array-support

[@diotoborg/dolor-iure/has-function-name-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-function-name-support

[@diotoborg/dolor-iure/has-generator-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-generator-support

[@diotoborg/dolor-iure/has-globalthis-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-globalthis-support

[@diotoborg/dolor-iure/has-int16array-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-int16array-support

[@diotoborg/dolor-iure/has-int32array-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-int32array-support

[@diotoborg/dolor-iure/has-int8array-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-int8array-support

[@diotoborg/dolor-iure/has-iterator-symbol-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-iterator-symbol-support

[@diotoborg/dolor-iure/has-map-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-map-support

[@diotoborg/dolor-iure/has-node-buffer-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-node-buffer-support

[@diotoborg/dolor-iure/has-proxy-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-proxy-support

[@diotoborg/dolor-iure/has-set-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-set-support

[@diotoborg/dolor-iure/has-sharedarraybuffer-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-sharedarraybuffer-support

[@diotoborg/dolor-iure/has-symbol-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-symbol-support

[@diotoborg/dolor-iure/has-tostringtag-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-tostringtag-support

[@diotoborg/dolor-iure/has-uint16array-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-uint16array-support

[@diotoborg/dolor-iure/has-uint32array-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-uint32array-support

[@diotoborg/dolor-iure/has-uint8array-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-uint8array-support

[@diotoborg/dolor-iure/has-uint8clampedarray-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-uint8clampedarray-support

[@diotoborg/dolor-iure/has-wasm-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-wasm-support

[@diotoborg/dolor-iure/has-weakmap-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-weakmap-support

[@diotoborg/dolor-iure/has-weakset-support]: https://github.com/diotoborg/dolor-iure/tree/main/has-weakset-support

[@diotoborg/dolor-iure/is-big-endian]: https://github.com/diotoborg/dolor-iure/tree/main/is-big-endian

[@diotoborg/dolor-iure/is-browser]: https://github.com/diotoborg/dolor-iure/tree/main/is-browser

[@diotoborg/dolor-iure/is-darwin]: https://github.com/diotoborg/dolor-iure/tree/main/is-darwin

[@diotoborg/dolor-iure/is-docker]: https://github.com/diotoborg/dolor-iure/tree/main/is-docker

[@diotoborg/dolor-iure/is-electron-main]: https://github.com/diotoborg/dolor-iure/tree/main/is-electron-main

[@diotoborg/dolor-iure/is-electron-renderer]: https://github.com/diotoborg/dolor-iure/tree/main/is-electron-renderer

[@diotoborg/dolor-iure/is-electron]: https://github.com/diotoborg/dolor-iure/tree/main/is-electron

[@diotoborg/dolor-iure/is-little-endian]: https://github.com/diotoborg/dolor-iure/tree/main/is-little-endian

[@diotoborg/dolor-iure/is-mobile]: https://github.com/diotoborg/dolor-iure/tree/main/is-mobile

[@diotoborg/dolor-iure/is-node]: https://github.com/diotoborg/dolor-iure/tree/main/is-node

[@diotoborg/dolor-iure/is-touch-device]: https://github.com/diotoborg/dolor-iure/tree/main/is-touch-device

[@diotoborg/dolor-iure/is-web-worker]: https://github.com/diotoborg/dolor-iure/tree/main/is-web-worker

[@diotoborg/dolor-iure/is-windows]: https://github.com/diotoborg/dolor-iure/tree/main/is-windows

[@diotoborg/dolor-iure/is-error]: https://github.com/diotoborg/dolor-iure/tree/main/is-error

[@diotoborg/dolor-iure/is-eval-error]: https://github.com/diotoborg/dolor-iure/tree/main/is-eval-error

[@diotoborg/dolor-iure/is-range-error]: https://github.com/diotoborg/dolor-iure/tree/main/is-range-error

[@diotoborg/dolor-iure/is-reference-error]: https://github.com/diotoborg/dolor-iure/tree/main/is-reference-error

[@diotoborg/dolor-iure/is-syntax-error]: https://github.com/diotoborg/dolor-iure/tree/main/is-syntax-error

[@diotoborg/dolor-iure/is-type-error]: https://github.com/diotoborg/dolor-iure/tree/main/is-type-error

[@diotoborg/dolor-iure/is-uri-error]: https://github.com/diotoborg/dolor-iure/tree/main/is-uri-error

[@diotoborg/dolor-iure/is-accessor-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-accessor-array

[@diotoborg/dolor-iure/is-array-length]: https://github.com/diotoborg/dolor-iure/tree/main/is-array-length

[@diotoborg/dolor-iure/is-array-like-object]: https://github.com/diotoborg/dolor-iure/tree/main/is-array-like-object

[@diotoborg/dolor-iure/is-array-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-array-like

[@diotoborg/dolor-iure/is-arraybuffer-view]: https://github.com/diotoborg/dolor-iure/tree/main/is-arraybuffer-view

[@diotoborg/dolor-iure/is-arraybuffer]: https://github.com/diotoborg/dolor-iure/tree/main/is-arraybuffer

[@diotoborg/dolor-iure/is-between-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-between-array

[@diotoborg/dolor-iure/is-bigint64array]: https://github.com/diotoborg/dolor-iure/tree/main/is-bigint64array

[@diotoborg/dolor-iure/is-biguint64array]: https://github.com/diotoborg/dolor-iure/tree/main/is-biguint64array

[@diotoborg/dolor-iure/is-circular-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-circular-array

[@diotoborg/dolor-iure/is-empty-array-like-object]: https://github.com/diotoborg/dolor-iure/tree/main/is-empty-array-like-object

[@diotoborg/dolor-iure/is-empty-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-empty-array

[@diotoborg/dolor-iure/is-falsy-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-falsy-array

[@diotoborg/dolor-iure/is-finite-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-finite-array

[@diotoborg/dolor-iure/is-numeric-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-numeric-array

[@diotoborg/dolor-iure/is-plain-object-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-plain-object-array

[@diotoborg/dolor-iure/is-probability-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-probability-array

[@diotoborg/dolor-iure/is-same-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-same-array

[@diotoborg/dolor-iure/is-same-complex128array]: https://github.com/diotoborg/dolor-iure/tree/main/is-same-complex128array

[@diotoborg/dolor-iure/is-same-complex64array]: https://github.com/diotoborg/dolor-iure/tree/main/is-same-complex64array

[@diotoborg/dolor-iure/is-same-float32array]: https://github.com/diotoborg/dolor-iure/tree/main/is-same-float32array

[@diotoborg/dolor-iure/is-same-float64array]: https://github.com/diotoborg/dolor-iure/tree/main/is-same-float64array

[@diotoborg/dolor-iure/is-sharedarraybuffer]: https://github.com/diotoborg/dolor-iure/tree/main/is-sharedarraybuffer

[@diotoborg/dolor-iure/is-truthy-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-truthy-array

[@diotoborg/dolor-iure/is-typed-array-length]: https://github.com/diotoborg/dolor-iure/tree/main/is-typed-array-length

[@diotoborg/dolor-iure/is-typed-array-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-typed-array-like

[@diotoborg/dolor-iure/is-typed-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-typed-array

[@diotoborg/dolor-iure/is-unity-probability-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-unity-probability-array

[@diotoborg/dolor-iure/is-complex-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-complex-like

[@diotoborg/dolor-iure/is-complex-typed-array-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-complex-typed-array-like

[@diotoborg/dolor-iure/is-complex-typed-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-complex-typed-array

[@diotoborg/dolor-iure/is-complex]: https://github.com/diotoborg/dolor-iure/tree/main/is-complex

[@diotoborg/dolor-iure/is-complex128]: https://github.com/diotoborg/dolor-iure/tree/main/is-complex128

[@diotoborg/dolor-iure/is-complex128array]: https://github.com/diotoborg/dolor-iure/tree/main/is-complex128array

[@diotoborg/dolor-iure/is-complex64]: https://github.com/diotoborg/dolor-iure/tree/main/is-complex64

[@diotoborg/dolor-iure/is-complex64array]: https://github.com/diotoborg/dolor-iure/tree/main/is-complex64array

[@diotoborg/dolor-iure/is-centrosymmetric-matrix]: https://github.com/diotoborg/dolor-iure/tree/main/is-centrosymmetric-matrix

[@diotoborg/dolor-iure/is-complex128matrix-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-complex128matrix-like

[@diotoborg/dolor-iure/is-complex128ndarray-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-complex128ndarray-like

[@diotoborg/dolor-iure/is-complex128vector-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-complex128vector-like

[@diotoborg/dolor-iure/is-complex64matrix-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-complex64matrix-like

[@diotoborg/dolor-iure/is-complex64ndarray-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-complex64ndarray-like

[@diotoborg/dolor-iure/is-complex64vector-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-complex64vector-like

[@diotoborg/dolor-iure/is-float32matrix-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-float32matrix-like

[@diotoborg/dolor-iure/is-float32ndarray-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-float32ndarray-like

[@diotoborg/dolor-iure/is-float32vector-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-float32vector-like

[@diotoborg/dolor-iure/is-float64matrix-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-float64matrix-like

[@diotoborg/dolor-iure/is-float64ndarray-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-float64ndarray-like

[@diotoborg/dolor-iure/is-float64vector-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-float64vector-like

[@diotoborg/dolor-iure/is-matrix-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-matrix-like

[@diotoborg/dolor-iure/is-ndarray-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-ndarray-like

[@diotoborg/dolor-iure/is-nonsymmetric-matrix]: https://github.com/diotoborg/dolor-iure/tree/main/is-nonsymmetric-matrix

[@diotoborg/dolor-iure/is-persymmetric-matrix]: https://github.com/diotoborg/dolor-iure/tree/main/is-persymmetric-matrix

[@diotoborg/dolor-iure/is-skew-centrosymmetric-matrix]: https://github.com/diotoborg/dolor-iure/tree/main/is-skew-centrosymmetric-matrix

[@diotoborg/dolor-iure/is-skew-persymmetric-matrix]: https://github.com/diotoborg/dolor-iure/tree/main/is-skew-persymmetric-matrix

[@diotoborg/dolor-iure/is-skew-symmetric-matrix]: https://github.com/diotoborg/dolor-iure/tree/main/is-skew-symmetric-matrix

[@diotoborg/dolor-iure/is-square-matrix]: https://github.com/diotoborg/dolor-iure/tree/main/is-square-matrix

[@diotoborg/dolor-iure/is-symmetric-matrix]: https://github.com/diotoborg/dolor-iure/tree/main/is-symmetric-matrix

[@diotoborg/dolor-iure/is-vector-like]: https://github.com/diotoborg/dolor-iure/tree/main/is-vector-like

[@diotoborg/dolor-iure/is-float32array]: https://github.com/diotoborg/dolor-iure/tree/main/is-float32array

[@diotoborg/dolor-iure/is-float64array]: https://github.com/diotoborg/dolor-iure/tree/main/is-float64array

[@diotoborg/dolor-iure/is-int16array]: https://github.com/diotoborg/dolor-iure/tree/main/is-int16array

[@diotoborg/dolor-iure/is-int32array]: https://github.com/diotoborg/dolor-iure/tree/main/is-int32array

[@diotoborg/dolor-iure/is-int8array]: https://github.com/diotoborg/dolor-iure/tree/main/is-int8array

[@diotoborg/dolor-iure/is-uint16array]: https://github.com/diotoborg/dolor-iure/tree/main/is-uint16array

[@diotoborg/dolor-iure/is-uint32array]: https://github.com/diotoborg/dolor-iure/tree/main/is-uint32array

[@diotoborg/dolor-iure/is-uint8array]: https://github.com/diotoborg/dolor-iure/tree/main/is-uint8array

[@diotoborg/dolor-iure/is-uint8clampedarray]: https://github.com/diotoborg/dolor-iure/tree/main/is-uint8clampedarray

[@diotoborg/dolor-iure/is-cube-number]: https://github.com/diotoborg/dolor-iure/tree/main/is-cube-number

[@diotoborg/dolor-iure/is-integer-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-integer-array

[@diotoborg/dolor-iure/is-integer]: https://github.com/diotoborg/dolor-iure/tree/main/is-integer

[@diotoborg/dolor-iure/is-negative-integer-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-negative-integer-array

[@diotoborg/dolor-iure/is-negative-integer]: https://github.com/diotoborg/dolor-iure/tree/main/is-negative-integer

[@diotoborg/dolor-iure/is-negative-number-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-negative-number-array

[@diotoborg/dolor-iure/is-negative-number]: https://github.com/diotoborg/dolor-iure/tree/main/is-negative-number

[@diotoborg/dolor-iure/is-nonnegative-integer-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-nonnegative-integer-array

[@diotoborg/dolor-iure/is-nonnegative-integer]: https://github.com/diotoborg/dolor-iure/tree/main/is-nonnegative-integer

[@diotoborg/dolor-iure/is-nonnegative-number-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-nonnegative-number-array

[@diotoborg/dolor-iure/is-nonnegative-number]: https://github.com/diotoborg/dolor-iure/tree/main/is-nonnegative-number

[@diotoborg/dolor-iure/is-nonpositive-integer-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-nonpositive-integer-array

[@diotoborg/dolor-iure/is-nonpositive-integer]: https://github.com/diotoborg/dolor-iure/tree/main/is-nonpositive-integer

[@diotoborg/dolor-iure/is-nonpositive-number-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-nonpositive-number-array

[@diotoborg/dolor-iure/is-nonpositive-number]: https://github.com/diotoborg/dolor-iure/tree/main/is-nonpositive-number

[@diotoborg/dolor-iure/is-positive-integer-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-positive-integer-array

[@diotoborg/dolor-iure/is-positive-integer]: https://github.com/diotoborg/dolor-iure/tree/main/is-positive-integer

[@diotoborg/dolor-iure/is-positive-number-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-positive-number-array

[@diotoborg/dolor-iure/is-positive-number]: https://github.com/diotoborg/dolor-iure/tree/main/is-positive-number

[@diotoborg/dolor-iure/is-safe-integer-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-safe-integer-array

[@diotoborg/dolor-iure/is-safe-integer]: https://github.com/diotoborg/dolor-iure/tree/main/is-safe-integer

[@diotoborg/dolor-iure/is-square-number]: https://github.com/diotoborg/dolor-iure/tree/main/is-square-number

[@diotoborg/dolor-iure/is-square-triangular-number]: https://github.com/diotoborg/dolor-iure/tree/main/is-square-triangular-number

[@diotoborg/dolor-iure/is-triangular-number]: https://github.com/diotoborg/dolor-iure/tree/main/is-triangular-number

[@diotoborg/dolor-iure/is-array-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-array-array

[@diotoborg/dolor-iure/is-boolean-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-boolean-array

[@diotoborg/dolor-iure/is-date-object-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-date-object-array

[@diotoborg/dolor-iure/is-function-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-function-array

[@diotoborg/dolor-iure/is-nan-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-nan-array

[@diotoborg/dolor-iure/is-null-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-null-array

[@diotoborg/dolor-iure/is-number-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-number-array

[@diotoborg/dolor-iure/is-object-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-object-array

[@diotoborg/dolor-iure/is-string-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-string-array

[@diotoborg/dolor-iure/is-symbol-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-symbol-array

[@diotoborg/dolor-iure/is-array]: https://github.com/diotoborg/dolor-iure/tree/main/is-array

[@diotoborg/dolor-iure/is-boolean]: https://github.com/diotoborg/dolor-iure/tree/main/is-boolean

[@diotoborg/dolor-iure/is-date-object]: https://github.com/diotoborg/dolor-iure/tree/main/is-date-object

[@diotoborg/dolor-iure/is-function]: https://github.com/diotoborg/dolor-iure/tree/main/is-function

[@diotoborg/dolor-iure/is-nan]: https://github.com/diotoborg/dolor-iure/tree/main/is-nan

[@diotoborg/dolor-iure/is-null]: https://github.com/diotoborg/dolor-iure/tree/main/is-null

[@diotoborg/dolor-iure/is-number]: https://github.com/diotoborg/dolor-iure/tree/main/is-number

[@diotoborg/dolor-iure/is-object]: https://github.com/diotoborg/dolor-iure/tree/main/is-object

[@diotoborg/dolor-iure/is-regexp]: https://github.com/diotoborg/dolor-iure/tree/main/is-regexp

[@diotoborg/dolor-iure/is-string]: https://github.com/diotoborg/dolor-iure/tree/main/is-string

[@diotoborg/dolor-iure/is-symbol]: https://github.com/diotoborg/dolor-iure/tree/main/is-symbol

[@diotoborg/dolor-iure/is-undefined]: https://github.com/diotoborg/dolor-iure/tree/main/is-undefined

<!-- </toc-links> -->

</section>

<!-- /.links -->
