# Python Next Steps Part I: Secondary Data Structures

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>This tutorial was written by Katherine Walden and is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

# Table of Contents
- [Key Concepts](#key-concepts)
- [Overview](#overview)
  * [Linear Arrays](#linear-arrays)
  * [Indexing in Python](#indexing-in-python)
  * [Associative Arrays](#associative-arrays)
- [Data Structures in Python](#data-structures-in-python)
  * [Strings](#strings)
  * [Lists](#lists)
  * [Dictionaries](#dictionaries)
  * [Tuples](#tuples)
  * [Sets](#sets)
- [Putting It All Together](#putting-it-all-together)
- [Additional Resources](#additional-resources)
- [Lab Notebook Questions (for this section)](#lab-notebook-questions-for-this-section)

[Click here](https://colab.research.google.com/drive/1ZbL4x0o3SDYBTCcRM_ZijBZwIyWa22M-?usp=sharing) to access this section of the lab as a Jupyter Notebook (Google CoLab, ND users)

## Key Concepts

[Click here](https://github.com/kwaldenphd/python-next-steps/blob/main/part-i-key-concepts.md) for a full list of key concepts and definitions from this section of the lab.

# Overview

<p align="center"><img src="https://github.com/kwaldenphd/python-data-structures/blob/main/images/Python_Data_Structures.png?raw=true" width="1000"></p>

Up to this point, we've been working with what are called "primitive" data types in Python. These include `integer`, `float`, `string`, and `Boolean`.

But we can imagine scenarios where we want to be able to work with more complex data structures or more complex ways of storing and accessing information in a programming language. 

In this lab, we're going to focus on some of the one-dimensional (or linear) data structures available to us in Python. These include `strings`, `lists`, `tuples`, `sets`, and `dictionaries`.

<table><tr><th>Name</th><th>Syntax</th><th>Example</th><th>Description</th></tr>
  <tr><td>String</td><td><code>str(), ""</code><td><code>"Hello world!"</code></td><td>Sequence of characters</td></tr>
  <tr><td>List</td><td><code>list(), []</code><td><code>["apple", "banana", "pear"], [1, 3, 5, 7]</code></td><td>Sequence of objects/values</td></tr>
  <tr><td>Dictionary</td><td><code>dict(), {}</code><td><code>{'first_name': 'Knute', 'last_name':'Rockne', 'class':'1918'}</code></td><td>Key-value pairs</td></tr>
  <tr><td>Set</td><td><code>set(), {}</code><td><code>{"apple", "banana", "pear"}, {1, 3, 5, 7}</code></td><td>Unordered group of unique values</td></tr> 
  <tr><td>Tuple</td><td><code>tuple(), ()</code><td><code>("apple", "banana", "pear"), (1, 3, 5, 7)</code></td><td>Ordered group of values that can include duplicates</td></tr>
  </table>

## Linear Arrays

<p align="center"><img src="https://github.com/kwaldenphd/python-data-structures/blob/main/images/One_Dimensional_Array.jpg?raw=true" width="500"></p>

"An array is a data structure consisting of a collection of elements (values or variables), each identified by at least one array index or key. Depending on the language, array types may overlap (or be identified with) other data types that describe aggregates of values, such as lists and strings. Array types are often implemented by array data structures, but sometimes by other means, such as hash tables, linked lists, or search trees" (Busbee and Braunschweig, "[Arrays and Lists](https://press.rebus.community/programmingfundamentals/chapter/arrays-and-lists/)")

"In computer science, an array is a data structure consisting of a collection of elements (values or variables), each identified by at least one array index or key...The simplest type of data structure is a linear array, also called one-dimensional array" ([Wikipedia, "Array (data structure)](https://en.wikipedia.org/wiki/Array_(data_structure))")

We can think of arrays as one-dimensional, linear data structures made up of a collection of items. As the definitions note, we can access specific elements in the array by using an index or key value. 

"In Python, the built-in array data structure is a list" (Busbee and Braunschweig, "[Arrays and Lists](https://press.rebus.community/programmingfundamentals/chapter/arrays-and-lists/)"). Python also includes a few other built-in array-like data structures, including `sets` and `tuples`. We'll come back to these later in this lab. We can also think of string objects, which are a sequence of characters, as a type of one-dimiensional, linear array.

These **one-dimensional or linear array structures** have a few key properties that differentiate the structures and shape how we can interact with or manipulate them in a programming environment.

Those properties include:
- Mutable: Can values in the structure be changed once it has been created or assigned to a variable?
- Order: Does the order of values in the structure have meaning/significance, or is order not significant?
- Indexing/Slicing: Can values in the structure be accessed using their position or index? Can we isolate values in the structure using their position?
- Duplicates: Does the structure allow duplicate values?

How these properties show up for Python's built-in data structures:

<p align="center"><img src="https://github.com/kwaldenphd/python-data-structures/blob/main/images/Python_Array_Comparison.png?raw=true" width="500"></p>

Each structure has its own specific vocabulary and syntax, but some common operations we can use with these structures:
- Getting number of values in the structure (using the `len()` function)
- For structures that are mutable, adding, modifying, and removing values
- Sorting values in the structure
- Testing for membership, if specific value(s) are present in the structure (using the `in` and `not in` operators)
- For structures that are ordered or indexed, accessing elements using their position

### Index/Indexing and Counting in Python

<p align="center"><img src="https://github.com/kwaldenphd/python-data-structures/blob/main/images/Indexing.PNG?raw=true" width="500"></p>

In Python, **indexing** allows us to refer to individual values in specific data structures using their position.

NOTE: Python (and many other programming languages) are **zero-indexed**, which means counting for index positions begins at `0`.

Let's use the example of a list of strings:

```Python
# list of string objects
fruits = ["apple", "banana", "blueberry", "cherry"]

# check data type
type(fruits)
```

We can determine the number of elements in the list using the `len()` function.

```Python
len(fruits)
```

Remember Python starts at `0` and counts left-to-right. We can access specific values using their position.

```Python
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

The last line of the program returns an `IndexError` message because `pear` is not a value in the list.

We can test for membership using the `in` and `not in` operators.

```Python
# test if apple is in list
print("apple" in fruits)

# test if blueberry is NOT in list
print("blueberry" not in fruits)
```

The `in` and `not in` operators return Boolean `True` or `False` values.

For more on Python's membership operators: [W3Schools, Python Membership Operators](https://www.w3schools.com/python/gloss_python_membership_operators.asp)

We can also use this index syntax with string objects.

```Python
# create string variable
message = "Hello world!"

# return number of characters in string
print(len(message))

# access first character in string
print(message[0])

# access last character in string
print(message[-1])

# test if character x is in string
print('x' in message) # returns false

# test if symbol % is NOT in string
print('%' not in message) # returns true
```

## Associative Arrays

<p align="center"><img src="https://github.com/kwaldenphd/python-data-structures/blob/main/images/Associative_Arrays.png?raw=true" width="500"></p>

The other primary type of array we can encounter is an **associative array**, "an abstract data type that stores a collection of (key, value) pairs, such that each possible key appears at most once in the collection" ([Wikpedia, Associative Array](https://en.wikipedia.org/wiki/Associative_array))

Python stores associate arrays using the **dictionary** data structure. Python dictionaries consist of key-value pairs, where the key is working as an identifier or index.

A preliminary example in Python:

```Python
# create dictionary
english_to_french = {
  'one': 'un',
  'two': 'deux',
  'three': 'trois',
  'four': 'quatre',
  'five': 'cinq'
}

# check data type
type(english_to_french)
```

We can use the index operator (`[]`) and key values to select specific values in the dictionary.

```Python
# access value for one key
english_to_french['one']

# access value for five key
english_to_french['five']

# access value for asdf key
english_to_french['asdf']
```

The last line will return a `KeyError` because `asdf` is not a key in this dictionary.

We can use the `.keys()` and `.values()` methods to output all of the keys or values in a dictionary.

```Python
# output keys
print(english_to_french.keys())

# output values
print(english_to_french.values())
```

# Data Structures in Python

<p align="center"><img src="https://github.com/kwaldenphd/python-data-structures/blob/main/images/Python_Data_Structures.png?raw=true" width="1000"></p>

Before we dive into more detail on these data structures in Python, remember some properties include:
- Mutable: Can values in the structure be changed once it has been created or assigned to a variable?
- Order: Does the order of values in the structure have meaning/significance, or is order not significant?
- Indexing/Slicing: Can values in the structure be accessed using their position or index? Can we isolate values in the structure using their position?
- Duplicates: Does the structure allow duplicate values?

How these properties show up for Python's built-in data structures:

<p align="center"><img src="https://github.com/kwaldenphd/python-data-structures/blob/main/images/Python_Array_Comparison.png?raw=true" width="500"></p>

Each structure has its own specific vocabulary and syntax, but some common operations we can use with these structures:
- Getting number of values in the structure (using the `len()` function)
- For structures that are mutable, adding, modifying, and removing values
- Sorting values in the structure
- Testing for membership, if specific value(s) are present in the structure (using the `in` and `not in` operators)
- For structures that are ordered or indexed, accessing elements using their position

## Strings

"A string data type is traditionally a sequence of characters, either as a literal constant or as some kind of variable...A string is generally considered a data type and is often implemented as an array data structure of bytes (or words) that stores a sequence of elements, typically characters, using some character encoding" (Busbee and Braunschweig, "[String Data Type](https://press.rebus.community/programmingfundamentals/chapter/string-data-type/)")

"Like many other popular programming languages, strings in Python are arrays of bytes representing unicode characters. However, Python does not have a character data type, a single character is simply a string with a length of 1. Square brackets can be used to access elements of the string" ([W3Schools, Python Strings](https://www.w3schools.com/python/python_strings.asp))

Python examples:
```Python
# creating a string variable
x = "Hello World!"

# checking data type
type(x)
```

```Python
# converting to a string data type
y = 7
y = str(y)

# checking data type
type(y)
```

Some Python string syntax we've seen previously:

```Python
# create string variable
message = "Hello world!"

# return number of characters in string
len(message)

# access first character in string
message[0]

# access last character in string
message[-1]

# test if character x is in string
'x' in message # returns false

# test if symbol % is NOT in string
'%' not in message # returns true
```

We can use the `in` operator in combination with `if-then-else` logic:

```Python
# create string variable
message = "Hello world!"

# if-then-else logic testing for specific characters in the string
if "!" in message:
  print("An exclamation point is present in this string")
  
else:
  print("An exclamation point is not present in this string")
```

Remember we can use concatenation to join or combine string objects.

```Python
# first and last name variables
first = "Knute"
last = "Rockne"

# use concatenation to create full name
name = first + " " + last
print(name)
```

### String Methods

Python includes a number of built-in methods we can use to interact with strings. Brief explanations and examples are provided for some common string methods.

#### Capitalization

- `.title()` (title case)
- `.upper()`(upper case)
- `.lower()` (lower case)

```Python
# create name variable
name = "Knute Rockne

# print in title case
print(name.title())

# print in lower case
print(name.lower())

# print in upper case
print(name.upper())
```

#### Searching

- `.count()` (returns number of times specific value appears in a string)
- `.startswith()` (returns Boolean True/False value if string begins with specific value
- `.endswith()` (returns Boolean True/False value if string ends with specific value)
- `.find()` (returns index for specific value in string, searching left-to-right)
- `.rfind()` (returns index for specific value in string, searching right-to-left)
- `.index()` (returns index for specific value in string)
- `.rfind()` (returns index for specific value in string, searching right-to-left)

```Python
# create color variable
color = "chartreuse"

# return number of e characters in string
print(color.count("e")

# return true/false if string begins with value
print(color.startswith("e")) # returns false

# return true/false if string ends with value
print(color.endswith("e")) # returns true

# returns position for first occurance of value in the string
print(color.find("e")) # returns 6

# returns index for first occurance of value in the string
print(color.index("e")) # returns 6

# returns position for first occurance of a value in the string searching right-to-left
print(color.rfind("e")) # returns 1

# returns index for first occurance of a value in the string searching right-to-left
print(color.rindex("e")) # returns 1
```

We can also use these methods to search for a substring within a string.

```Python
# create string variable
passage = "As there is no other school within more than a hundred miles, this college cannot fail to succeed. Before long, it will develop on a large scale. It will be one of the most powerful means for good in this country."

# return true/false if string ends with substring
print(passage.endswith("good")) # returns false

# returns position for first occurance of substring
print(passage.find("college"))
```

#### Modifying 

Strings in Python are immutable- that is values in the string cannot be modified once it has been created and assigned to a variable. But Python include string methods that facilitate modifying a string to create a new string object.

`.replace()` replaces a value in a string. Syntax: `.replace("OLD VALUE", "NEW VALUE")`

`.split()` splits a string at a specific separator and returns a list. The default separator is a space or whitespace character. Syntax: `.split("SEPARATOR")`

`.strip()` trims specific character(s) from a string. The default character `.strip()` removes is a whitespace character. Syntax: `.strip("CHARACTERS TO STRIP")`

```Python
# create string variable
passage = "As there is no other school within more than a hundred miles, this college cannot fail to succeed. Before long, it will develop on a large scale. It will be one of the most powerful means for good in this country."

# replace value in string
modified = passage.replace("cannot", "can't")
print(modified)

# split string at separator
sentences = passage.split(". ")
print(sentences)

# remove strip whitespace from string
modified = passage.strip()
print(modified)
```

For more on strings (general):
- Kenneth Leroy Busbee and Dave Braunschweig, "[String Data Type](https://press.rebus.community/programmingfundamentals/chapter/string-data-type/)" in *Programming Fundamentals*

More on strings in Python:
- [W3Schools, Python Strings](https://www.w3schools.com/python/python_strings.asp)
- [W3Schools, Python String Methods](https://www.w3schools.com/python/python_ref_string.asp)
- Allen Downey, Chapter 8 "Strings" in *[Think Python: How To Think Like a Computer Scientist](https://www.oreilly.com/library/view/think-python-2nd/9781491939406/)* (O'Reilly, 2016): 85-99.

### Comprehension Check

<table>
 <tr><td>
<img src="https://github.com/kwaldenphd/internet/blob/main/images/clipboard.png?raw=true" alt="Clipboard icon" width="50"/></td>
  <td><a href="https://docs.google.com/forms/d/e/1FAIpQLSdFMybseRW8-rommWKphdCFBgqWtpxCY1z8wT2_qk3NaJ8awQ/viewform?usp=sf_link">Strings in Python Comprehension Check</a></td>
  </tr>
  </table>

### Application

Q1: Write a program that converts integer, float, or boolean values to a string, using the `str()` function.

Q2: Write a program that prompts the user to enter a 6-letter word, and then prints the first, third, and fifth letters of that word.

Q3: Modify the program provided below to search for the character `q` or `u` in the string. Does it always return the index number you expect? What index is returned if you ask for the index of the letter u (i.e., what happens when the desired character appears more than once in the string)?

```Python
# program you're modifying for Q8
# assign string variable
color = "turquoise"

# get index number of t character
index_number = color.index("t")

# show index number as part of print statement
print ("The index number for the letter t within the word " + color + " is " + index_number)
```

## Lists

"An array is a data structure consisting of a collection of elements (values or variables), each identified by at least one array index or key...In Python, the built-in array data structure is a list" (Busbee and Braunschweig, "[Arrays and Lists](https://press.rebus.community/programmingfundamentals/chapter/arrays-and-lists/)")
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

Some Python list syntax we've seen previously:

```Python
# list of string objects
fruits = ["apple", "banana", "blueberry", "cherry"]

# check data type
type(fruits)

# determine number of elements in list
len(fruits)
```

We can access specific values using their position.

```Python
# access first value 
fruits[0]

# access second value
fruits[1]

# access third value
fruits[2]

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

The last line of the program returns an `IndexError` message because `pear` is not a value in the list.

We can test for membership using the `in` and `not in` operators.

```Python
# test if apple is in list
"apple" in fruits

# test if blueberry is NOT in list
"blueberry" not in fruits
```

### Nested Lists, or Lists With Sublists

Lists can also contain other lists- this is referred to as nested lists or sub-lists.

Syntax for selecting items or values within a nested list: `list_name[list_item_number][sublist_item_number]`

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

We would also use the double bracket syntax to modify a sublist or a value within a sublist.

```Python
# modify second value in last sublist
points[2][1] = 4

# show updated list
points
```

### List Methods

#### Modifying

Unlike strings, lists in Python are mutable, meaning they can be modified after they have been created.

We can use the index and assignment operators (`[]` and `=`) to modify specific values.

```Python
# list of string objects
fruits = ["apple", "banana", "blueberry", "cherry"]

# modify second value
fruits[1] = "peach"

# show new list
print(fruits)
```

We can add values to a list using `.append()`, `.insert()`, or `.extend()`.
- `.append()` adds or appends a value to the end of a list
- `.insert()` adds or inserts a value at a specific position
- `.extend()` extends a list by adding specific elements to the end of the current list

```Python
# create list of numbers
numbers = [1, 3, 5, 7, 9]

# add value to end of list using append
numbers.append(13)

# show updated list
print(numbers)
```

```Python
# show updated list
print(numbers)

# insert value at specific position
numbers.insert(4, 11)

# show updated list
print(numbers)
```

```Python
# show updated list
print(numbers)

# create second list of number values
num2 = [15, 17, 19]

# add num2 to numbers using extend
numbers.extend(num2)

# show updated list
print(numbers)
```

NOTE: for lists with string objects, `.extend()` works similarly to concatenation.

We can remove values from a list using `.remove()`, `.pop()`, or `del`.
- `.remove()` removes the first matching element from a list
- `.pop()` removes an item at a specific position; if no index is supplied, last element is removed
- `del` removes or deletes the value at a specific position

```Python
# show updated list
print(numbers)

# remove 19 using remove
numbers.remove(19)

# show updated list
print(numbers)
```

```Python
# show updated list
print(numbers)

# remove 17 using pop
numbers.pop(-1)

# show updated list
print(numbers)
```

```Python
# show updated list
print(numbers)

# remove 15 using del
del numbers[7]

# show updated list
print(numbers)
```

#### Slicing

<p align="center"><img src="https://github.com/kwaldenphd/python-data-structures/blob/main/images/Python_List_Slicing.png?raw=true" width="500"></p>

We can also modify a list using a technique called **list slicing**, selecting multiple values in the list using their position.

In Python, we use a combination of index operators `[]` and index values for list slicing.

```Python
# list of strings
dorms = ["alumni", "badin", "baumer", "breen-phillips", "carroll", "cavanaugh", "dillon", "duncan", "dunne", "farley", "fisher", "flaherty", "howard", "johnson", "keenan", "keough", "knott", "lewis", "lyons", "mcglinn", "morrissey", "oneill", "pangborn", "pasquerilla east", "pasquerilla west", "ryan", "st. edward's", "sigfried", "sorin", "stanford", "walsh", "welsh", "zahm"]

# use list slicing to show first 3 strings
print(dorms[0:3])
```

For more on list slicing in PythoN:
- [Geeks for Geeks, "Python List Slicing"](https://www.geeksforgeeks.org/python-list-slicing/)

#### Searching & Sorting

We can search for values in a list using `.count()` or `.index()`.
- `.count()` returns the number of times a value appears in the list
- `.index()` returns the specific position for a list item

```Python
# show list
print(dorms)

# show nubmer of times howard appears in list
print(dorms.count("howard"))

# show index position for lewis
print(dorms.index("lewis"))
```

We can also test for membership using the `in` and `not in` operators.

```Python
# tests if welsh is in dorms list
"welsh" in dorms # returns True

# tests if sophomore is not in dorms list
"sophomore" not in dorms # returns True
```

We can sort the values in the list using `.sort()`, `sorted()`, and `.reverse()`.

A few notes on sorting lists in Python.
- Ascending order in Python is `[0, 1, 2, 3..]` and `[a, b, c, d..]`
- Sorting a list **in-place** changes the underlying order of items in a list
- Generating a sorted version of a list **does not** change the underlying item order

So how do the sorting functions work in Python?
- `.sort()` does not have any output- it sorts the list in place; we can set the `reverse` parameter to `True` to sort in descending order
- `.sorted()` returns a sorted version of the list
- `.reverse()` does not have any output- it reverse sorts the list in place


```Python
# show list of dorms
print(dorms)

# generate sorted version using sorted
print(sorted(dorms))

# change underlying order using a reverse sort
dorms.sort(reverse=True) # remember sort does not have an output

# show updated list
print(dorms)
```

Another workflow for sorting list values in descending order:

```Python
# sort list alphabetically
dorms.sort()

# show updated list
print(dorms)

# reverse sort using reverse
dorms.reverse()

# show updated list
print(dorms)
```

#### Summary Statistics

Python includes a few built-in fucntion that calculate summary statistics for lists with numeric values.
- `.max()` identifies the highest value in the list
- `.min()` identifies the lowest value in the list
- `.sum()` calculates the sum for all values in the list

```Python
# create list of numbers
numbers = [1, 3, 5, 7, 9, 11, 13, 15, 17]

# highest value
print("The highest value in this list is ", str(max(numbers)))

# lowest value
print("The lowest value in this is list ", str(min(numbers)))

# sum
print("The sum of the values in this list is ", str(sum(numbers)))
```

#### Additional Resources

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

More on arrays/lists (general):
- Kenneth Leroy Busbee and Dave Braunschweig, "[Arrays and Lists](https://press.rebus.community/programmingfundamentals/chapter/arrays-and-lists/)" in *Programming Fundamentals*

More on lists in Python:
- [W3Schools, Python Lists](https://www.w3schools.com/python/python_lists.asp)
- [W3Schools, Python List Methods](https://www.w3schools.com/python/python_lists_methods.asp)
- Allen Downey, Chapter 10 "Lists" in *[Think Python: How To Think Like a Computer Scientist](https://www.oreilly.com/library/view/think-python-2nd/9781491939406/)* (O'Reilly, 2016): 107-124.

### Looking Ahead

In an upcoming lab, we'll look at how to create looping structures (or code blocks that repeat under specific conditions). But for now, let's take a step back and think about how Python interacts with or treats the items in our list.

For example, when we're using the `in` operator, how does Python test for membership (i.e. see if the value we're looking for is located in the list)? Python accomplishes this via **iteration**, which involves iterating over each item in the list. 

So Python starts at the first item in the list (index position `0`), and goes through each item on the list (left to right) until it reaches the end of the list. Again, we will have a whole lab on iteration and loops, but a few quick examples for now just to illustrate the concept of iteration.

We can use a **`for` loop** to iterate over the items in a list.

```Python
# list of numbers
numbers = [1, 3, 5, 7, 9, 11, 13, 15, 17]

# sample for loop that iterates over items in list and outputs each number
for number in numbers:
 print(number)
```

We can also nest `if` statements in a `for` loop:
```Python
# list of numbers
numbers = [1, 3, 5, 7, 9, 11, 13, 15, 17]

# for loop that iterates over numbers
for number in numbers:
  if number < 10:
    print(str(number) + " is less than 10")
  elif number > = 10 and number < 15:
    print(str(number) + " is greater than or equal to 10 and less than 15")
  else:
    print(str(number) + " is greater than 15")
```

Again, more to come on loops and iteration.

### Comprehension Check

<table>
 <tr><td>
<img src="https://github.com/kwaldenphd/internet/blob/main/images/clipboard.png?raw=true" alt="Clipboard icon" width="50"/></td>
  <td><a href="https://docs.google.com/forms/d/e/1FAIpQLSdJ6e9GsPUCYx3EVw-n9ajIGUo0zAJOEGolkfgNg4aVT0Ix8A/viewform?usp=sf_link">Lists in Python Comprehension Check</a></td>
  </tr>
  </table>

### Application

Q4: Write a program that creates a list of numbers. Use the arguments and syntax presented in this section of the lab to include code in your program that answers the following questions:
- What is the length of your list? 
- What is the number position for each of the items in your list? 
- How would you return the value of the first item? 
- How would you return the value of the last item?

Answer to this question includes program + comments that document process and explain your code.

Q5: Modify your Q4 program (working with the same list), using arguments and syntax covered in this section of the lab to accomplish the following tasks:
- Add a new item to your list
- Delete an item from your list
- Sort your list in-place
- Generate a sorted version of your list
- Reverse your list in-place
- Determine the min and max values for your list

Answer to this question includes program + comments that document process and explain your code.

Q6: Write a program that creates a list with the following values: `[[0, 1], [2, 3], [4, 5]]`. Use the arguments and syntax presented in this section of the lab to include code in your program that answers the following questions:
- What is the second element?
- How would you change 4 to 'four'?
- How would you change 1 to 'one'?
- How would you print out each sub-list (one sub-list per line)?
  * *HINT: Could a `for` loop be helpful for this task?*
- How would you print out each number (one number per line)?
  * *HINT: Could a `for` loop be helpful for this task?*

Answer to this question includes program + comments that document process and explain your code.

Q7: Modify your Q6 program (working with the same list), using arguments and syntax covered in this section of the lab to accomplish the following tasks:
- Add a new item to your list
- Delete an item from your list
- Sort your list in-place
- Generate a sorted version of your list
- Reverse your list in-place
- Determine the min and max values for your list

Answer to this question includes program + comments that document process and explain your code.

## Dictionaries

<p align="center"><img src="https://github.com/kwaldenphd/python-data-structures/blob/main/images/Key_Value_2.png?raw=true" width="500"></p>

Python stores associate arrays using the **dictionary** data structure. Python dictionaries consist of key-value pairs, where the key is working as an identifier or index. To put that another way, a dictionary is a mapping between a set of indeces (keys) and a set of values. Each key maps to a value, and the association of a key and a value is called a **key-value pair**.

Some dictionary syntax we encountered previously in this lab:

```Python
# create dictionary
english_to_french = {
  'one': 'un',
  'two': 'deux',
  'three': 'trois',
  'four': 'quatre',
  'five': 'cinq'
}

# check data type
type(english_to_french)
```

We can also create a dictionary using the `dict()` function.
```Python
# create dictionary
english_to_french = dict({
  'one': 'un',
  'two': 'deux',
  'three': 'trois',
  'four': 'quatre',
  'five': 'cinq'
}

# check data type
type(english_to_french)
```

We can use the index operator (`[]`) and key values to select specific values in the dictionary.

```Python
# access value for one key
english_to_french['one']

# access value for five key
english_to_french['five']

# access value for asdf key
english_to_french['asdf']
```

The last line will return a `KeyError` because `asdf` is not a key in this dictionary.

We can use the `.keys()` and `.values()` methods to output all of the keys or values in a dictionary.

```Python
# output keys
print(english_to_french.keys())

# output values
print(english_to_french.values())
```

We can also use iteration to output the keys or values in a dictionary. Let's say we want to iterate by keys through our dictionary.

We can use a `for` loop to tell Python "`FOR` each key-value pair in my dictionary...do this thing!"

An example that prints out the key for each key-value pair:

```Python
# for loop that outputs keys
for key in english_to_french.keys():
  print(key)
```

We can also iterate over key-value pairs, using the `.items()` method.

```Python
# for loop that outputs key-value pairs using items
for key, value, in english_to_french.items():
  print(key, value)
```

Again, more on iteration in an upcoming lab.

In the previous example, our keys and our values were all strings. But we can also have a dictionary where the values are a different data type- for example, a list.

```Python
terms = { # create dictionary with list values
    'nouns': ['person', 'place','thing'],
    'verbs': ['hop', 'skip', 'jump'],
    'prepositions': ['in', 'on', 'over', 'under'],
    'adjectives': ['big', 'small', 'quiet', 'loud'],
}

print(terms.keys()) # show keys
print(terms['verbs']) # show values for verbs key
```

### Modifying 

We can modify values in our dictionary using the index `[]` and assignment `=` operators. This is also the workflow we would use to add values to a dictionary.

```Python
# create new dictionary
numbers = {
  '1': 'one',
  '2': 'two',
  '3': 'five'
}

# modify value for 3 key
numbers['3'] = 'three'

# add key-value pairs to dictionary
numbers['4'] = 'four'
numbers['5'] = 'five'
numbers['6'] = 'six'

# show updated dictionary
for key value in numbers.items():
  print(key, value)
```

For more on dictionaries in Python:
- [W3Schools, Python Dictionaries](https://www.w3schools.com/python/python_dictionaries.asp)
- Allen Downey, Chapter 11 "Dictionaries" in *[Think Python: How To Think Like a Computer Scientist](https://www.oreilly.com/library/view/think-python-2nd/9781491939406/)* (O'Reilly, 2016): 125-138.

### Comprehension Check

<table>
 <tr><td>
<img src="https://github.com/kwaldenphd/internet/blob/main/images/clipboard.png?raw=true" alt="Clipboard icon" width="50"/></td>
  <td><a href="https://docs.google.com/forms/d/e/1FAIpQLScf-FDL2IyVOf0Kj3knOZukP__rcAZuCiukTmFUQDXz8KffMA/viewform?usp=sf_link">Dictionaries in Python Comprehension Check</a></td>
  </tr>
  </table>

### Application

Q8: Write a program that creates a dictionary on a topic of your choosing. Include at least 5 key-value pairs. Use arguments and syntax covered in this section of the lab to accomplish the following tasks:
- Add a new element to your dictionary
- Update or modify an element in your dictionary
- Print a list of all the keys in your dictionary
- Print a list of all the values in your dictionary

Answer to this question includes program + comments that document process and explain your code.

## Tuples

"Tuples are used to store multiple items in a single variable...A tuple is a collection which is ordered and unchangeable. Tuples are written with round brackets...and allow duplicate values" ([W3Schools, Python Tuples](https://www.w3schools.com/python/python_tuples.asp))

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

Some of the methods we've already seen for lists and strings can also be used with tuples.

```Python
# return number of items in tuple
len(sample)

# access first item in tuple
sample[0]

# count number of times specific value appears in  tuple
sample.count("apple")

# return index for specific value
sample.index("pear")
```

NOTE: The last line of code will return an error because `peach` does not appear in this tuple.

For more on tuples in Python:
- [W3Schools, Python Tuples](https://www.w3schools.com/python/python_tuples.asp)
- Allen Downey, Chapter 12 "Tuples" in *[Think Python: How To Think Like a Computer Scientist](https://www.oreilly.com/library/view/think-python-2nd/9781491939406/)* (O'Reilly, 2016): 139-150.

## Sets

<p align="center"><img src="https://github.com/kwaldenphd/python-data-structures/blob/main/images/Python_Sets.jpg?raw=true" width="500"></p>

A set is an unordered collection of unique objects. Sets are primarily used to see if an object or value is in the collection (membership). Python supports a number of set operations, but one of the primary uses is to test for membership.

We can use the `in` operator to test for membership with a set.

```Python
# create a set
s = set([0,1,2])

# show set values
s

# test if 0 is in s
0 in s # returns true

# test if 7 is in s
7 in s # returns false
```

We can add items to our set using `.add()` or remove them using `.remove()`.

```Python
# add values to set
s.add(3)
s.add(4)
s.add(5)

# show new set with values
s
```

```Python
# remove 1 number value from set
s.remove(5)

# show updated set
s
```

For more on sets in Python:
- [W3Schools, Python Sets](https://www.w3schools.com/python/python_sets.asp)

### Comprehension Check (Tuples and Sets)

<table>
 <tr><td>
<img src="https://github.com/kwaldenphd/internet/blob/main/images/clipboard.png?raw=true" alt="Clipboard icon" width="50"/></td>
  <td><a href="https://docs.google.com/forms/d/e/1FAIpQLSf63bUSp3wlTnPz_ZTGCKjW-uotPYYD6FaOH9R3DqtFJPY_hg/viewform?usp=sf_link">Tuples and Sets in Python Comprehension Check</a></td>
  </tr>
  </table>

### Application (Tuples and Sets)

Q9: Write a program that creates a tuple with at least 4 values. Use arguments and syntax covered in this section of the lab to accomplish the following tasks:
- Count the number of times a specific value appears
- Return the index for a specific value
- Access a value using its index

Answer to this question includes program + comments that document process and explain your code.

Q10: Write a program that creates the set `s` with the following values: `[1, 3, 5, 7, 9]`. Use arguments and syntax covered in this section of the lab to accomplish the following tasks:
- Test to see if the value `11` is a member of the set
- Test to see if the value `7` is a member of the set
- Add a value to the set
- Remove a value from the set

Answer to this question includes program + comments that document process and explain your code.

# Putting It All Together

<p align="center"><img src="https://github.com/kwaldenphd/python-data-structures/blob/main/images/Python_Array_Comparison.png?raw=true" width="500"></p>

## Additional Resources

Allen Downey, *[Think Python: How To Think Like a Computer Scientist](https://www.oreilly.com/library/view/think-python-2nd/9781491939406/)* (O'Reilly, 2016).
- Includes chapters on strings, lists, tuples, and dictionaries

Section 3.1 from Chapter 3 "Built-in Data Structures, Functions, and Files" in Wes McKinney's *[Python for Data Analysis, 3rd edition](https://www.oreilly.com/library/view/python-for-data/9781098104023/)* (O'Reilly, 2022): 51-68.

# Lab Notebook Questions (for this section)

Q1: Write a program that converts integer, float, or boolean values to a string, using the `str()` function.

Q2: Write a program that prompts the user to enter a 6-letter word, and then prints the first, third, and fifth letters of that word.

Q3: Modify the program provided below to search for the character `q` or `u` in the string. Does it always return the index number you expect? What index is returned if you ask for the index of the letter u (i.e., what happens when the desired character appears more than once in the string)?

```Python
# program you're modifying for Q8
# assign string variable
color = "turquoise"

# get index number of t character
index_number = color.index("t")

# show index number as part of print statement
print ("The index number for the letter t within the word " + color + " is " + index_number)
```

Q4: Write a program that creates a list of numbers. Use the arguments and syntax presented in this section of the lab to include code in your program that answers the following questions:
- What is the length of your list? 
- What is the number position for each of the items in your list? 
- How would you return the value of the first item? 
- How would you return the value of the last item?

Answer to this question includes program + comments that document process and explain your code.

Q5: Modify your Q4 program (working with the same list), using arguments and syntax covered in this section of the lab to accomplish the following tasks:
- Add a new item to your list
- Delete an item from your list
- Sort your list in-place
- Generate a sorted version of your list
- Reverse your list in-place
- Determine the min and max values for your list

Answer to this question includes program + comments that document process and explain your code.

Q6: Write a program that creates a list with the following values: `[[0, 1], [2, 3], [4, 5]]`. Use the arguments and syntax presented in this section of the lab to include code in your program that answers the following questions:
- What is the second element?
- How would you change 4 to 'four'?
- How would you change 1 to 'one'?
- How would you print out each sub-list (one sub-list per line)?
  * *HINT: Could a `for` loop be helpful for this task?*
- How would you print out each number (one number per line)?
  * *HINT: Could a `for` loop be helpful for this task?*

Answer to this question includes program + comments that document process and explain your code.

Q7: Modify your Q6 program (working with the same list), using arguments and syntax covered in this section of the lab to accomplish the following tasks:
- Add a new item to your list
- Delete an item from your list
- Sort your list in-place
- Generate a sorted version of your list
- Reverse your list in-place
- Determine the min and max values for your list

Answer to this question includes program + comments that document process and explain your code.

Q8: Write a program that creates a dictionary on a topic of your choosing. Include at least 5 key-value pairs. Use arguments and syntax covered in this section of the lab to accomplish the following tasks:
- Add a new element to your dictionary
- Update or modify an element in your dictionary
- Print a list of all the keys in your dictionary
- Print a list of all the values in your dictionary

Answer to this question includes program + comments that document process and explain your code.

Q9: Write a program that creates a tuple with at least 4 values. Use arguments and syntax covered in this section of the lab to accomplish the following tasks:
- Count the number of times a specific value appears
- Return the index for a specific value
- Access a value using its index

Answer to this question includes program + comments that document process and explain your code.

Q10: Write a program that creates the set `s` with the following values: `[1, 3, 5, 7, 9]`. Use arguments and syntax covered in this section of the lab to accomplish the following tasks:
- Test to see if the value `11` is a member of the set
- Test to see if the value `7` is a member of the set
- Add a value to the set
- Remove a value from the set

Answer to this question includes program + comments that document process and explain your code.
