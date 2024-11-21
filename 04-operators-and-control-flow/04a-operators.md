![[operators-banner.png]]

<br>

Operators in Python are special symbols or keywords used to perform operations on variables and values. They enable arithmetic, comparisons, logical decisions, and more. Python supports several categories of operators, making it a versatile language for mathematical and logical expressions.

<br>

---

<br>

## Categories of Operators

Python provides the following categories of operators:

- **Arithmetic Operators**: Perform mathematical calculations.
- **Comparison Operators**: Compare two values and return a Boolean.
- **Logical Operators**: Combine Boolean expressions.
- **Bitwise Operators**: Perform operations on binary representations.
- **Identity Operators**: Check object identity.
- **Membership Operators**: Check membership in a sequence.
- **Assignment Operators**: Assign and modify values.

<br>

---

<br>

## Arithmetic Operators

> [!info]
> Used for mathematical operations like addition, subtraction, multiplication, etc.

<br>

### List of Arithmetic Operators

| **Operator** | **Description**     | **Example** | **Result** |
| :----------: | :------------------ | :---------: | :--------: |
|      +       | Addition            |    3 + 2    |     5      |
|      -       | Subtraction         |    3 - 2    |     1      |
|      \*      | Multiplication      |   3 \* 2    |     6      |
|      /       | Division            |    3 / 2    |    1.5     |
|      //      | Floor Division      |   3 // 2    |     1      |
|      %       | Modulus (remainder) |    3 % 2    |     1      |
|     \*\*     | Exponentiation      |  3 \*\* 2   |     9      |

<br>

### Examples

```python
a = 10
b = 3

print(a + b)   # Addition
print(a - b)   # Subtraction
print(a * b)   # Multiplication
print(a / b)   # Division
print(a // b)  # Floor Division
print(a % b)   # Modulus
print(a ** b)  # Exponentiation
```

> [!success]- Code Output
> 13  
> 7  
> 30  
> 3.3333333333333335  
> 3  
> 1  
> 1000

<br>

---

<br>

## Comparison Operators

> [!info]
> Used to compare two values. The result is always a Boolean (True or False).

<br>

### List of Comparison Operators

| **Operator** | **Description**          | **Example** | **Result** |
| :----------: | :----------------------- | :---------: | :--------: |
|      ==      | Equal to                 |   3 == 3    |    True    |
|      !=      | Not equal to             |   3 != 2    |    True    |
|      <       | Less than                |    3 < 5    |    True    |
|      >       | Greater than             |    3 > 5    |   False    |
|      <=      | Less than or equal to    |   3 <= 3    |    True    |
|      >=      | Greater than or equal to |   3 >= 5    |   False    |

<br>

### Examples

```python
x = 5
y = 3

print(x == y) # Equal to
print(x != y) # Not equal to
print(x > y)  # Greater than
print(x < y)  # Less than
print(x >= y) # Greater than or equal to
print(x <= y) # Less than or equal to
```

> [!success]- Code Output
> False  
> True  
> True  
> False  
> True  
> False

<br>

---

<br>

## Logical Operators

> [!info]
> Used to combine Boolean expressions.

<br>

### List of Logical Operators

| **Operator** | **Description**                              | **Example**    | **Result** |
| :----------: | :------------------------------------------- | :------------- | :--------: |
|     and      | Returns True if both operands are True       | True and False |   False    |
|      or      | Returns True if at least one operand is True | True or False  |    True    |
|     not      | Reverses the Boolean value                   | not True       |   False    |

<br>

### Examples

```python
a = True
b = False

print(a and b) # Logical AND
print(a or b)  # Logical OR
print(not a)   # Logical NOT
```

> [!success]- Code Output
> False  
> True  
> False

<br>

---

<br>

## Bitwise Operators

> [!info]
> Perform operations on the binary representation of integers.

<br>

### List of Bitwise Operators

| **Operator** | **Description** | **Example** | **Result** |
| :----------: | :-------------- | :---------: | :--------: |
|      &       | Bitwise AND     |  5 & 3 → 1  |     1      |
|      \|      | Bitwise OR      | 5 \| 3 → 7  |     7      |
|      ^       | Bitwise XOR     |  5 ^ 3 → 6  |     6      |
|      ~       | Bitwise NOT     |   ~5 → -6   |     -6     |
|      <<      | Left Shift      | 5 << 1 → 10 |     10     |
|      >>      | Right Shift     | 5 >> 1 → 2  |     2      |

<br>

### Examples

```python
x = 5 # Binary: 101
y = 3 # Binary: 011

print(x & y)  # Bitwise AND
print(x | y)  # Bitwise OR
print(x ^ y)  # Bitwise XOR
print(~x)     # Bitwise NOT
print(x << 1) # Left Shift
print(x >> 1) # Right Shift
```

> [!success]- Code Output
> 1  
> 7  
> 6  
> -6  
> 10  
> 2

<br>

---

<br>

## Identity Operators

> [!info]
> Used to compare the identity of two objects (whether they are the same in memory).

<br>

### List of Identity Operators

| **Operator** | **Description**                                                | **Example** |
| ------------ | -------------------------------------------------------------- | ----------- |
| is           | Returns True if both variables refer to the same object        | x is y      |
| is not       | Returns True if both variables do not refer to the same object | x is not y  |

<br>

### Examples

```python
x = [1, 2, 3]
y = x
z = [1, 2, 3]

print(x is y)     # True, same object
print(x is z)     # False, different objects
print(x is not z) # True
```

> [!success]- Code Output
> True  
> False  
> True

<br>

---

<br>

## Membership Operators

> [!info]
> Used to test for membership in sequences (e.g., strings, lists).

<br>

### List of Membership Operators

| **Operator** | **Description**                              | **Example**        |
| ------------ | -------------------------------------------- | ------------------ |
| in           | Returns True if value is in the sequence     | "a" in "apple"     |
| not in       | Returns True if value is not in the sequence | "x" not in "apple" |

<br>

### Examples

```python
fruits = ["apple", "banana", "cherry"]

print("apple" in fruits)      # True
print("orange" not in fruits) # True
```

> [!success]- Code Output
> True  
> True

<br>

---

<br>

## Assignment Operators

> [!info]
> Used to assign values to variables, with optional modifications.

<br>

### List of Assignment Operators

| **Operator** | **Description**         | **Example** | **Result** |
| :----------: | :---------------------- | :---------: | :--------: |
|      =       | Assign                  |    x = 5    |     5      |
|      +=      | Add and assign          |   x += 3    |     8      |
|      -=      | Subtract and assign     |   x -= 3    |     2      |
|     \*=      | Multiply and assign     |   x \*= 3   |     15     |
|      /=      | Divide and assign       |   x /= 3    |    1.67    |
|     //=      | Floor divide and assign |   x //= 3   |     1      |
|      %=      | Modulus and assign      |   x %= 3    |     2      |
|    \*\*=     | Exponent and assign     |  x \*\*= 3  |    125     |
|      &=      | Bitwise AND and assign  |   x &= 3    |     1      |
|     \|=      | Bitwise OR and assign   |   x \|= 3   |     7      |
|      ^=      | Bitwise XOR and assign  |   x ^= 3    |     6      |
|     <<=      | Left shift and assign   |   x <<= 3   |     40     |
|     >>=      | Right shift and assign  |   x >>= 3   |     0      |

<br>

### Examples

```python
x = 10
x += 5
print(x) # 15

x \*= 2
print(x) # 30
```

> [!success]- Code Output
> 15  
> 30
