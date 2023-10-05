Python Next Steps Part II: Control Structures

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
- [Application(#application)

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

This guess is too high.

Better luck next time!
``` 
