![[booleans-banner.png]]

<br>

Booleans are a fundamental data type in Python, representing one of two values: `True` or `False`. They are often used in conditions, control flow, and logical operations.

<br>

---

<br>

## Basics of Booleans

In Python, Booleans are represented by the `bool` type and have only two possible values:

- `True`
- `False`

<br>

> [!warning]
> These values are case-sensitive, so `true` or `false` will result in a `NameError`.

<br>

### Example

```python
is_python = True
is_java = False

print(is_python)
print(is_java)
```

> [!success]- Code Output
> True  
> False

<br>

---

<br>

## Booleans in Expressions

Booleans often appear as the result of expressions involving:

- Comparison operators (`==`, `<`, `>`, etc.)
- Logical operators (`and`, `or`, `not`)

<br>

---

<br>

## Truthy and Falsy Values

Python considers some values to be "truthy" (equivalent to `True`) and others to be "falsy" (equivalent to `False`). These values are often used in conditions.

<br>

---

<br>

### Falsy Values

The following values evaluate to `False`:
- `None`
- `False`
- `0` (any numeric type, including `0.0`, `0j`)
- Empty sequences or collections: `''`, `[]`, `{}`, `set()`, `range(0)`

---

<br>

### Truthy Values

Any value that is **not falsy** is considered truthy.

<br>

### Example: Truthy and Falsy

```python
print(bool(None))       # False
print(bool(0))          # False
print(bool([]))         # False
print(bool(1))          # True
print(bool("Hello"))    # True
print(bool([1, 2, 3]))  # True
```

> [!success]- Code Output
> False  
> False  
> False  
> True  
> True  
> True

<br>

---

<br>

## Booleans and Built-in Functions

Python provides several functions that interact with Booleans or return Boolean values.

<br>

---

<br>

### bool()

> [!info]
> Converts a value to its Boolean equivalent.
>
> ```python
> print(bool(1))        # True
> print(bool(0))        # False
> print(bool("Hello"))  # True
> print(bool(""))       # False
> ```
>
> > [!success]- Code Output
> True  
> False  
> True  
> False

<br>

### any()

> [!info]
> Returns `True` if **any** element in the iterable is truthy.
>
> ```python
> values = [0, None, False, 1]
> print(any(values))
> ```
>
> > [!success]- Code Output
> True

<br>

### all()

> [!info]
> Returns `True` if **all** elements in the iterable are truthy.
>
> ```python
> values = [1, "Hello", True]
> print(all(values))
> ```
>
> > [!success]- Code Output
> True