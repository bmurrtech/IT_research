
# Intro to Programing

#### What is Programing
- Programming languages are actually similar to humans spoken languages since they have a __syntax__ and __semantics__. 
 - In a human language, __syntax__ is the _rules for how a sentence is constructed_ while __semantics__ refers to _the actual meaning of the statements_.
 - __Syntax__ _is the rules for how each instruction is written_
 - __Semantics__ _is the effects the instructions have_.

 > In English, sentences generally have both a
 > subject, that's a person, place, or thing and a
 > predicate usually a verb and a statement that
 > explains what the subject is doing.

#### What is Automation
 - __Script/Program__  is a short development cycle that can be created and deployed rapidly. In other words, a script is a program that is short, simple, and can be written very quickly.
 - __Automation__ is the process of replacing a manual step with one that happens automatically
   - Sometimes automation is not always the best solution. In scenarios requiring more complex, creative, or difficult tasks or when performing less frequently executed tasks, _automation may actually be more effort or cost than it's worth._
   - However, automation is still a powerful tool when used in the _right place at the right moment_. It can save time, reduce errors, increase consistency, and provide a way to centralize solutions and mistakes, making them easier to fix.

> It is important to understand that basic automation is _not_ the same as __artificial intelligence__. Automation is used to explicitly instruct a machine on how to perform a task. Artificial intelligence (AI) involves training a computing machine to perform more complex tasks through a process called machine learning.

#### Getting Computers to Work for You (When to Automate)

- When repetitive or accident-prone task are, automation should be considered. For example, you could write a program that checks for duplicates and add data to a list.
- Automation examples are:
  - Periodically scanning the disk usage of a group of fileservers.
  - Installing software on laptops given to new employees when they are hired.
  - A script that changes a bunch of access permissions.
  - A script that traverses a large directory tree with many different files, checks the file contents, and then updated the permissions to the services based on the conditions.

- But automating tasks requiring any kind of:
    - creative thinking
    - investigation
    - or designing is not.

### Introdcution to Programming | Key Terms
- Programming code - Programming code is a set of written computer instructions, guided by rules, using a computer programming language. It might help to think of the computer instructions as a detailed, step-by-step recipe for performing tasks. The instructions tell computers and machines how to perform an action. Programming code may also be referred to as source code or scripts.

- Programming languages - Programming languages are similar to human spoken languages in that they both use syntax and semantics. Programming languages are used to write computer programs.  Some common programming languages include Python, Java, C, C++, C#, and R.

- Syntax - Syntax is a set of rules for how statements are constructed in both human and computer languages. Programming syntax includes rules for the order of elements in programming instructions, as well as the use of special characters and their placements in statements. This concept is similar to the syntax rules for grammar and punctuation in human language.

- Semantics - Semantics refers to the intended meaning or effect of statements, or collections of words, in both human and computer languages. Semantic errors are also referred to as logical errors.

- Computer program - A computer program is a step-by-step list of instructions that a computer follows to reach an intended goal. It is important to be clear and precise about the actions a computer program is supposed to perform because computers will do exactly what they are instructed to do. Computer programs can be long, complex, and accomplish a variety of tasks. They are often developed by computer programmers and software engineers, but anyone can learn to create them. Computer programs may involve a structured development cycle. They can be written in a wide variety of programming languages, such as Python, Java, C++,  R, and more. The completed format of a program is often a single executable file.

- Script - Scripts are usually shorter and less complex than computer programs. Scripts are often used to automate specific tasks. However, they can be used for complex tasks if needed. Scripts are often written by IT professionals, but anyone can learn to write scripts. Scripts have a shorter, less structured development cycle as compared to the development of complex computer programs and software. Scripts can be written in a variety of programming languages, like Python, Javascript, Ruby, Bash, and more. Some scripting languages are interpreted languages and are only compatible with certain platforms.

- Automation - Automation is used to replace a repetitive manual step with one that happens automatically. 

- Output - Output is the end result of a task performed by a function or computer program. Output can include a single value, a report, entries into a database, and more. 

- Input - Input is information that is provided to a program by the end user. Input can be text, voice, images, biometrics, and more.   

- Functions - A function is a reusable block of code that performs a specific task.

- Variables - Variables are used to temporarily store changeable values in programming code.

# Introduction to Python

Why pick Python? Well, we chose Python for a few reasons. First off, programming in Python usually feels similar to using a human language.

```python
friends = ['Taylor', 'Alex ' , 'Pat', 'Eli']
for friend in friends:
    print ("Hi" + friend)
```
- __Python interpreter__ In programming, an interpreter is the program that reads and executes code.

> Remember how we said a computer program is like a recipe with step-by-step instructions? Well, if your recipe is written in Python, the Python interpreter is the program that reads what is in the recipe and translates it into instructions for your computer to follow.

#### Getting Hands-on with Python

- You can execute the interpreter by running the python3 command (or just python on Windows), and you can close it by typing exit() or Ctrl-D.

##### Python Practice Resources

- https://www.python.org/shell/

- https://www.onlinegdb.com/online_python_interpreter

- https://repl.it/languages/python3

- https://www.tutorialspoint.com/execute_python3_online.php

- https://rextester.com/l/python3_online_compiler

- https://trinket.io/python3

Read the [official Python documentation](https://docs.python.org/3/).

##### Other Python Resources

- Search for answers or ask a question on [Stack Overflow](https://stackoverflow.com/). 

- Subscribe to the [Python tutor mailing list](https://mail.python.org/mailman/listinfo/tutor), where you can ask questions and collaborate with other Python learners.

- Subscribe to the [Python-announce mailing list](https://mail.python.org/mailman/listinfo/python-announce-list) to read about the latest updates in the language.

- You can read more about it on the [History of Python](https://en.wikipedia.org/wiki/History_of_Python) Wikipedia page.

### Syntax Errors and Code Blocks
Common Syntax errors:

- Misspellings
- Incorrect indentations
- Missing or incorrect key characters:
  - Bracket types - ( curved ), [ square ], { curly } 
   - Quote types - "straight-double" or 'straight-single', “curly-double” or ‘curly-single’
   - Block introduction characters, like colons - :
- Data type mismatches
- Missing, incorrectly used, or misplaced Python reserved words
- Using the wrong case (uppercase/lowercase) - Python is a case-sensitive language 

If your syntax is correct, but the script has unexpected behavior or output, this may be due to a semantic problem. Syntax is like the vocabulary, grammar, spelling, and punctuation of code. Semantics are the meaning and logic of coded statements. It is possible to have syntactically correct code that runs successfully, but doesn't do what we want it to do.

Common semantic errors:
- Creating functional code, but getting unintentional output
- Poor logic structures in the design of the code

When working with the code blocks in exercises for this course, be mindful of syntax and semantic (logic) errors, along with the overall result of your code. Just because you fixed an error doesn't mean that the code will have the desired effect when it runs! Once you’ve fixed an error in your code, don't forget to click Run to check your work.
