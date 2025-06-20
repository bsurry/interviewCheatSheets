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

# List manipulation
# Lists ARE mutable

# Adding elements

# add one item to end
my_list.append(4)           # [1, 2, 3, 4]

# add an iterable to the end of this list. Unlike list.append(), which adds an entire iterable as a single element, extend() iterates through the provided iterable and adds each of its elements as separate items to the list.

my_list.extend([5, 6])      # [1, 2, 3, 4, 5, 6]

# insert an element at the index list.insert(index, element)
my_list.insert(1, 10)       # [1, 10, 2, 3, 4, 5, 6]

# Removing elements
my_list.remove(10)          # [1, 2, 3, 4, 5, 6] Removes first occurrence of 10 (mo return)
last = my_list.pop()        # [1, 2, 3, 4, 5] Removes and returns last element
my_list.clear()             # Removes all elements

# Accessing elements
first = mixed_list[0]       # 1
last = mixed_list[-1]       # True (last item in the list - -2 would return "hello" for example)
slice = mixed_list[1:3]     # ['hello', True], format is list_name[start:stop:step] (-1 step can be used to reverse)

# Searching and counting
index = mixed_list.index("hello")  # 1
count = mixed_list.count(1)         # 1

# Sorting and reversing
numbers = [3, 1, 2]
numbers.sort()               # [1, 2, 3]
numbers.reverse()            # [3, 2, 1]

# Copying
copy_list = numbers.copy()

# List comprehensions
squares = [x**2 for x in range(5)]  # [0, 1, 4, 9, 16]

# Tuples (immutable)
my_tuple = (1, 2, 3)

# Dictionaries
my_dict = {"key": "value", "number": 42}

# Sets
my_set = {1, 2, 3}

#In Python, a set is an unordered collection of unique elements. Sets are useful for storing items without duplicates and for performing mathematical set operations like union, intersection, and difference.

# Sets are:
# Unordered: The elements have no specific order.
# Unique: No duplicate elements allowed.
# Mutable: You can add or remove elements.

# Sets are often used to test membership, remove duplicates from a list, or perform set algebra.
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
