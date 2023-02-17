
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

### Introduction to Programming | Key Terms
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

Python isn't new. Its first version was released by __Guido van Rossum back in 1991__. Since then, the community that develops it has grown and the language has advanced a lot. Whenever there's a significant change to the semantics or syntax of the language, a new major version is released. In 2000, Python 2 was released. In 2008, we got Python 3.

#### Why pick Python?

Well, we chose Python for a few reasons. First off, programming in Python usually feels similar to using a human language.

You can use Python to:
- calculate statistics,
- run your e-commerce site,
- process images,
- interact with web services...

_Python is perfect for automation_. It lets you automate everyday tasks by writing simple scripts that are easy to understand and easy to maintain. That's why Python is the language of choice for lots of people working in IT support.

- Python is:
  - a general purpose scripting language;
  - a popular language used to code a variety of applications;
  - a frequently used tool for automation;
  - a cross-platform compatible language;
  - a beginner-friendly language.

- Python is not: 
  - a platform-specific / OS-specific scripting language;
  - a client-side scripting language;
  - a purely object-oriented programming language.

#### Glimpse of Python Code

```py
print ("Hello world~")
```

```py
# Syntax for printing a string of text
print("I love Python!")

# Syntax for printing numeric values
print(360)
print(32*45)

# Syntax for printing the value of a variable
value = 8*6
print(value)
```

```python
friends = ['Taylor', 'Alex ' , 'Pat', 'Eli']
for friend in friends:
    print ("Hi" + friend)
```

##### Getting Info from Input

```python
name = "Brook"
    print ("Hello " + name)
```
##### Python Calculator

```python
print (4+5)
print (9*7)
print (-1/4)
print (1/3)
print (((2050/5)-32)/9)
print (2**10)
```

#### Similarites of Coding Languages

Python :

```python
for i in range(l0):
        print ("Hello World!")
```

Bash:

```bash
for i in {1..10}; do
    echo Hello, World!
done
```

PowerShell:
```ps
for ($1=1; $1 -le 10; $i++) {
Write-Host "Hello, World! "
```

Similarity breakdown:
* Each language must somehow put text on the screen
    * Python `print`
    * Bash: `echo`
    * PowerShell `Write-Host`
* Counting mechaninism (counting to 10):
  * Python specifies the range
  * Bash uses a seqence notation to count from 1 to 10
  * PS has the most complex syntax, but it, like Bash, starts at 1 and counts up to 10.

- __Python interpreter__ In programming, an interpreter is the program that reads and executes code.

> Remember how we said a computer program is like a recipe with step-by-step instructions? Well, if your recipe is written in Python, the Python interpreter is the program that reads what is in the recipe and translates it into instructions for your computer to follow.

### Getting Hands-on with Python

- You can execute the interpreter by running the python3 command (or just python on Windows), and you can close it by typing `exit()` or `CTRL + D`.

##### Python Practice Resources

- [Welcome to Python](https://www.python.org/shell/)

- [Online Python Interpreter](https://www.onlinegdb.com/online_python_interpreter)

- [Create a New Repl](https://repl.it/languages/python3)

- [Online Python-3 Compiler](https://www.tutorialspoint.com/execute_python3_online.php)

- [Compile Python 3 Online](https://rextester.com/l/python3_online_compiler)

- [Your Python Trinket](https://trinket.io/python3)

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

### Key Terms for Intro to Python

- Platform-specific / OS specific scripting language - Platform-specific scripting languages, like PowerShell (for Windows) and Bash (for Linux), are used by system administrators on those platforms. 

- Client-side scripting language - Client-side scripting languages, like JavaScript, are used mostly for web programming. The scripts are transferred from a web server to the end-user’s internet browser, then executed in the browser.

- Machine language - Machine language is the lowest-level computer language. It communicates directly with computing machines in binary code (ones and zeros). In binary code, one equals a pulse of electricity and zero equals no electrical pulse. Machine language instructions are made from translating languages like Python into complex patterns of ones and zeros. 

- Cross-platform language - Programming language that is compatible with one or more platforms / operating systems (e.g., Windows, Linux, Mac, iOS, Android).

- Object-oriented programming language - In object-oriented programming languages, most coding elements are considered to be objects with configurable properties. For example, a form field is an object that can be configured to accept only dates as input in the mm/dd/yy format, and can be configured to read from and write to a specific database. 

- Python interpreter - An interpreter is the program that reads and executes Python code by translating Python code into computer instructions.

# First Programing Concepts

A __function__ _is a piece of code that performs a unit of work_. In the examples you've seen so far, you have only encountered the print() function, which outputs a message to the screen.

```py
# Syntax for printing a string of text. Click Run to check the result.
print("Hello world!")
```

A keyword is a reserved word in a programming language that performs a specific purpose. In your first Python example, you briefly encountered the keywords for and in.  Note that keywords will often appear in bold in this course.

Examples are:

- Values: __True, False, None__
- Conditions: __if, elif, else__
- Logical __operators: and, or, not__
- Loops: __for, in, while, break, continue__
- Functions: __def, return__

#### Arithmetic operators
Python can calculate numbers using common mathematical operators.

Example:
```py
# Assignment of values to the variables:
years = 10
weeks_in_a_year = 52
# This variable is assigned an arithmetic calculation:
weeks_in_a_decade = years * weeks_in_a_year
# Prints the calculation stored in the "weeks_in_a_decade" variable:
print(weeks_in_a_decade)
```

```py
days = 365
hours = 24
min = 60
min_in_year = days * hours * min
print(min_in_year)
```

There are some special operators, too:  

| Syntax | Description |
| ----------- | ----------- |
| x + y  | Addition + operator returns the sum of x  |
| x - y  | Subtraction - operator returns the difference of x minus y |
| x * y  | Multiplication * operator returns the product of x times y |
| x / y  | Division / operator returns the quotient of x divided by y |
| x**e  | Exponent ** operator returns the result of raising x to the power of e  |
| x**2 | Square expression returns x squared
 |
| x**3 | Cube expression returns x cubed |
| x**(1/2) | Square root (½) or (0.5) fractional exponent operator returns the square root of x |
| x // y  | Floor division operator returns the integer part of the integer division of x by y |
| x % y | Modulo operator returns the remainder part of the integer division of x by y |

```py
# Multiplication, division, addition, and subtraction
print(3*8/2+5-1)
 
# Exponents
print(4**6) # Syntax means 4 to the power of 6
print(4**2) # To square a number
print(4**3) # To cube a number
print(4**0.5) # To find the square root of a number

# To calculate how many different possible combinations can be
# formed using a set of "x" characters with each character in "x"
# having "y" number of possible values, you will need to use an 
# exponent for the calculation:
x = 4
y = 26
print(y**x)
```

#### Order of Operations

1. __P__arentheses ( ), { }, [ ]
1. __E__xponents x^e^ (x**e)
1. __M__ultiplication * and __D__ivision /  
1. __A__ddition + and __S__ubtraction -

You might find the __PEMDAS__ mnemonic device to be helpful in remembering the order.

For more information about the concepts covered in this reading, please visit:

[Built-in Functions](https://docs.python.org/3/library/functions.html) - Lists and summarizes Python’s built-in functions.

[Python Keywords](https://www.w3schools.com/python/python_ref_keywords.asp) - Lists Python’s reserved keywords and a brief description of what each keyword does.

[Different Arithmetic](https://flexiple.com/python/arithmetic-operators-in-python/) operators in Python - Provides more examples of the proper syntax for using arithmetic operators in Python.
          