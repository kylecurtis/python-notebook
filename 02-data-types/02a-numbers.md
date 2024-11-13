![[numbers-banner.png]]

<br>

In Python, numbers are essential data types with rich functionality for both simple and complex calculations.

<br>

---

<br>

## Integers (`int`)

Integers in Python represent whole numbers, positive or negative, without decimal points. Python supports arbitrary-precision integers, meaning they can grow as large as needed without fixed boundaries.

<br>

```python
positive_int = 42
negative_int = -18
large_int = 10**18

print(positive_int, negative_int, large_int)
```

>[!success]- Code Output
> 42 -18 1000000000000000000

<br>

---

<br>

## **Methods for Integers**

Python's `int` type includes several built-in methods that allow for a wide range of operations, from bit manipulation to type conversions, enhancing the flexibility and power of integer handling.

<br>

---

<br>

### bit_length()

> [!info]
> Returns the number of bits required to represent an integer in binary.
>
> ```python
> num = 42
> print(num.bit_length())
> ```
> > [!success]- Code Output
> 6

<br>

### to_bytes(length, byteorder)

> [!info]
> Converts an integer to a byte array, using a specified `byteorder`.
> 
> ```python
> num = 255
> print(num.to_bytes(2, byteorder='big'))
> ```
> > [!success]- Code Output
> b'\x00\xff'

<br>

### from_bytes(bytes, byteorder)

> [!info]
> Converts a bytes object back to an integer.
>
> ```python
> byte_data = b'\x00\xff'
> print(int.from_bytes(byte_data, byteorder='big'))
> ```
> > [!success]- Code Output
> 255

<br>

### as_integer_ratio()

> [!info]
> Returns a tuple representing the integer as a fraction, allowing interoperability with float methods.
>
> ```python
> num = 42
> print(num.as_integer_ratio())
> ```
> > [!success]- Code Output
> (42, 1)

<br>

### abs()

> [!info]
> Returns the absolute value of an integer.
>
> ```python
> print(abs(-42))
> ```
> > [!success]- Code Output
> 42

<br>

### pow(base, exp[, mod])

> [!info]
> Calculates `base` raised to `exp`, optionally modulo `mod`.
>
> ```python
> print(pow(2, 3))  # Without modulus
> print(pow(2, 3, 3))  # With modulus
> ```
> > [!success]- Code Output
> > 8 
> > 2

<br>

---

<br>

## Floating-Point Numbers (`float`)

Floats represent real numbers with a decimal component. They use double-precision (64-bit) IEEE 754 format, which may introduce minor precision errors.

<br>

```python
positive_float = 3.14159
negative_float = -2.71828
scientific_float = 1.6e-3  # Equivalent to 0.0016

print(positive_float, negative_float, scientific_float)
```

> [!success]- Code Output
> 3.14159 -2.71828 0.0016

<br>

---

<br>

## Methods for Floats

Python’s `float` type provides numerous methods for precise numeric operations, including checks for integer values, conversions, and representations in hexadecimal, making it highly versatile for handling real numbers and scientific calculations.

<br>

---

<br>

### is_integer()

> [!info]
> Checks if the float represents a whole number.
> ```python
> num = 3.0
> print(num.is_integer())
> ```
> > [!success]- Code Output
> True

<br>

### as_integer_ratio()

> [!info]
> Returns a tuple representing the fraction equivalent of the float.
> ```python
> num = 0.75
> print(num.as_integer_ratio())
> ```
> > [!success]- Code Output
> (3, 4)

<br>

### hex()

> [!info]
> Returns the hexadecimal string representation of the float.
> ```python
> num = 3.14
> print(num.hex())
> ```
> > [!success]- Code Output
> '0x1.91eb851eb851fp+1'

<br>

### float.fromhex(string)

> [!info]
> Converts a hexadecimal string back to a float.
> ```python
> hex_str = '0x1.91eb851eb851fp+1'
> print(float.fromhex(hex_str))
> ```
> > [!success]- Code Output
> 3.14

<br>

### abs()

> [!info]
> Returns the absolute value of a float.
> ```python
> print(abs(-3.14159))
> ```
> > [!success]- Code Output
> 3.14159

<br>

---

<br>

## Complex Numbers (`complex`)

Complex numbers consist of a real and an imaginary part, represented as $a + bj$, where $j$ is the imaginary unit satisfying $j^2 = -1$.

<br>

```python
complex_num = 3 + 4j
print(complex_num)
```

> [!success]- Code Output
> (3+4j)

<br>

---

<br>

## Properties and Methods for Complex Numbers

Python’s `complex` type includes properties and methods that allow you to access the real and imaginary components, calculate magnitudes, and perform complex-specific operations such as finding conjugates, making it versatile for handling complex number arithmetic and analysis.

<br>

---

<br>

### real 

> [!info]
> Returns the real part of the complex number.
> ```python
> num = 3 + 4j
> print(num.real)  
> ```
> > [!success]- Code Output
> 3.0  

<br>

### imag

> [!info]
> Returns the imaginary part of the complex number.
> ```python
> num = 3 + 4j
> print(num.imag)
> ```
> > [!success]- Code Output
> 4.0

<br>

### abs()

> [!info]
> Returns the magnitude (modulus) of the complex number.
> ```python
> num = 3 + 4j
> print(abs(num))
> ```
> > [!success]- Code Output
> 5.0

<br>

### conjugate()

> [!info]
> Returns the complex conjugate of the number.
> ```python
> num = 3 + 4j
> print(num.conjugate())
> ```
> > [!success]- Code Output
> (3-4j)

<br>

---

<br>

## Type Conversions

Python provides built-in functions to convert among `int`, `float`, and `complex` types, making it easy to handle and switch data types as needed in arithmetic and data processing.

<br>

```python
print(int(3.8))            # Converts float to int, truncates decimal
print(float(42))          # Converts int to float
print(complex(3, 4))  # Converts to complex form
```

> [!success]- Code Output
> 3  
> 42.0  
> (3+4j)