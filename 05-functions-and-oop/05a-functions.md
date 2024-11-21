![[functions-banner.png]]

<br>

Functions are reusable blocks of code that perform a specific task. They help improve code modularity, readability, and maintainability. Python provides a variety of ways to define and use functions, including support for anonymous functions, closures, and higher-order functions.

<br>

---

<br>

## Basics of Functions

Functions are defined using the `def` keyword, followed by the function name, parentheses `()`, and a colon `:`. The function body contains the logic to be executed.

<br>

### **Defining a Function**

> [!info]
> Define a function using the `def` keyword. You can optionally use the `return` statement to return the result to the caller of the function. Using the `return` keyword ends the execution of the function, and does not print to the console unless `print()` is used. If no return values are given, the function will return `None`.
>
> ```python
> def greet(name):
>     return f"Hello, {name}!"
>
> greet("World")              # Does not print
> print(greet("Python"))  # Does print
> ```
> > [!success]- Code Output
> Hello, Python!

<br>

---

<br>

## **Function Parameters**

Functions can accept parameters to customize their behavior. Python supports various types of parameters.

<br>

---

<br>

### Positional Parameters

> [!info]
> Positional parameters are the most basic type. The order of arguments passed to the function must match the order of parameters in the definition.
>
> ```python
> def add(a, b):
>     return a + b
>
> print(add(2, 3))
> ```
> > [!success]- Code Output
> 5

<br>

### Default Parameters

> [!info]
> Default parameters allow you to specify a default value for a parameter if no value is provided.
>
> ```python
> def greet(name="World"):
>     return f"Hello, {name}!"
>
> print(greet())               # Uses default value
> print(greet("Planet"))  # Overrides default value
> ```
> > [!success]- Code Output
> Hello, World!  
> Hello, Planet!

<br>

### Keyword Arguments

> [!info]
> Pass arguments to a function using their parameter names. This allows flexibility in the order of arguments.
>
> ```python
> def describe(name, age):
>     return f"{name} is {age} years old."
>
> print(describe(age=25, name="Adam"))
> ```
> > [!success]- Code Output
> Adam is 25 years old.

<br>

### Arbitrary Arguments (`*args`)

> [!info]
> Use `*args` to pass a variable number of positional arguments to a function.
>
> ```python
> def multiply(*args):
>     result = 1
>     for num in args:
>         result *= num
>     return result
>
> print(multiply(2, 3, 4))
> ```
> > [!success]- Code Output
> 24

<br>

### Arbitrary Keyword Arguments (`**kwargs`)

> [!info]
> Use `**kwargs` to pass a variable number of keyword arguments to a function.
>
> ```python
> def display_info(**kwargs):
>     for key, value in kwargs.items():
>         print(f"{key}: {value}")
>
> display_info(name="Adam", age=25, profession="Engineer")
> ```
> > [!success]- Code Output
> name: Adam  
> age: 25  
> profession: Engineer

<br>

---

<br>

## Scope and Lifetime of Variables

Python functions have their own scope, which determines the accessibility of variables.

<br>

---

<br>

### Local Variables

> [!info]
> Variables declared inside a function are local and cannot be accessed outside the function.
>
> ```python
> def example():
>     x = 10
>     print(x)
>
> example()
> ```
> > [!success]- Code Output
> 10

<br>

### Global Variables

> [!info]
> Variables declared outside a function are global and accessible inside the function unless shadowed by a local variable.
>
> ```python
> x = 10
>
> def example():
>     print(x)
>
> example()
> ```
> > [!success]- Code Output
> 10

<br>

### The `global` Keyword

> [!info]
> Use the `global` keyword to modify a global variable inside a function.
>
> ```python
> x = 10
>
> def modify():
>     global x
>     x = 20
>
> modify()
> print(x)
> ```
> > [!success]- Code Output
> 20

<br>

---

<br>

## Advanced Function Features

<br>

---

<br>

### Lambda Functions

> [!info]
> Lambda functions are anonymous functions defined using the `lambda` keyword. They are typically used for short, throwaway functions.
>
> ```python
> square = lambda x: x ** 2
> print(square(5))
> ```
> > [!success]- Code Output
> 25

<br>

### Higher-Order Functions

> [!info]
> Functions that take other functions as arguments or return them as results are called higher-order functions.
>
> ```python
> def apply(func, value):
>     return func(value)
>
> print(apply(lambda x: x ** 2, 5))
> ```
> > [!success]- Code Output
> 25

<br>

### Closures

> [!info]
> A closure is a function that retains access to variables from its enclosing scope, even after the outer function has finished execution.
>
> ```python
> def make_multiplier(n):
>     def multiplier(x):
>         return x * n
>     return multiplier
>
> double = make_multiplier(2)
> print(double(5))
> ```
> > [!success]- Code Output
> 10

<br>

### Decorators

> [!info]
> Decorators are functions that modify the behavior of other functions. They are often used for logging, authentication, etc.
>
> ```python
> def decorator(func):
>     def wrapper(*args, **kwargs):
>         print("Before the function call")
>         result = func(*args, **kwargs)
>         print("After the function call")
>         return result
>     return wrapper
>
> @decorator
> def say_hello():
>     print("Hello!")
>
> say_hello()
> ```
> > [!success]- Code Output
> Before the function call  
> Hello!  
> After the function call

<br>

---

<br>

## Type Hints in Functions

Python supports type hints to specify the expected data types of function arguments and return values.

<br>

---

<br>

### Adding Type Hints

> [!info]
> Use type annotations to add type hints to your functions.
>
> ```python
> def greet(name: str) -> str:
>     return f"Hello, {name}!"
>
> print(greet("World"))
> ```
> > [!success]- Code Output
> Hello, World!

<br>

---

<br>

## Built-in Functions

Python provides several built-in functions that operate on or alongside user-defined functions.

<br>

---

<br>

### map()

> [!info]
> Applies a function to all items in an iterable.
>
> ```python
> nums = [1, 2, 3]
> squares = map(lambda x: x ** 2, nums)
> print(list(squares))
> ```
> > [!success]- Code Output
> [1, 4, 9]

<br>

### filter()

> [!info]
> Filters items in an iterable based on a condition.
>
> ```python
> nums = [1, 2, 3, 4]
> evens = filter(lambda x: x % 2 == 0, nums)
> print(list(evens))
> ```
> > [!success]- Code Output
> [2, 4]

<br>

### reduce()

> [!info]
> Performs a cumulative operation on items in an iterable. Requires the `functools` module.
>
> ```python
> from functools import reduce
>
> nums = [1, 2, 3, 4]
> product = reduce(lambda x, y: x * y, nums)
> print(product)
> ```
> > [!success]- Code Output
> 24