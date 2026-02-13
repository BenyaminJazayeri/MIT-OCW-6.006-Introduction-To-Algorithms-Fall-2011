# Arbitrary-Precision Arithmetic Library for RSA

A complete big number arithmetic library implementing Karatsuba multiplication (O(n^log₂3)), Newton-Raphson division with inverse caching, and modular exponentiation (square-and-multiply). Uses hybrid dispatch, switching between asymptotically fast and brute-force algorithms based on input size — the same pattern used in production libraries like GMP. Applied to RSA public-key encryption and decryption.

## Implementation

The `BigNum` class represents numbers as little-endian arrays of `Byte` objects (base-256).

### Construction and Comparison
`zero()`, `one()`, `from_hex()`, `normalize()`, and the full set of comparison operators (`__eq__`, `__ne__`, `__lt__`, `__le__`, `__gt__`, `__ge__`).

### Shifts
`__lshift__` and `__rshift__` multiply and divide by 256^digits.

### Addition and Subtraction
`__add__` uses standard carry-propagation in O(N). `__sub__` uses 2's complement subtraction in O(N).

### Multiplication
Dispatches between two implementations:
- `slow_mul` — O(N²) schoolbook multiplication with good constant factors, used for inputs ≤ 64 digits
- `fast_mul` — Karatsuba multiplication that splits numbers in half, computes three recursive multiplications instead of four, and combines results in O(N^log₂3)

### Division
Dispatches between two implementations:
- `slow_divmod` — O(N²) binary long division using repeated doubling, used for inputs ≤ 256 digits
- `fast_divmod` — Newton-Raphson division using multiplicative inverse approximation with iterative refinement; the inverse is cached for repeated divisions by the same divisor

### Modular Exponentiation
`powmod` implements the square-and-multiply algorithm, processing the exponent bit by bit for efficient modular exponentiation used in RSA.
