![[strings-banner.png]]

<br>

In Python, strings are a core data type for handling text, offering numerous built-in methods for manipulation, searching, formatting, and transformations.

<br>

---

<br>

## Basics of Strings

Strings in Python are sequences of characters enclosed within single (`'...'`), double (`"..."`), or triple quotes (`'''...'''` or `"""..."""`). They are immutable, meaning they cannot be changed after creation.

<br>

```python
example_str = "Hello, World!"

multiline_str = """This is
a multi-line
string."""

print(example_str)
print(multiline_str)
```

> [!success]- Code Output
> Hello, World!  
> This is  
> a multi-line  
> string.

<br>

---

<br>

### Escape Characters in Strings

Escape characters are used to represent characters in strings that would otherwise be difficult or impossible to include. They are preceded by a backslash (`\`) to signal their special meaning.

<br>

---

<br>

### Common Escape Characters

| **Escape Character** | **Description**            | **Example**                 | **Output**                    |
| :------------------: | -------------------------- | --------------------------- | ----------------------------- |
|         `\\`         | Backslash                  | `"This is a backslash: \\"` | `This is a backslash: \`      |
|         `\'`         | Single quote               | `"It\'s Python!"`           | `It's Python!`                |
|         `\"`         | Double quote               | `"She said, \"Hello!\""`    | `She said, "Hello!"`          |
|         `\n`         | New line                   | `"Hello\nWorld!"`           | `Hello`<br>`World!`           |
|         `\t`         | Tab                        | `"Hello\tWorld!"`           | `Hello    World!`             |
|         `\r`         | Carriage return            | `"Hello\rWorld!"`           | `World!`                      |
|         `\b`         | Backspace                  | `"Hello\bWorld!"`           | `HelloWorld!`                 |
|         `\f`         | Form feed                  | `"Hello\fWorld!"`           | `Hello`<form feed>`World!`    |
|         `\v`         | Vertical tab               | `"Hello\vWorld!"`           | `Hello`<vertical tab>`World!` |
|       `\uXXXX`       | Unicode character (16-bit) | `"\u2764"`                  | ❤️ (heart symbol)             |
|     `\UXXXXXXXX`     | Unicode character (32-bit) | `"\U0001F600"`              | 😀 (smiley face)              |
|        `\xXX`        | Hexadecimal character      | `"\x48\x65\x6C\x6C\x6F"`    | `Hello`                       |
|         `\0`         | Null character             | `"Hello\0World!"`           | `HelloWorld!`                 |

<br>

### Examples of Escape Characters

> [!info]
> Escape characters help include special characters in strings or format strings in specific ways.

<br>

```python
# Including quotes
print('It\'s Python!')
print("She said, \"Hello!\"")

# New lines and tabs
print("Line1\nLine2")
print("Column1\tColumn2")

# Unicode and hexadecimal characters
print("\u2764")                # Heart symbol
print("\U0001F600")            # Smiley face
print("\x48\x65\x6C\x6C\x6F")  # Hexadecimal for "Hello"
```

> [!success]- Code Output
> It's Python!  
> She said, "Hello!"  
> Line1  
> Line2  
> Column1 Column2  
> ❤️  
> 😀  
> Hello

<br>

---

<br>

### Raw Strings

> [!info]
> Sometimes, escape sequences should be treated as literal text. Use raw strings by prefixing the string with an `r`.
>
> In raw strings, backslashes are treated as literal characters, and escape sequences are not processed.

<br>

```python
# Without raw string
print("C:\\Users\\Name\\Documents")

# Using raw string
print(r"C:\Users\Name\Documents")
```

> [!success]- Code Output
> C:\Users\Name\Documents  
> C:\Users\Name\Documents

<br>

---

<br>

## String Slicing and Reversing

Python strings are sequences, which means you can access individual characters and subsequences using slicing. This makes operations like extracting parts of a string, skipping characters, or reversing straightforward.

<br>

---

<br>

### Accessing Characters by Index

> [!info]
> Strings support zero-based indexing to access individual characters. Use negative indices to count from the end of the string.
>
> ```python
> text = "Python"
>
> print(text[0])  # First character
> print(text[-1])  # Last character
> ```
>
> > [!success]- Code Output
> > P  
> > n

<br>

### Slicing a String

> [!info]
> Slicing allows you to extract a substring by specifying a start, stop, and optional step in the format `string[start:stop:step]`. The slice includes the start index but excludes the stop index.
>
> ```python
> text = "Python"
>
> print(text[0:3])  # First three characters
> print(text[2:])    # From index 2 to the end
> print(text[:4])    # From the start to index 4 (exclusive)
> print(text[::2])   # Every second character
> ```
>
> > [!success]- Code Output
> > Pyt  
> > thon  
> > Pyth  
> > Pto

<br>

### Negative Index Slicing

> [!info]
> Negative indices allow you to slice relative to the end of the string. For example, `-1` is the last character, `-2` is the second-to-last, and so on.
>
> ```python
> text = "Python"
>
> print(text[-3:])   # Last three characters
> print(text[:-3])   # All except the last three characters
> ```
>
> > [!success]- Code Output
> > hon  
> > Pyt

<br>

### Reversing a String

> [!info]
> To reverse a string, use slicing with a step of `-1`.
>
> ```python
> text = "Python"
> print(text[::-1])
> ```
>
> > [!success]- Code Output
> > nohtyP

<br>

### Skipping Characters in Slices

> [!info]
> The step parameter in slicing lets you skip characters. For example, a step of `2` selects every second character.
>
> ```python
> text = "Python"
>
> print(text[::2])   # Every second character
> print(text[1::2])  # Every second character starting at index 1
> ```
>
> > [!success]- Code Output
> > Pto  
> > yhn

<br>

### Modifying a String Using Slicing

> [!warning]
> Strings in Python are immutable, so you cannot modify them directly. Instead, create a new string by combining slices or using other string operations.
>
> ```python
> text = "Python"
>
> modified_text = text[:3] + "x" + text[4:]
> print(modified_text)
> ```
>
> > [!success]- Code Output
> > Pyxhon

<br>

---

<br>

## Common String Methods

Python’s `str` type provides various methods that simplify text processing, search, and formatting.

<br>

---

<br>

### upper()

> [!info]
> Converts all characters in the string to uppercase.
>
> ```python
> text = "hello"
> print(text.upper())
> ```
>
> > [!success]- Code Output
> > HELLO

<br>

### lower()

> [!info]
> Converts all characters in the string to lowercase.
>
> ```python
> text = "HELLO"
> print(text.lower())
> ```
>
> > [!success]- Code Output
> > hello

<br>

### capitalize()

> [!info]
> Capitalizes the first character of the string, making the rest lowercase.
>
> ```python
> text = "hello world"
> print(text.capitalize())
> ```
>
> > [!success]- Code Output
> > Hello world

<br>

### title()

> [!info]
> Capitalizes the first character of each word in the string.
>
> ```python
> text = "hello world"
> print(text.title())
> ```
>
> > [!success]- Code Output
> > Hello World

<br>

### swapcase()

> [!info]
> Swaps uppercase characters to lowercase and vice versa.
>
> ```python
> text = "Hello World"
> print(text.swapcase())
> ```
>
> > [!success]- Code Output
> > hELLO wORLD

<br>

---

<br>

## String Search Methods

Python strings provide methods to search for substrings, find their positions, and verify content.

<br>

---

<br>

### find(sub[, start[, end]])

> [!info]
> Returns the lowest index of the substring `sub` within the string. Returns `-1` if not found.
>
> ```python
> text = "Hello, World!"
> print(text.find("World"))
> ```
>
> > [!success]- Code Output
> > 7

<br>

### index(sub[, start[, end]])

> [!info]
> Returns the lowest index of the substring `sub`. Raises `ValueError` if not found.
>
> ```python
> text = "Hello, World!"
> print(text.index("World"))
> ```
>
> > [!success]- Code Output
> > 7

<br>

### rfind(sub[, start[, end]])

> [!info]
> Returns the highest index of the substring `sub`. Returns `-1` if not found.
>
> ```python
> text = "Hello, World!"
> print(text.rfind("o"))
> ```
>
> > [!success]- Code Output
> > 8

<br>

### rindex(sub[, start[, end]])

> [!info]
> Returns the highest index of the substring `sub`. Raises `ValueError` if not found.
>
> ```python
> text = "Hello, World!"
> print(text.rindex("o"))
> ```
>
> > [!success]- Code Output
> > 8

<br>

### count(sub[, start[, end]])

> [!info]
> Counts occurrences of substring `sub` within the string.
>
> ```python
> text = "Hello, World!"
> print(text.count("o"))
> ```
>
> > [!success]- Code Output
> > 2

<br>

---

<br>

## String Validation Methods

These methods check if a string meets certain conditions, such as being alphabetical or numeric.

<br>

---

<br>

### isalpha()

> [!info]
> Returns `True` if all characters in the string are alphabetic.
>
> ```python
> text = "Hello"
> print(text.isalpha())
> ```
>
> > [!success]- Code Output
> > True

<br>

### isdigit()

> [!info]
> Returns `True` if all characters in the string are digits.
>
> ```python
> text = "12345"
> print(text.isdigit())
> ```
>
> > [!success]- Code Output
> > True

<br>

### isalnum()

> [!info]
> Returns `True` if all characters in the string are alphanumeric.
>
> ```python
> text = "Hello123"
> print(text.isalnum())
> ```
>
> > [!success]- Code Output
> > True

<br>

### isspace()

> [!info]
> Returns `True` if the string contains only whitespace characters.
>
> ```python
> text = "   "
> print(text.isspace())
> ```
>
> > [!success]- Code Output
> > True

<br>

### istitle()

> [!info]
> Returns `True` if the string is in title case.
>
> ```python
> text = "Hello World"
> print(text.istitle())
> ```
>
> > [!success]- Code Output
> > True

<br>

### islower()

> [!info]
> Returns `True` if all characters in the string are lowercase.
>
> ```python
> text = "hello"
> print(text.islower())
> ```
>
> > [!success]- Code Output
> > True

<br>

### isupper()

> [!info]
> Returns `True` if all characters in the string are uppercase.
>
> ```python
> text = "HELLO"
> print(text.isupper())
> ```
>
> > [!success]- Code Output
> > True

<br>

---

<br>

## String Modification Methods

These methods allow transformations of string content, such as replacing, removing whitespace, or joining elements.

<br>

---

<br>

### replace(old, new[, count])

> [!info]
> Replaces occurrences of `old` with `new`. Optionally limits replacements to `count`.
>
> ```python
> text = "Hello, World!"
> print(text.replace("World", "Python"))
> ```
>
> > [!success]- Code Output
> > Hello, Python!

<br>

### strip([chars])

> [!info]
> Removes leading and trailing characters specified in `chars` (defaults to whitespace).
>
> ```python
> text = "  Hello, World!  "
> print(text.strip())
> ```
>
> > [!success]- Code Output
> > Hello, World!

<br>

### lstrip([chars])

> [!info]
> Removes leading characters specified in `chars`.
>
> ```python
> text = "  Hello, World!"
> print(text.lstrip())
> ```
>
> > [!success]- Code Output
> > Hello, World!

<br>

### rstrip([chars])

> [!info]
> Removes trailing characters specified in `chars`.
>
> ```python
> text = "Hello, World!  "
> print(text.rstrip())
> ```
>
> > [!success]- Code Output
> > Hello, World!

<br>

---

<br>

## String Formatting Methods

Python offers several ways to format strings, including f-strings, `format()`, and methods for alignment.

<br>

---

<br>

### format(\*args, \*\*kwargs)

> [!info]
> Formats the string using placeholders (`{}`) with positional or keyword arguments.
>
> ```python
> text = "Hello, {}!"
> print(text.format("Python"))
> ```
>
> > [!success]- Code Output
> > Hello, Python!

<br>

### f-strings (formatted string literals)

> [!info]
> Embeds expressions inside string literals using `{}`.
>
> ```python
> name = "Python"
> print(f"Hello, {name}!")
> ```
>
> > [!success]- Code Output
> > Hello, Python!

<br>

### fr-strings (formatted raw string literals)

> [!info]
> Formatted raw strings (`rf`) are powerful for scenarios like working with Windows file paths or regex patterns that need dynamic variable interpolation. They combine the best of both raw and formatted strings.
>
> `rf` or `fr` can be used interchangeably; the behavior is the same.
>
> ```python
> user_name = "Adam"
> path = rf"C:\{user_name}\Documents"
> print(path)
> ```
>
> > [!success]- Code Output
> > C:\Adam\Documents

<br>

---

<br>

## String Joining and Splitting

These methods are used to join multiple strings or split strings into lists.

<br>

---

<br>

### join(iterable)

> [!info]
> Concatenates a sequence of strings with the specified separator.
>
> ```python
> words = ["Hello", "World"]
> print(" ".join(words))
> ```
>
> > [!success]- Code Output
> > Hello World

<br>

### split([sep[, maxsplit]])

> [!info]
> Splits the string at each occurrence of `sep` (defaults to whitespace). Returns a list of substrings.
>
> ```python
> text = "Hello World"
> print(text.split())
>
> # Assign split values to variables
> first, second = text.split()
> print(first, second)
> ```
>
> > [!success]- Code Output
> > ['Hello', 'World']
> > Hello World

<br>

### partition(sep)

> [!info]
> Splits the string into a tuple of three parts: part before `sep`, `sep` itself, and part after `sep`.
>
> ```python
> text = "Hello, World!"
> print(text.partition(","))
> ```
>
> > [!success]- Code Output
> > ('Hello', ',', ' World!')

<br>

### rpartition(sep)

> [!info]
> Splits the string at the last occurrence of `sep`.
>
> ```python
> text = "Hello, World!"
> print(text.rpartition(","))
> ```
>
> > [!success]- Code Output
> > ('Hello', ',', ' World!')
