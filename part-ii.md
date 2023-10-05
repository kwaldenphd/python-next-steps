# Python Next Steps Part II: Control Structures, Iteration & Loops

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>This tutorial was written by Katherine Walden and is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

# Table of Contents

- [Lecture & Live Coding](#lecture--live-coding)
- [Key Concepts](#key-concepts)
- [Overview](#overview)
  * [Iteration Control Structures](#iteration-control-structures)
  * [Iteration in Python](#iteration-in-python)
- [`if-then-else`](#if-then-else)
  * [`while` Statements](#while-statements)
  * [Indentation](#indentation)
- [Application](#application)
- [Loops](#loops)
  * [Event-Controlled Loops](#event-controlled-loops)
  * [Count-Controlled Loops](#count-controlled-loops)
- [Additional Considerations](#additional-considerations)
  * [`range()`](#range)
  * [`enumerate()`](#enumerate)
  * [Infinite Loops](#infinite-loops)
  * [Break & Continue](#break--continue)
- [Putting It All Together](#putting-it-all-together)
- [Lab Notebook Questions (for this section)](#lab-notebook-questions-for-this-section)

[Click here](https://colab.research.google.com/drive/1SpA0gG6AuhxhXjdlO2PkOO80G-bkcKAY?usp=sharing) to access this section of the lab procedure as a Jupyter Notebook (Google CoLab, ND users)


# Lecture & Live Coding

Throughout this lab, you will see a Panopto icon at the start of select sections.

This icon indicates there is lecture/live coding asynchronous content that accompanies this section of the lab. 

You can click the link in the figure caption to access these materials (ND users only).

Example:

<table>
 <tr><td>
<img src="https://elearn.southampton.ac.uk/wp-content/blogs.dir/sites/64/2021/04/PanPan.png" alt="Panopto logo" width="50"/></td>
<td><a href="https://notredame.hosted.panopto.com/Panopto/Pages/Viewer.aspx?pid=8759844b-e5a0-4fa3-98cf-af360142d72b">Lecture/live coding playlist</a></td>
  </tr>
  </table>

# Key Concepts

[Click here](https://github.com/kwaldenphd/python-next-steps/blob/main/part-ii-key-concepts.md) for a full list of key concepts and definitions from this section of the lab.

# Overview

From Busbee and Braunschweig's "[Structured Programming](https://press.rebus.community/programmingfundamentals/chapter/structured-programming/)" from *Programming Fundamentals*
    
"One of the most important concepts of programming is the ability to control a program so that different lines of code are executed or that some lines of code are executed many times. The mechanisms that allow us to control the flow of execution are called control structures. Flowcharting is a method of documenting (charting) the flow (or paths) that a program would execute. There are three main categories of control structures:"
  * Sequence [executes in given sequence]
  * Selection [selects between two or more flows using condition or question]
  * Iteration [repeats same piece of code multiple times]
  
We're going to spend multiple labs thinking through control structures and control flow, with a focus on how we use them in Python.
    
Examples of control structures in Python include:
- `if-then-else` (syntax: `if`, `else`, `elif`)
- `while` statements (syntax: `while`)

Foundational to most control structures are something called conditional statements- code that tests whether a condition is `True` or `False`. 

# `if-then-else` 

From Busbee and Braunschweig's "[Selection Control Structures](https://press.rebus.community/programmingfundamentals/chapter/selection-control-structures/)" from *Programming Fundamentals*:
- "The basic attribute of a selection control structure is to be able to select between two or more alternate paths. This is described as either two-way selection or multi-way selection. A question using Boolean concepts usually controls which path is selected. All of the paths from a selection control structure join back up at the end of the control structure, before moving on to the next lines of code in a program."
- "The if then else control structure is a two-way selection"

In Python, this logic is expressed using the `if`, `else`, and `elif` syntax. From W3Schols, "[Python Conditions](https://www.w3schools.com/python/python_conditions.asp)":
- "An 'if statement' is written by using the `if` keyword"
- "The `elif` keyword is Python's way of saying 'if the previous conditions were not true, then try this condition'"
- "The `else` keyword catches anything which isn't caught by the preceding conditions"

```Python
# assign variables
x = 5
y = 7

# if statement
if x > y:
    print("The value of x is greater than the value of y")

# else if statement
elif x == y:
    print("The value of x is equal to the value of y")

# else statement
else:
    print("The value of x is less than the value of y")
```

To frame this another way:
- `if` introduces and evaluates an initial condition. The lines of code indented under `if` will only run when the `if` statement is `True`
- `else-if` or `elif` introduces and evaluates another condition. The lines of code indented under `elif` will only run when the `elif` statement is `True`
- `else` **does not** introduce a new condition. The lines of code indented under `else` will only run when the preceeding `if`/`elif` statements **are not** true 

For more on `if-then-else` logic in Python:
- [W3Schools, Python If ... Else](https://www.w3schools.com/python/python_conditions.asp)

## `while` statements

Another way to express `if-then-else` logic in Python is using a `while` statement. 

A `while` statement tests for an initial condition, and the lines of code indented under `while` run only when the initial condition is `True`.

An example of the prior `if-then-else` program, written using `while`.
    
```Python
# while statement with initial condition
while x != y:
  # if statement
  if x > y:
      print("The value of x is greater than the value of y")

      # else if statement
  elif x == y:
      print("The value of x is equal to the value of y")

  # else statement
  else:
      print("The value of x is less than the value of y")
```

As we see in this example, we can nest multiple `if-then-else` logical statements in the same piece of code.

## Indentation

As we continue to introduce more programming concepts and further our work in Python, we're starting to see **code blocks** and **indentation** at work.

From Busbee and Braunschweig's "[Code Blocks](https://press.rebus.community/programmingfundamentals/chapter/code-blocks/)" from *Programming Fundamentals*:
- "A code block, sometimes referred to as a compound statement, is a lexical structure of source code which is grouped together. Blocks consist of one or more declarations and statements. A programming language that permits the creation of blocks, including blocks nested within other blocks, is called a block-structured programming language. Blocks are fundamental to structured programming, where control structures are formed from blocks."
   
In Python syntax, code blocks are marked by indentation, or indented lines of code. 

```Python
# an example of indentation in Python
if expression:
   statement
   statement
else:
   statement
   statement
```

## Comprehension Check

<table>
 <tr><td>
<img src="https://github.com/kwaldenphd/internet/blob/main/images/clipboard.png?raw=true" alt="Clipboard icon" width="50"/></td>
  <td><a href="https://docs.google.com/forms/d/e/1FAIpQLSfP5zF_hGh2tEgr0pz3D56a6YiIkjJxcfRZq5YAHcjhZQ3wqw/viewform?usp=sf_link"><code>if-then-else</code> Comprehension Check</a></td>
  </tr>
  </table>

## Application

Q11: Write a program that asks a user to enter a color value and returns an output message comparing that value with your favorite color. This program will use a combination of the `input()` function, comparison operators, and `if-then-else` logic. Answer to this question includes program + comments that document process and explain your code.

Sample output for this program:
```
Your favorite color: green

My age: blue

We don't have the same favorite color.
```

Q12: Write a program that lets the user play a guessing game.
- First, your program should set a number as the "correct answer"
- Then, your program will ask the user to guess a number
- Your program should give a message indicating whether the user's guess is correct, too high, or too low

This program will use a combination of the `input()` function, comparison operators, and `if-then-else` logic. Answer to this question includes program + comments that document process and explain your code.

Sample output for this program (for a correct answer of 7:
```
You guessed 13.
```

## Loops

Testing for membership or returning index values are a couple examples of tasks we can accomplish in Python using iteration.

But let's review the definition of iteration as a control structure. From Busbee and Braunschweig's "[Iteration Control Structures](https://press.rebus.community/programmingfundamentals/chapter/iteration-control-structures/)," in *Programming Fundamentals*:

"In iteration control structures, a statement or block is executed until the program reaches a certain state, or operations have been applied to every element of a collection. This is usually expressed with keywords such as `while`, `repeat`, `for`, or `do..until`. The basic attribute of an iteration control structure is to be able to repeat some lines of code. The visual display of iteration creates a circular loop pattern when flowcharted, thus the word 'loop' is associated with iteration control structures."

Breaking down that definition:
- Iteration (repetition of a process) is a type of control structure
- In programming languages, iteration involves lines of code repeating until a condition is met of the end of a group of values has been reached.
- Because iteration in this context involves a circular pattern, many object-oriented programming languages refer to these structures as `loops`

The power of iteration as a control structure comes from a programming concept called `loops`.

<p align="center"><img src="https://github.com/kwaldenphd/python-loops-iteration/blob/main/images/loop-comparison-diagram.png?raw=true" width="1000"></p>

Most high-level programming languages support two main types of loops: event-controlled and count-controlled
- **Event-controlled loops** test for an initial condition, and execution continues as long as the initial condition is `True`. How many times the loop will execute *is not known*.
- **Count-controlled loops** (sometimes called counter-controlled loops) continue executing for a pre-determined number of times. The number of times the loop will execute is known because the loop is iterating through a collection of objects/values (i.e. a string or list), or the iteration when the initial condition will no longer be `True` is known.

Let's break down each type.

### Event-Controlled Loops

<table>
 <tr><td>
<img src="https://elearn.southampton.ac.uk/wp-content/blogs.dir/sites/64/2021/04/PanPan.png" alt="Panopto logo" width="50"/></td>
<td><a href="https://notredame.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=f8df7787-9bff-4802-9f57-af36014148bd">While Loops in Python</a></td>
  </tr>
  </table>

<p align="center"><img src="https://github.com/kwaldenphd/python-loops-iteration/blob/main/images/while-loop-diagram.png?raw=true" width="500"></p>

In Python, event-controlled loops are written using a `while` statement and are called `while loop`. A `while` statement tests for an initial condition, and the lines of code indented under `while` run only when the initial condition is `True`.

In each iteration through the `while` loop, Python will:
- Evaluate the initial condition (which is a Boolean true/false expression)
- If the condition is `False`, exit the loop and continue the program
- If the condition is `True`, then execute other statements in the body of the loop and return to the beginning of the loop

The basic syntax for a `while` loop:

```Python
# while loop sample syntax
while condition:
	statement(s)
```

To express this logic another way:

```Python
# while loop sample syntax
while THIS CONDITION IS TRUE:
	DO THIS THING
```

For example, in a previous lab, you were asked to write a guessing game program that used a `while` statement. What this program might have looked like:

```Python
# correct answer
secret = 7

# guess
guess = int(input("Guess a number: "))

# while statement
while guess != secret:
  if guess > secret:
    print("Your guess is too high. Better luck next time")
    guess = int(input("Guess again. Enter another number: "))
  else:
    print("Your guess is too low. Better luck next time.")
    guess = int(input("Guess again. Enter another number: "))
  

print("Congrats, you guessed the secret number!")
```

This is an example of a `while` loop. Because the number of times the loop will execute is not known, this is an example of an event-controlled loop. That is, the loop will continue executing (looping) until the initial condition (`guess != secret`) is no longer true.

#### `While` Loop Comprehension Check

<table>
 <tr><td>
<img src="https://github.com/kwaldenphd/internet/blob/main/images/clipboard.png?raw=true" alt="Clipboard icon" width="50"/></td>
  <td><a href="https://docs.google.com/forms/d/e/1FAIpQLSfhrN-wLhsGhxnbEDjBNVkF35Z8p31OIJSDdBfgOtI_KzAlAg/viewform?usp=sf_link">Python While Loops Comprehension Check</a></td>
  </tr>
  </table>
  
#### `While` Loop Application

Q13: Given the following program:

```Python
# assign count variable
count = 1

# while loop
while count <= 5: # initial condition
   print ("Python") # print statement
   count = count + 1 # reassign count

# final print statement
print ("Done")
```

How would you modify the program to print or output the string nine (9) times and also include line numbers as part of the output? Answer to this question includes program + comments that document process and explain your code.

For example, your output might look like the following: 

```
1 Python
2 Python
3 Python
4 Python
5 Python 
6 Python
7 Python
8 Python
9 Python
IS FUN!
```

### Count-Controlled Loops in Python

<table>
 <tr><td>
<img src="https://elearn.southampton.ac.uk/wp-content/blogs.dir/sites/64/2021/04/PanPan.png" alt="Panopto logo" width="50"/></td>
<td><a href="https://notredame.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=decd0417-c579-4ee2-9ed3-af360140fa70">For Loops in Python</a></td>
  </tr>
  </table>

<p align="center"><img src="https://github.com/kwaldenphd/python-loops-iteration/blob/main/images/for-loop-diagram.png?raw=true" width="500"></p>

In Python, count-controlled loops are written using a `for` statement and are called `for loop`. A `for loop` iterates over each value in a group of values- the lines of code nested under the initial statement run for each iteration.

`for` loops let us iterate through a definite set of objects. In each iteration through the `for` loop, Python will:
- Extract one element from the dataset
- Execute the body of the `for` loop using the item bound to the element
- Go back to the first step
- Keep iterating through the loop until reaching the end of the dataset

The basic syntax in a `for` loop:

```Python
# sample for loop syntax
for item in dataset:
 statement(s)
```

In this syntax, `item` is a placeholder for each element in `dataset`. We can replace `item` with another word or letter character.

```Python
# sample for loop syntax
for i in dataset:
	statement(s)
```

In this syntax, `dataset` stands for the group of items we want Python to iterate over. That group of items could be a list, a list variable, string, string variable, etc. 

We've encountered a few `for` loops in previous labs.

Iterating over items in a list:

```Python
# list of numbers
numbers = [1, 3, 5, 7, 9, 11, 13, 15, 17]

# sample for loop that iterates over items in list and outputs each number
for number in numbers:
 print(number)
 ```

Nesting `if-then-else` logic in a `for` loop:

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

A previous lab notebook question asked you to print out each sublist (in a nested list or list of lists) on its own line, and also print the individual values on their own lines.

An approach to that program that doesn't use iteration or a `for` loop:

```Python
# create list with sublists
numbers = [[0, 1], [2, 3], [4, 5]]

# print out each sublist
print(numbers[0])
print(numbers[1])
print(numbers[2])

# print out each number
print(numbers[0][0])
print(numbers[0][1])
# etc
```

Rewriting those programs to use `for` loops:

```Python
# print each sublist
for number in numbers:
  print(number)
  
# print each value in the sublist
for number in numbers:
  for n in number:
    print(n)
```

Another example with dictionary keys and values:

```Python
# create dictionary
states = {"Missouri": "MO", "Indiana": "IN", "Iowa":"IA", "Nebraska":"NE", "Kansas":"KS", "Illinois":"IL", "Ohio":"OH", "Michigan":"MI"}

# show keys
print(states.keys)

# alternate approach that uses for loop
for key in states.keys():
  print(key)

# show values
print(states.values)

# alternate approach that uses for loop
for value in states.values():
  print(value)
```

#### `For` Loop Comprehension Check

<table>
 <tr><td>
<img src="https://github.com/kwaldenphd/internet/blob/main/images/clipboard.png?raw=true" alt="Clipboard icon" width="50"/></td>
  <td><a href="https://docs.google.com/forms/d/e/1FAIpQLSePIOvFVTaQLTUh_xDFByNVUvvqY64sBt2NHpR17hXhF0S8Eg/viewform?usp=sf_link">Python For Loops Comprehension Check</a></td>
  </tr>
  </table>

#### `For` Loop Application

Q14: Let's return to the program we modified for Q13. How would you modify your Q13 answer to use a `for` loop instead of a `while` loop? Answer to this question includes program + comments that document process and explain your code.

```Python
# assign count variable
count = 1

# while loop
while count <= 5: # initial condition
   print ("Python") # print statement
   count = count + 1 # reassign count

# final print statement
print ("Done")
```

As a reminder, your output might look like the following: 

```
1 Python
2 Python
3 Python
4 Python
5 Python 
6 Python
7 Python
8 Python
9 Python
IS FUN!
```

Q15: In a previous program, you were asked to modify the program below to search for the characters `q` and `u` in the string `turquoise`. 

Program you modified:
```Python
# assign string variable
color = "turquoise"

# get index number of t character
index_number = color.index("t")

# show index number as part of print statement
print ("The index number for the letter t within the word " + color + " is " + index_number)
```

Write a program that uses a `for` loop to return all instances of `q` and `u` in the string, not just the first occurrence. Answer to this question includes program + comments that document process and explain your code.

# Additional Considerations

## `range()`

Python's `range()` function allows us to generate a list of integer values. The general syntax:

```Python
range(START VALUE, END VALUE, STEP INTERVAL)
```

The default start value for `range()` is `0`, and the default step interval is `1`.

So for example, `range(6)` would include the values `[0, 1, 2, 3, 4, 5]`. While `range(1, 6, 2)` would include the values `[1, 3, 5]`.

We can use `range()` in combination with `list()` to generate a list of numbers.
- `list(range(6))` would generate the list `[0, 1, 2, 3, 4, 5]`

We can also use `range()` as part of a `for` loop to iterate over a list of numeric values (without having to create that list manually).

For example: 

```Python
# for loop that iterates over values in range
for i in range(0, 3):
 print(i)
 ```

For more information on Python's `range()` function: 
- W3Schools, "[Python Range Function](https://www.w3schools.com/python/ref_func_range.asp)"
- Python documentation, "[4.3 The range() Function](https://docs.python.org/3/tutorial/controlflow.html#the-range-function)"

## `enumerate()`

In a previous lab, we talked about how each item in a list has an index, or a number that indicates its position in the list. We can use the `enumerate()` function to generate a list of pairs containing each item in the list and its index.

We can use the `enumerate()` function as part of a `for` loop.

```Python
# for loop that iterates over list index and values
for index, letter in enumerate('abc'):
 print(index, letter)
```

In this last example, `for index, letter` instructed Python to iterate over both components in the `enumerate()` output. `print(index, letter)` instructed Python to print both components for each element.

For more information on Python's `enumerate()` function: 
- W3Schools, "[Python Enumerate Function](https://www.w3schools.com/python/ref_func_enumerate.asp)"
- Python documentation, "[enumerate](https://docs.python.org/3/library/functions.html#enumerate)"

## Infinite loop

Loops that have no endpoint are called *infinite loops*.

For example, given the following program:

```Python
# assign count variable
count = 1

# while loop
while count <= 5: # initial condition
   print ("Python") # print statement
   count = count + 1 # reassign count

# final print statement
print ("Done")
```

What would happen if we removed `count = count + 1` from the loop? The value of `count` would never change, the initial condition's truth value (`count <= 5`) would never change (because `count` would always equal `1`), and we would have an infinite loop.

## Break & Continue

We can exit a loop immediately by using the `break` statement. `break` will stop or exit the `while` loop even if the condition is true.

For example:

```Python
# assign i variable 
i = 1

# while loop
while i < 6: # initial condition
	
	print(i) # print statement

	if i == 3: # if statement
		break # break statement
	
	i += 1 # reassign i
```

In this example, the loop breaks as soon as the `i == 3` condition is `True`.

We can skip the rest of the body of a loop and move on to the next iteration using `continue`. 

For example:

```Python
# assign the i variable
i = 0

# while loop
while i < 6: # initial condition

	i += 1 # reassign i
	
	if i ==3: # if statement
		continue # continue statement
	
	print(i) # print statement
```

In this example, the current iteration of the loop will stop when `i == 3` is true. Unlike with `break`, the loop will not end. Instead when `i == 3` is true, the loop will skip over the final nested `print` statement and return to the beginning of the loop for a new iteration.

For more on `break` and `continue`:
- W3Schools, "[Python break Keyword](https://www.w3schools.com/python/ref_keyword_break.asp)"
- W3Schools, "[Python For Break](https://www.w3schools.com/python/gloss_python_for_break.asp)"
- W3Schools, "[Python Continue For Loop](https://www.w3schools.com/python/gloss_python_for_continue.asp)"

## Additional Loop Considerations Comprehension Check

<table>
 <tr><td>
<img src="https://github.com/kwaldenphd/internet/blob/main/images/clipboard.png?raw=true" alt="Clipboard icon" width="50"/></td>
  <td><a href="https://docs.google.com/forms/d/e/1FAIpQLSdQCHB6tauQplugunNCqJrVJiZ0W-WqAHAizAft_izi_8X_1g/viewform?usp=sf_link">Additional Python Loop Considerations Comprehension Check</a></td>
  </tr>
  </table>

# Putting It All Together

NOTE: For the following lab notebook questions, write two programs for each- one that uses a `while` loop and one that uses a `for` loop to accomplish the same task. 

Q16: Write a program that counts from 10 down to 1, and then prints "Blastoff!" Answer to this question includes programs with a `while` loop and a `for` loop + comments that document process and explain your code.

Your output should similar to the following:
```
10
9
8
7
6
5
4
3
2
1
Blastoff!
```

Q17: Write a program that asks the user to enter three numbers: a starting value, an ending value, and an increment. Your program should then "count" based on these criteria, as shown in the sample output below. Answer to this question includes programs with a `while` loop and a `for` loop + comments that document process and explain your code.

```
This program counts for you.
Enter the starting value: 3
Enter the ending value: 13
Enter the increment: 2
3
5
7
9
11
13
```

Q18: Write a program that prints the numbers 1 through 10, except that between 7 and 8 it should print the word "happy." Answer to this question includes programs with a `while` loop and a `for` loop + comments that document process and explain your code.

Sample output for this program:
```
1
2
3
4
5
6
7
happy
8
9
10
```

HINT: How could an `if` statement be helpful to achieve this output? 

# Lab Notebook Questions (for this section)

Q11: Write a program that asks a user to enter a color value and returns an output message comparing that value with your favorite color. This program will use a combination of the `input()` function, comparison operators, and `if-then-else` logic. Answer to this question includes program + comments that document process and explain your code.

Sample output for this program:
```
Your favorite color: green

My age: blue

We don't have the same favorite color.
```

Q12: Write a program that lets the user play a guessing game.
- First, your program should set a number as the "correct answer"
- Then, your program will ask the user to guess a number
- Your program should give a message indicating whether the user's guess is correct, too high, or too low

This program will use a combination of the `input()` function, comparison operators, and `if-then-else` logic. Answer to this question includes program + comments that document process and explain your code.

Sample output for this program (for a correct answer of 7:
```
You guessed 13.
```

Q13: Given the following program:

```Python
# assign count variable
count = 1

# while loop
while count <= 5: # initial condition
   print ("Python") # print statement
   count = count + 1 # reassign count

# final print statement
print ("Done")
```

How would you modify the program to print or output the string nine (9) times and also include line numbers as part of the output? Answer to this question includes program + comments that document process and explain your code.

For example, your output might look like the following: 

```
1 Python
2 Python
3 Python
4 Python
5 Python 
6 Python
7 Python
8 Python
9 Python
IS FUN!
```

Q14: Let's return to the program we modified for Q13. How would you modify your Q13 answer to use a `for` loop instead of a `while` loop? Answer to this question includes program + comments that document process and explain your code.

```Python
# assign count variable
count = 1

# while loop
while count <= 5: # initial condition
   print ("Python") # print statement
   count = count + 1 # reassign count

# final print statement
print ("Done")
```

As a reminder, your output might look like the following: 

```
1 Python
2 Python
3 Python
4 Python
5 Python 
6 Python
7 Python
8 Python
9 Python
IS FUN!
```

Q15: In a previous program, you were asked to modify the program below to search for the characters `q` and `u` in the string `turquoise`. 

Program you modified:
```Python
# assign string variable
color = "turquoise"

# get index number of t character
index_number = color.index("t")

# show index number as part of print statement
print ("The index number for the letter t within the word " + color + " is " + index_number)
```

Write a program that uses a `for` loop to return all instances of `q` and `u` in the string, not just the first occurrence. Answer to this question includes program + comments that document process and explain your code.

NOTE: For the following lab notebook questions, write two programs for each- one that uses a `while` loop and one that uses a `for` loop to accomplish the same task. 

Q16: Write a program that counts from 10 down to 1, and then prints "Blastoff!" Answer to this question includes programs with a `while` loop and a `for` loop + comments that document process and explain your code.

Your output should similar to the following:
```
10
9
8
7
6
5
4
3
2
1
Blastoff!
```

Q17: Write a program that asks the user to enter three numbers: a starting value, an ending value, and an increment. Your program should then "count" based on these criteria, as shown in the sample output below. Answer to this question includes programs with a `while` loop and a `for` loop + comments that document process and explain your code.

```
This program counts for you.
Enter the starting value: 3
Enter the ending value: 13
Enter the increment: 2
3
5
7
9
11
13
```

Q18: Write a program that prints the numbers 1 through 10, except that between 7 and 8 it should print the word "happy." Answer to this question includes programs with a `while` loop and a `for` loop + comments that document process and explain your code.

Sample output for this program:
```
1
2
3
4
5
6
7
happy
8
9
10
```

HINT: How could an `if` statement be helpful to achieve this output? 
