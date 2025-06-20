# Python Basics Cheatsheet

## Variables and Data Types

```python
# Numbers
x = 5         # int
y = 3.14      # float
z = 1 + 2j    # complex

# Strings
name = "Python"
multi_line = """Multiple
line string"""

# Boolean
is_true = True
is_false = False

# Lists
my_list = [1, 2, 3]
mixed_list = [1, "hello", True]

# Tuples (immutable)
my_tuple = (1, 2, 3)

# Dictionaries
my_dict = {"key": "value", "number": 42}

# Sets
my_set = {1, 2, 3}
```

## Control Flow

### If Statements
```python
if condition:
    # code
elif another_condition:
    # code
else:
    # code
```

### Loops
```python
# For loop
for item in iterable:
    # code

# While loop
while condition:
    # code
```

## Functions

```python
def function_name(parameter1, parameter2="default"):
    """Docstring explaining the function"""
    # function body
    return result

# Lambda functions
square = lambda x: x**2
```

## Common Operations

### String Operations
```python
text = "Hello, World!"
length = len(text)
upper = text.upper()
lower = text.lower()
split_text = text.split(",")
```

### List Operations
```python
numbers = [1, 2, 3]
numbers.append(4)
numbers.extend([5, 6])
first = numbers[0]
last = numbers[-1]
sliced = numbers[1:3]
```

### Dictionary Operations
```python
dict = {"name": "Python"}
dict["version"] = 3.9
value = dict.get("name")
keys = dict.keys()
values = dict.values()
```

## Error Handling

```python
try:
    # code that might raise an exception
except ExceptionType:
    # handle the exception
else:
    # runs if no exception
finally:
    # always runs
```
