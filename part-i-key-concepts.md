# Part I Key Concepts

<table><tr><th>Name</th><th>Syntax</th><th>Example</th><th>Description</th></tr>
  <tr><td>String</td><td><code>str(), ""</code><td><code>"Hello world!"</code></td><td>Sequence of characters</td></tr>
  <tr><td>List</td><td><code>list(), []</code><td><code>["apple", "banana", "pear"], [1, 3, 5, 7]</code></td><td>Sequence of objects/values</td></tr>
  <tr><td>Dictionary</td><td><code>dict(), {}</code><td><code>{'first_name': 'Knute', 'last_name':'Rockne', 'class':'1918'}</code></td><td>Key-value pairs</td></tr>
  <tr><td>Set</td><td><code>set(), {}</code><td><code>{"apple", "banana", "pear"}, {1, 3, 5, 7}</code></td><td>Unordered group of unique values</td></tr> 
  <tr><td>Tuple</td><td><code>tuple(), ()</code><td><code>("apple", "banana", "pear"), (1, 3, 5, 7)</code></td><td>Ordered group of values that can include duplicates</td></tr>
  </table>
  
String methods:
- `.count()` (returns number of times specific value appears in a string)
- `.startswith()` (returns Boolean True/False value if string begins with specific value
- `.endswith()` (returns Boolean True/False value if string ends with specific value)
- `.find()` (returns index for specific value in string, searching left-to-right)
- `.rfind()` (returns index for specific value in string, searching right-to-left)
- `.index()` (returns index for specific value in string)
- `.rfind()` (returns index for specific value in string, searching right-to-left)


List methods:
- Creating a list: `[]` or `list()`
- Checking length of list: `len()`
- Accessing values using index: `fruits[0]`, `fruits.index("cherry")`
- Testing for membership: `in` or `not in`
- Modifying an existing list value: `fruits[1] = "new value"`
- Appending a value to a list: `numbers.append(13)`
- Inserting a value in a specific position: `numbers.insert(4, 11)`
- Extending a list (to include additional values): `numbers.extend(num2)`
- Removing values from a list: `numbers.remove(19)`, `numbers.pop(-1)`, `del numbers[7]`
- Slicing a list: `dorms[0:3]`
- Searching for values: `.count()`, `.index()`
- Sorting: `.sort()`, `.sorted()`, `.reverse()`
- Summary statistics: `.max()`, `.min()`, `.sum()`

## Arrays
- "An array is a data structure consisting of a collection of elements (values or variables), each identified by at least one array index or key. Depending on the language, array types may overlap (or be identified with) other data types that describe aggregates of values, such as lists and strings. Array types are often implemented by array data structures, but sometimes by other means, such as hash tables, linked lists, or search trees" (Busbee and Braunschweig, "[Arrays and Lists](https://press.rebus.community/programmingfundamentals/chapter/arrays-and-lists/)")
-  "In Python, the built-in array data structure is a list" (Busbee and Braunschweig, "[Arrays and Lists](https://press.rebus.community/programmingfundamentals/chapter/arrays-and-lists/)")

For more on array structures:
- Kenneth Leroy Busbee and Dave Braunschweig, "[Arrays and Lists](https://press.rebus.community/programmingfundamentals/chapter/arrays-and-lists/)" in *Programming Fundamentals*

## Dictionaries
- Python stores associate arrays using the **dictionary** data structure. Python dictionaries consist of key-value pairs, where the key is working as an identifier or index. To put that another way, a dictionary is a mapping between a set of indeces (keys) and a set of values. Each key maps to a value, and the association of a key and a value is called a **key-value pair**.
- For more on dictionaries in Python: [W3Schools, Python Dictionaries](https://www.w3schools.com/python/python_dictionaries.asp)

## Index, Indexing
- In Python, **indexing** allows us to refer to individual values in specific data structures using their position. NOTE: Python (and many other programming languages) are **zero-indexed**, which means counting for index positions begins at `0`.

```Python
# list of string objects
fruits = ["apple", "banana", "blueberry", "cherry"]

# access first value 
fruits[0]

# access second value
fruits[1]

# access third value
fruits[2]
```

Python lists also support negative indexing- we can use negative index values to count right-to-left. 
- NOTE: Negative indexing starts counting at `-1`

```Python
# access last value
fruits[-1]

# access next to last value
fruits[-2]
```

We can also use the `.index()` method to output the position for specific values (if they are present in the structure).

```Python
# return index for cherry
print("The index for cherry is ", fruits.index("cherry"))

# return index for pear
print("The index for pear is ", fruits.index("pear"))
```

## Iteration
- "In iteration control structures, a statement or block is executed until the program reaches a certain state, or operations have been applied to every element of a collection" (Busbee and Braunschweig, "[Iteration Control Structures](https://press.rebus.community/programmingfundamentals/chapter/iteration-control-structures/)")

When we're thinking about the types of data structures covered in this lab, when a Python program iterates over a data structure, it starts at the first item (index position `0`) and goes through each item (left to right) until it reaches the last value. 

Sample `for` loop that illustrates iteration:

```Python
# list of numbers
numbers = [1, 3, 5, 7, 9, 11, 13, 15, 17]

# sample for loop that iterates over items in list and outputs each number
for number in numbers:
 print(number)
```

## Lists
- "An array is a data structure consisting of a collection of elements (values or variables), each identified by at least one array index or key...In Python, the built-in array data structure is a list" (Busbee and Braunschweig, "[Arrays and Lists](https://press.rebus.community/programmingfundamentals/chapter/arrays-and-lists/)")
- An list is a single-dimension array

In Python, we can create lists using square brackets `[]` or the `list()` function.

Python examples:
```Python
# creating a list of numbers using square brackets
numbers = [1, 3, 5, 7, 9]

# checking data type
type(numbers)
```

```Python
# creating a list of strings using the list function
words = list(("apple", "banana", "blueberry", "cherry")) # note the double round bracket syntax

# check data type
type(words)
```

A few other preliminary notes on lists in Python:
- We can check the number of elements in a list using `len()` 
- We can access specific elements in a list using an index operator (`[]`) and position (numeric value)
- We can add values to a list using the `.append()`, `.insert()`, and `.extend()` methods
- We can isolate elements in a list using `.pop()`
- We can remove elements from a list using `.remove()` or `del`
- We can test for membership using the `in` operator
- We can sort elements in a list using `.sort()`, `sorted()`, and `.reverse()`
- We can access descriptive statistics for list values using `sum()`, `max()`, and `min()`

More on arrays/lists (general):
- Kenneth Leroy Busbee and Dave Braunschweig, "[Arrays and Lists](https://press.rebus.community/programmingfundamentals/chapter/arrays-and-lists/)" in *Programming Fundamentals*

More on lists in Python:
- [W3Schools, Python Lists](https://www.w3schools.com/python/python_lists.asp)

## Membership Operators
- "Membership operators are used to test if a sequence is presented in an object" (W3Schools, [Python Membership Operators](https://www.w3schools.com/python/gloss_python_membership_operators.asp))

The `in` and `not in` operators return Boolean `True` or `False` values.

```Python
# create list
fruits = ["apple", "banana", "peach"]

# test if apple is in list
"apple" in fruits # returns true

# test if blueberry is NOT in list
"blueberry" not in fruits # returns false
```

## Nested Lists, Sublists
- Lists in Python can also contain other lists- this is referred to as nested lists or sub-lists. Syntax for selecting items or values within a nested list: `list_name[list_item_number][sublist_item_number]`

```Python
# create list with two sub-lists
points = [[0, 1], [2, 3]]

# show list
points

# access first item on list, which is a sublist
points[0]

# access first item WITHIN second item on list
points[1][0]
```

## Sets
- A set is an unordered collection of unique objects. Sets are primarily used to see if an object or value is in the collection (membership). Python supports a number of set operations, but one of the primary uses is to test for membership.
- For more on sets in Python: [W3Schools, Python Sets](https://www.w3schools.com/python/python_sets.asp)

## Strings
- "A string data type is traditionally a sequence of characters, either as a literal constant or as some kind of variable...A string is generally considered a data type and is often implemented as an array data structure of bytes (or words) that stores a sequence of elements, typically characters, using some character encoding" (Busbee and Braunschweig, "[String Data Type](https://press.rebus.community/programmingfundamentals/chapter/string-data-type/)")
- "Like many other popular programming languages, strings in Python are arrays of bytes representing unicode characters. However, Python does not have a character data type, a single character is simply a string with a length of 1. Square brackets can be used to access elements of the string" ([W3Schools, Python Strings](https://www.w3schools.com/python/python_strings.asp))

Python examples:
```Python
# creating a string variable
x = "Hello World!"

# checking data type
type(x)
```

More on strings (general):
- Kenneth Leroy Busbee and Dave Braunschweig, "[String Data Type](https://press.rebus.community/programmingfundamentals/chapter/string-data-type/)" in *Programming Fundamentals*

More on strings in Python:
- [W3Schools, Python Strings](https://www.w3schools.com/python/python_strings.asp)

## Tuples
- "Tuples are used to store multiple items in a single variable...A tuple is a collection which is ordered and unchangeable. Tuples are written with round brackets...and allow duplicate values" ([W3Schools, Python Tuples](https://www.w3schools.com/python/python_tuples.asp))

We can create a tuple in Python using the round bracket syntax `(())` or the `tuple()` method.

```Python
# creating a tuple using round brackets
sample = ("apple", "banana", "blueberry")

# checking data type
type(sample)
```

```Python
# creating tuple using tuple method
sample = tuple(("apple", "banana", "blueberry"))

# check data type
type(sample)
```

Additional resources:
- [W3Schools, Python Tuples](https://www.w3schools.com/python/python_tuples.asp)
