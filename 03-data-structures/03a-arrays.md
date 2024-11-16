![[arrays-banner.png]]

<br>

Arrays in Python are a data structure used to store multiple items of the same data type in a contiguous memory location. While Python does not have a built-in array type like some other languages, it offers several ways to work with arrays using libraries like `array` (from the standard library) and third-party tools like NumPy.

<br>

---

<br>

## Basics of Arrays

Python’s `array` module provides the array type, which is used to create arrays of fixed type and size. Unlike lists, arrays from the `array` module store items of the same data type and are more memory-efficient.

<br>

### Creating an Array

> [!info]
> Use the `array` module to create arrays. Specify the type code for the data type, followed by an iterable of values.
>
> ```python
> from array import array
> 
> arr = array('i', [1, 2, 3, 4, 5])  # 'i' is the type code for integers
> print(arr)
> ```
> > [!success]- Code Output
> array('i', [1, 2, 3, 4, 5])

<br>

---

<br>

## Type Codes

Python’s `array` module uses type codes to define the type of elements stored in the array.

| **Type Code** | **C Type**        | **Python Type** | **Size (bytes)** |
|---------------|-------------------|-----------------|------------------|
| `'b'`         | signed char       | int             | 1                |
| `'B'`         | unsigned char     | int             | 1                |
| `'u'`         | wchar_t           | Unicode         | 2                |
| `'h'`         | signed short      | int             | 2                |
| `'H'`         | unsigned short    | int             | 2                |
| `'i'`         | signed int        | int             | 2                |
| `'I'`         | unsigned int      | int             | 2                |
| `'l'`         | signed long       | int             | 4                |
| `'L'`         | unsigned long     | int             | 4                |
| `'f'`         | float             | float           | 4                |
| `'d'`         | double            | float           | 8                |

<br>

> [!tip]
> Choose the type code based on the type of data and memory efficiency you need.

<br>

---

<br>

## Array Operations

Python arrays support several operations, such as indexing, slicing, and iteration.

<br>

---

<br>

### Indexing

> [!info]
> Access elements in an array using their index. Indexing starts at `0`.
>
> ```python
> arr = array('i', [10, 20, 30, 40, 50])
> 
> print(arr[0])  # First element
> print(arr[-1])  # Last element
> ```
> > [!success]- Code Output
> 10  
> 50

<br>

### Slicing

> [!info]
> Extract subarrays using slicing syntax `array[start:stop:step]`.
>
> ```python
> arr = array('i', [10, 20, 30, 40, 50])
> 
> print(arr[1:4])   # Elements from index 1 to 3
> print(arr[::-1])   # Reverse the array
> ```
> > [!success]- Code Output
> array('i', [20, 30, 40])  
> array('i', [50, 40, 30, 20, 10])

<br>

### Iteration

> [!info]
> Use a `for` loop to iterate over an array.
>
> ```python
> for elem in arr:
>     print(elem, end=" ")
> ```
> > [!success]- Code Output
> 10 20 30 40 50

<br>

---

<br>

## Methods for Arrays

The `array` module provides methods for common operations like adding, removing, and searching for elements.

<br>

---

<br>

### append(x)

> [!info]
> Adds an element `x` to the end of the array.
>
> ```python
> arr = array('i', [10, 20, 30])
> 
> arr.append(40)
> print(arr)
> ```
> > [!success]- Code Output
> array('i', [10, 20, 30, 40])

<br>

### extend(iterable)

> [!info]
> Extends the array by appending elements from the iterable.
>
> ```python
> arr = array('i', [10, 20])
> 
> arr.extend([30, 40, 50])
> print(arr)
> ```
> > [!success]- Code Output
> array('i', [10, 20, 30, 40, 50])

<br>

### insert(index, x)

> [!info]
> Inserts an element `x` at the specified `index`.
>
> ```python
> arr = array('i', [10, 20, 30])
> 
> arr.insert(1, 15)
> print(arr)
> ```
> > [!success]- Code Output
> array('i', [10, 15, 20, 30])

<br>

### remove(x)

> [!info]
> Removes the first occurrence of the value `x` from the array.
>
> ```python
> arr = array('i', [10, 20, 30])
> 
> arr.remove(20)
> print(arr)
> ```
> > [!success]- Code Output
> array('i', [10, 30])

<br>

### pop([index])

> [!info]
> Removes and returns the element at the specified `index`. If no index is provided, removes the last element.
>
> ```python
> arr = array('i', [10, 20, 30])
> 
> print(arr.pop(1))  # Remove element at index 1
> print(arr)
> ```
> > [!success]- Code Output
> 20  
> array('i', [10, 30])

<br>

### index(x)

> [!info]
> Returns the index of the first occurrence of the value `x`.
>
> ```python
> arr = array('i', [10, 20, 30])
> print(arr.index(20))
> ```
> > [!success]- Code Output
> 1

<br>

### reverse()

> [!info]
> Reverses the elements of the array in place.
>
> ```python
> arr = array('i', [10, 20, 30])
> 
> arr.reverse()
> print(arr)
> ```
> > [!success]- Code Output
> array('i', [30, 20, 10])

<br>

### count(x)

> [!info]
> Counts the occurrences of the value `x` in the array.
>
> ```python
> arr = array('i', [10, 20, 30, 20])
> print(arr.count(20))
> ```
> > [!success]- Code Output
> 2

<br>

---

<br>

## Comparison: Arrays vs Lists

> [!info]
> Python arrays and lists have overlapping features but differ in performance and use cases.
>
> | **Feature**        | **Array**                  | **List**                    |
> |---------------------|----------------------------|-----------------------------|
> | Data Type           | Homogeneous (single type) | Heterogeneous (mixed types) |
> | Memory Efficiency   | More efficient            | Less efficient              |
> | Operations          | Limited                   | Extensive                   |
> | Import Requirement  | Requires `array` module   | Built-in                    |

<br>

> [!tip]
> Use arrays when you need memory efficiency and lists when you need flexibility.

<br>

---

<br>

## NumPy for Advanced Arrays

For more complex operations and multidimensional arrays, consider using the third-party library NumPy. NumPy arrays (`ndarray`) provide a rich set of features for mathematical and matrix operations.

<br>

```bash
pip install numpy
```

```python
import numpy as np
arr = np.array([1, 2, 3, 4, 5])
print(arr)
```

> [!success]- Code Output
> [1 2 3 4 5]