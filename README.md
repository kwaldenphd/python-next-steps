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

This second part of this lab provides an overview of foundational programming concepts in the areas of control flow and functions, with a focus on Python syntax. Topics covered include:
- Control flow and control structures
- Event-controlled and count-controlled loops
- Looping structures in Python (`for` and `while`)

This last section of this lab provides an overview of foundational programming concepts in the areas of control flow and functions, with a focus on Python syntax. Topics covered include:
- Control flow and control structures
- Code modularity and reuse
- Built-in functions in Python
- Named functions in Python
- Core function components, including definition, arguments, parameters, scoping, and docstrings

## Acknowledgements

[Click here](https://github.com/kwaldenphd/python-next-steps/blob/main/acknowledgements.md) for a full list of acknowledgements for this lab. 

# Table of Contents
- [Key Concepts](#key-concepts)
- [Lab Notebook Template](#lab-notebook-template)
- [Part I: Secondary Data Structures](#part-i-secondary-data-structures)
- [Part II: Control Structures, Iteration & Loops](#part-ii-control-structures-iteration--loops)
- [Part III: Functions](#part-iii-functions)
- [How to Submit This Lab (and show your work)](#how-to-submit-this-lab-and-show-your-work)
- [Lab Notebook Questions](#lab-notebook-questions)

# Key Concepts
- [Part I key concepts](https://github.com/kwaldenphd/python-next-steps/blob/main/part-i-key-concepts.md)
- [Part II key concepts](https://github.com/kwaldenphd/python-next-steps/blob/main/part-ii-key-concepts.md)
- [Part III key concepts](https://github.com/kwaldenphd/python-next-steps/blob/main/part-iii-key-concepts.md)

# Lab Notebook Template

[Click here](https://replit.com/team/eoc-f23/Python-Next-Steps) to make a copy of the Replit template for this lab.

Alternatives:
- [`.py` template](https://drive.google.com/file/d/1OWt8cBbLlr88eQkH8nrSE-RytluwjHbo/view?usp=sharing) (Google Drive, ND users)
- [Jupyter Notebook, `.ipynb`](https://colab.research.google.com/drive/1SG3C4QJNOMqpWmaAqDUpaWYl_hPyFpsm?usp=sharing) (Google Colab, ND users)

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

# Part II: Control Structures, Iteration & Loops

From Busbee and Braunschweig's "[Structured Programming](https://press.rebus.community/programmingfundamentals/chapter/structured-programming/)" from *Programming Fundamentals*
    
"One of the most important concepts of programming is the ability to control a program so that different lines of code are executed or that some lines of code are executed many times. The mechanisms that allow us to control the flow of execution are called control structures. Flowcharting is a method of documenting (charting) the flow (or paths) that a program would execute. There are three main categories of control structures:"
  * Sequence [executes in given sequence]
  * Selection [selects between two or more flows using condition or question]
  * Iteration [repeats same piece of code multiple times]
  
We're going to spend multiple labs thinking through control structures and control flow, with a focus on how we use them in Python.
    
Examples of control structures in Python include:
- `if-then-else` (syntax: `if`, `else`, `elif`)
- `while` statements (syntax: `while`)

[Click here](https://github.com/kwaldenphd/python-next-steps/blob/main/part-ii.md) to access this section of the lab.

# Part III: Functions

We've previously been introduced to the concept of **code blocks**. From Busbee and Braunschweig's "[Code Blocks](https://press.rebus.community/programmingfundamentals/chapter/code-blocks/)" from *Programming Fundamentals*:
- "A code block, sometimes referred to as a compound statement, is a lexical structure of source code which is grouped together. Blocks consist of one or more declarations and statements. A programming language that permits the creation of blocks, including blocks nested within other blocks, is called a block-structured programming language. Blocks are fundamental to structured programming, where control structures are formed from blocks."
   
Approaching a program as a series of components that each accomplish tasks that are part of the larger workflow gets us to a new concept: **modularity** or **modular programming**

From Busbee and Braunschweig's "[Modular Programming](https://press.rebus.community/programmingfundamentals/chapter/modular-programming/)," in *Programming Fundamentals*:
- "Modular programming is a software design technique that emphasizes separating the functionality of a program into independent, interchangeable modules, such that each contains everything necessary to execute only one aspect of the desired functionality."

Code blocks are one way to think about these discrete parts of a program. A more precise term used in programming languages is **function.** "Functions are important because they allow us to take large complicated programs and to divide them into smaller manageable pieces. Because the function is a smaller piece of the overall program, we can concentrate on what we want it to do and test it to make sure it works properly" (Busbee and Braunschweig, [Modular Programming](https://press.rebus.community/programmingfundamentals/chapter/modular-programming/)).

[Click here](https://github.com/kwaldenphd/python-next-steps/blob/main/part-iii.md) to access this section of the lab.

## How to submit this lab (and show your work)

Moving forward, we'll submit lab notebooks as `.py` files. 

One option is to have a `.py` file that you use to run code and test programs while working through the lab. When ready to submit the lab notebook, you add comments and remove extraneous materials.

Another option is to have an "official" `.py` file that you are using as a lab notebook (separate from your working/testing file). Use comments in Python to note when you are starting a new question (as well as answering a question).
  * Example: `Lab_Notebook_Walden.py`

What gets submitted as the lab notebook is the `Lab_Notebook_Walden.py` file.
- When in doubt, use comments
- Be sure you are using comments to note what question you're responding to

# Lab Notebook Questions

[Click here](https://replit.com/team/eoc-f23/Python-Next-Steps) to make a copy of the Replit template for this lab.

Alternatives:
- [`.py` template](https://drive.google.com/file/d/1OWt8cBbLlr88eQkH8nrSE-RytluwjHbo/view?usp=sharing) (Google Drive, ND users)
- [Jupyter Notebook, `.ipynb`](https://colab.research.google.com/drive/1SG3C4QJNOMqpWmaAqDUpaWYl_hPyFpsm?usp=sharing) (Google Colab, ND users)

## Part I Questions (secondary data structures)

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

## Part II Questions (control flow, iteration & loops)

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

## Part III Questions (functions)

Q19A: Describe how you would start building out a program to accomplish this task (print a string a specific number of times)? What functions, statements, or keywords would you need to use? How would you start to organize this program?

Q19B: See where you can get with writing this program. What parts of the program were you able to get working? Where did you run into challenges? Answer to this question includes program + comments that document process and explain your code.

Q19C: How does the sample program compare to your approach? What was similar? What was different? How are you thinking differently (if at all) about how to approach this type of program?

Q20A: Modify the program you built for the previous section of the lab to take specific values as inputs (rather than get inputs as part of the function). Answer to this question includes program + comments that document process and explain your code.

Q20B: Then, create a named function and function call for this program. Answer to this question includes program + comments that document process and explain your code.

Q20C: What parts of the program were you able to get working? Where did you run into challenges?

Q21: Write a function is_even that determines whether or not a number n is even. Include the function definition as well as a sample function call. Answer to this question includes program + comments that document process and explain your code.

Q22: Write a function average that determines the average value of a list. Include the function definition as well as a sample function call. Answer to this question includes program + comments that document process and explain your code.

Q23: Write a function uniq that takes a list and returns a new list containing only unique values. Include the function definition as well as a sample function call. Answer to this question includes program + comments that document process and explain your code.
