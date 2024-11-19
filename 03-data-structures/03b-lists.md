![[lists-banner.png]]

<br>

Python’s **list** is a versatile, mutable, and general-purpose data structure that can hold heterogeneous elements. It allows dynamic resizing and provides a wide variety of methods for manipulation, making it one of the most commonly used data types in Python.

<br>

---

<br>

## Basics of Lists

A **list** in Python is created using square brackets `[]` or the `list()` constructor. Lists can store elements of any type, including other lists.

<br>

### Creating Lists

> [!info]
> Lists can be created using literals or the `list()` function.
>
> ```python
> empty_list = []                    # Empty list
> numbers = [1, 2, 3, 4, 5]      # List of integers
> mixed = [1, "Python", 3.14]  # List of mixed types
> nested = [[1, 2], [3, 4]]        # Nested list
> 
> print(numbers, mixed, nested)
> ```
> > [!success]- Code Output
> [1, 2, 3, 4, 5] [1, 'Python', 3.14] [\[1, 2], [3, 4]]

<br>

---

<br>

## Operations on Lists

Lists support a wide range of operations, including indexing, slicing, and iteration.

<br>

---

<br>

### Indexing

> [!info]
> Access elements in a list using zero-based indexing. Negative indices access elements from the end.
>
> ```python
> lst = [10, 20, 30, 40, 50]
> 
> print(lst[0])   # First element
> print(lst[-1])  # Last element
> ```
> > [!success]- Code Output
> 10  
> 50

<br>

### Slicing

> [!info]
> Extract a subsequence of the list using slicing syntax: `list[start:stop:step]`.
>
> ```python
> lst = [10, 20, 30, 40, 50]
> 
> print(lst[1:4])   # Elements from index 1 to 3
> print(lst[::-1])  # Reverse the list
> ```
> > [!success]- Code Output
> [20, 30, 40]  
> [50, 40, 30, 20, 10]

<br>

### Iteration

> [!info]
> Use a `for` loop to iterate over the elements of a list.
>
> ```python
> lst = [10, 20, 30]
> 
> for elem in lst:
>     print(elem, end=" ")
> ```
> > [!success]- Code Output
> 10 20 30

<br>

### Membership Testing

> [!info]
> Use the `in` and `not in` operators to test for membership in a list.
>
> ```python
> lst = [10, 20, 30]
> 
> print(20 in lst)         # Check if 20 is in the list
> print(40 not in lst)  # Check if 40 is not in the list
> ```
> > [!success]- Code Output
> True  
> True

<br>

---

<br>

## Common Methods for Lists

The `list` type in Python includes several methods for modifying, searching, and analyzing lists.

<br>

---

<br>

### append(x)

> [!info]
> Adds an element `x` to the end of the list.
>
> ```python
> lst = [1, 2, 3]
> lst.append(4)
> print(lst)
> ```
> > [!success]- Code Output
> [1, 2, 3, 4]

<br>

### extend(iterable)

> [!info]
> Extends the list by appending elements from the iterable.
>
> ```python
> lst = [1, 2, 3]
> lst.extend([4, 5, 6])
> print(lst)
> ```
> > [!success]- Code Output
> [1, 2, 3, 4, 5, 6]

<br>

### insert(index, x)

> [!info]
> Inserts an element `x` at the specified `index`.
>
> ```python
> lst = [10, 20, 30]
> lst.insert(1, 15)
> print(lst)
> ```
> > [!success]- Code Output
> [10, 15, 20, 30]

<br>

### remove(x)

> [!info]
> Removes the first occurrence of the value `x`. Raises a `ValueError` if `x` is not in the list.
>
> ```python
> lst = [10, 20, 30]
> lst.remove(20)
> print(lst)
> ```
> > [!success]- Code Output
> [10, 30]

<br>

### pop([index])

> [!info]
> Removes and returns the element at the specified `index`. If no index is provided, removes the last element.
>
> ```python
> lst = [10, 20, 30]
> print(lst.pop())  # Remove last element
> print(lst.pop(0)) # Remove first element
> print(lst)
> ```
> > [!success]- Code Output
> 30  
> 10  
> [20]

<br>

### index(x[, start[, end]])

> [!info]
> Returns the first index of the value `x`. Raises a `ValueError` if `x` is not in the list.
>
> ```python
> lst = [10, 20, 30, 20]
> print(lst.index(20))
> ```
> > [!success]- Code Output
> 1

<br>

### count(x)

> [!info]
> Returns the number of occurrences of the value `x` in the list.
>
> ```python
> lst = [10, 20, 20, 30]
> print(lst.count(20))
> ```
> > [!success]- Code Output
> 2

<br>

### reverse()

> [!info]
> Reverses the elements of the list in place.
>
> ```python
> lst = [1, 2, 3]
> lst.reverse()
> print(lst)
> ```
> > [!success]- Code Output
> [3, 2, 1]

<br>

### sort(key=None, reverse=False)

> [!info]
> Sorts the list in place. By default, it sorts in ascending order. Use `reverse=True` for descending order.
>
> ```python
> lst = [3, 1, 2]
> lst.sort()
> print(lst)
> lst.sort(reverse=True)
> print(lst)
> ```
> > [!success]- Code Output
> [1, 2, 3]  
> [3, 2, 1]

<br>

---

<br>

## Other Useful Features

<br>

---

<br>

### List Comprehensions

> [!info]
> Create new lists by applying an expression to each element in an iterable.
>
> ```python
> squares = [x**2 for x in range(5)]
> print(squares)
> ```
> > [!success]- Code Output
> [0, 1, 4, 9, 16]

<br>

### Nested Lists

> [!info]
> Lists can contain other lists, enabling multidimensional data structures.
>
> ```python
> matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
> print(matrix[1][2])  # Access element in row 1, column 2
> ```
> > [!success]- Code Output
> 6

<br>

---

<br>

## Lists vs Arrays

> [!info]
> Lists are more flexible but less memory-efficient than arrays. Use lists for general-purpose programming and heterogeneous data, and use arrays (or NumPy) for numerical computations.