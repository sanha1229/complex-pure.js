# cplx.js
Javascript complex number class

## Copyright
&copy; 2021 Sanha, all rights reserved.

## Basic
 
### It's compatible with..
- Front-end Javascript
- Node.js
- Rhino Javascript Engine

## Get Started
```javascript
const { Complex, Cxmath } = require(PATH);

```

## Complex

### Constructor
#### constructor(re, im)
Declare in cartesian form
<sup>[note](https://en.wikipedia.org/wiki/Complex_number#Cartesian_complex_plane)</sup> (if the imaginary part equals zero, you may leave it out.)
```javascript
new Complex(1, 2); // 1+2i
```
|name|type|required|
|:---:|:---:|:---:|
|re|number|O|
|im|number|X|

#### constructor(arg, abs, polarTag)
Declare in polar form
<sup>[note](https://en.wikipedia.org/wiki/Complex_number#Polar_complex_plane)</sup>
```javascript
new Complex(Math.PI, 2, 'polar'); // 2exp(iπ) = -2
```
|name|type|required|
|:---:|:---:|:---:|
|arg|number|O|
|abs|number|O|
|polar|string|O|

#### constructor(cplx)
Copy complex that has already been declared
```javascript
new Complex(z);
```
|name|type|required|
|:---:|:---:|:---:|
|cplx|Complex|O|

### Properties
#### re
Real part
```javascript
z.re;
```

#### im
Imaginary part
```javascript
z.im;
```

#### abs
Absolute value (Modulus)
<sup>[note](https://en.wikipedia.org/wiki/Complex_number#Modulus_and_argument)</sup>
```javascript
z.abs;
```

#### arg
Argument
<sup>[note](https://en.wikipedia.org/wiki/Complex_number#Modulus_and_argument)</sup>
```javascript
z.arg;
```


### Operations & Exponentiation
```javascript
let p = new Complex(1, 2);
let q = new Complex(3, -4);
```
#### Complex add(z)
Addition
<sup>[note](https://en.wikipedia.org/wiki/Complex_number#Addition_and_subtraction)</sup>
```javascript
p.add(q); // 4-2i
p.add(6); // 7+2i
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

#### Complex sub(z)
Subtraction
<sup>[note](https://en.wikipedia.org/wiki/Complex_number#Addition_and_subtraction)</sup>
```javascript
p.sub(q); // -2+6i
p.sub(6); // -5+2i
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

#### Complex mul(z)
Multiplication
<sup>[note1](https://en.wikipedia.org/wiki/Complex_number#Multiplication_and_square)</sup>
<sup>[note2](https://en.wikipedia.org/wiki/Complex_number#Multiplication_and_division_in_polar_form)</sup>
```javascript
p.mul(q); // 11+2i
p.mul(6); // 6+12i
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

#### Complex div(z)
Division
<sup>[note1](https://en.wikipedia.org/wiki/Complex_number#Reciprocal_and_division)</sup>
<sup>[note2](https://en.wikipedia.org/wiki/Complex_number#Multiplication_and_division_in_polar_form)</sup>
```javascript
p.div(q); // -0.2+0.4i
p.div(4); // 0.25+0.5i
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

#### Complex inv(z)
Exponentiation
<sup>[note](https://en.wikipedia.org/wiki/Complex_number#Exponentiation)</sup>
```javascript
p.inv(q); // 932.1391946432212+95.9465336603415i
p.inv(6); // 117+44i
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

## Cxmath

### Additive Inverse & Complex Conjugate

#### Complex opp(z)
Opposite number (Additive inverse)<sup>[note](https://en.wikipedia.org/wiki/Additive_inverse)</sup>
```javascript
Cxmath.opp(z);
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

#### Complex conj(z)
Complex conjugate
<sup>[note](https://en.wikipedia.org/wiki/Complex_conjugate)</sup>
```javascript
Cxmath.conj(z);
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

### Radical Roots
[[note]](https://en.wikipedia.org/wiki/Square_root#Square_roots_of_negative_and_complex_numbers)

#### Complex sqrt(z)
Principal square root
<sup>[note](https://en.wikipedia.org/wiki/Complex_number#Square_root)</sup>
```javascript
Cxmath.sqrt(z);
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

#### Complex cbrt(z)
Principal cube root
```javascript
Cxmath.cbrt(z);
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

### Exponential Function & Logarithm

#### Complex exp(z)
Exponential function
<sup>[note1](https://en.wikipedia.org/wiki/Exponential_function)</sup>
<sup>[note2](https://en.wikipedia.org/wiki/Complex_number#Exponentiation)</sup>
```javascript
Cxmath.exp(z);
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

#### Complex log(a, b)
Logarithm
<sup>[note1](https://en.wikipedia.org/wiki/Logarithm)</sup>
<sup>[note2](https://en.wikipedia.org/wiki/Complex_number#Complex_logarithm)</sup>
defined in principal branch
<sup>[note1](https://en.wikipedia.org/wiki/Principal_branch)</sup>
<sup>[note2](https://en.wikipedia.org/wiki/Branch_point#Branch_cuts)</sup>
with base b and antilogarithm a (if the base equals e, you may leave it out.)
```javascript
Cxmath.log(a); // Natural Logarithm
Cxmath.log(a, 2); // Binary Logarithm
Cxmath.log(a, 10); // Decimal Logarithm
Cxmath.log(a, b);
```
|name|type|required|
|:---:|:---:|:---:|
|a|number/Complex|O|
|b|numner/Complex|X|

### Trigonometric Functions
[[note]](https://en.wikipedia.org/wiki/Trigonometric_functions)

#### Complex sin(z)
Sine
```javascript
sin(z);
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

#### Complex cos(z)
Cosine
```javascript
Cxmath.cos(z);
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

#### Complex tan(z)
Tangent
```javascript
Cxmath.tan(z);
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

### Inverse Trigonometric Functions
[[note]](https://en.wikipedia.org/wiki/Inverse_trigonometric_functions)

#### Complex asin(z)
Arcsine
```javascript
Cxmath.asin(z);
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

#### Complex acos(z)
Arccosine
```javascript
Cxmath.acos(z);
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

#### Complex atan(z)
Arctangent
```javascript
Cxmath.atan(z);
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

#### Complex atan2(w, z)
arctangent2
```javascript
Cxmath.atan2(w, z);
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|
|w|number/Complex|O|

### Hyperbolic Functions
[[note]](https://en.wikipedia.org/wiki/Hyperbolic_functions)

#### Cxmath.sinh(z: number/complex)
Hyperbolic sine
```javascript
Cxmath.sinh(z);
```

#### Cxmath.cosh(z: number/complex)
Hyperbolic cosine
```javascript
Cxmath.cosh(z);
```

#### Cxmath.tanh(z: number/complex)
Hyperbolic tangent
```javascript
Cxmath.tanh(z);
```

### Inverse Hyperbolic Functions
[[note]](https://en.wikipedia.org/wiki/Inverse_hyperbolic_functions)

#### Cxmath.asinh(z: number/complex)
Inverse hyperbolic sine
```javascript
Cxmath.asinh(z);
```

#### Cxmath.acosh(z: number/complex)
Inverse hyperbolic cosine
```javascript
Cxmath.acosh(z);
```

#### Cxmath.atanh(z: number/complex)
Inverse hyperbolic tangent
```javascript
Cxmath.atanh(z);
```

### Sign Function

#### Cxmath.csgn(z: number/complex)
Complex sign function
<sup>[note](https://en.wikipedia.org/wiki/Sign_function#Complex_signum)</sup>
```javascript
Cxmath.csgn(z);
```

### Distance

#### Cxmath.dist(w: number/complex, z: number/complex)
Distance between w and z in the complex plane
```javascript
Cxmath.dist(w, z);
```

### Mean

#### Cxmath.am(z_1, z_2, ..., z_n: number/complex)
Arithmetic mean
```javascript
Cxmath.am(z_1, z_2, ..., z_n);
```

#### Cxmath.gm(z_1, z_2, ..., z_n: number/complex)
Geometric mean
```javascript
Cxmath.gm(z_1, z_2, ..., z_n);
```

### Random

#### Cxmath.random()
Random complex (both real part and imaginary part are more than or equal to 0 and less than 1)
```javascript
Cxmath.random();
```
