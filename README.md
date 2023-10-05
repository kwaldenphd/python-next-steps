# Python Next Steps (secondary data structures, conditional statements, iteration/loops, functions)

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>This tutorial was written by Katherine Walden and is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

## Lab Overview & Goals

This first part of this lab provides an overview of foundational programming concepts in the areas of data structures and data storage, with a focus on Python syntax. Topics covered include:
- Linear and associative arrays
- Indexing
- String objects and methods
- Lists and list methods
- Dictionaries
- Tuples
- Sets

This later parts of this lab provides an overview of foundational programming concepts in the areas of control flow and functions, with a focus on Python syntax. Topics covered include:
- Control flow and control structures
- Event-controlled and count-controlled loops
- Looping structures in Python (`for` and `while`)

## Acknowledgements

[Click here](https://github.com/kwaldenphd/python-next-steps/blob/main/acknowledgements.md) for a full list of acknowledgements for this lab. 

# Table of Contents
- [Key Concepts](#key-concepts)
- [Lab Notebook Template](#lab-notebook-template)
- [Part I: Secondary Data Structures](#part-i-secondary-data-structures)
- [Part II: Control Structures](#part-ii-control-structures)
- [Part III: Iteration & Loops](#part-iii-iteration-loops)
- [Lab Notebook Questions](#lab-notebook-questions)

# Key Concepts

[Click here](https://github.com/kwaldenphd/python-next-steps/blob/main/key-concepts.md) for a full list of key concepts and definitions for this lab.

# Lab Notebook Template

[Click here]() to make a copy of the Replit template for this lab.

Alternatives:
- [`.py` template]() (Google Drive, ND users)
- [Jupyter Notebook, `.ipynb`]() (Google Colab, ND users)

# Part I: Secondary Data Structures

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

[Click here](https://github.com/kwaldenphd/python-next-steps/blob/main/part-i.md) to access this section of the lab.

# Part II: Control Structures

From Busbee and Braunschweig's "[Structured Programming](https://press.rebus.community/programmingfundamentals/chapter/structured-programming/)" from *Programming Fundamentals*
    
"One of the most important concepts of programming is the ability to control a program so that different lines of code are executed or that some lines of code are executed many times. The mechanisms that allow us to control the flow of execution are called control structures. Flowcharting is a method of documenting (charting) the flow (or paths) that a program would execute. There are three main categories of control structures:"
  * Sequence [executes in given sequence]
  * Selection [selects between two or more flows using condition or question]
  * Iteration [repeats same piece of code multiple times]
  
We're going to spend multiple labs thinking through control structures and control flow, with a focus on how we use them in Python.
    
Examples of control structures in Python include:
- `if-then-else` (syntax: `if`, `else`, `elif`)
- `while` statements (syntax: `while`)

[Click here](https://github.com/kwaldenphd/python-next-steps/tree/main) to access this section of the lab.

# Part III: Iteration & Loops


