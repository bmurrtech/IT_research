### **Any and all copyright materials used are for educational, non-commercial, illustrative (research, criticism, & comment), unpublished purposes only. Facts themselves are not copyrightable.**

### **Any other works of mine are under the Attribution NonCommercial ShareAlike 4.0 International license.**

Shield: [![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg
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

# Expressions and Variables

#### Data Types
The text between "" is known as a __string__

```py
print ("Hollow world...")
```

In the example above the string would be: "Hollow world..."

A string is as known as a "_data type_". A data type could be defined as: classes of data (e.g., string, int, float, Boolean, etc.), which include the properties and behaviors of instances of the data type (variables).

 Data types include:
 - __integer__ which represents whole numbers __without__ a fraction. Ex. 1, 7, 342 are all integers.
 - __float__, which represents real numbers or in other words, a number __with a fractional part__ like 2.5. Ex. 5.3, 3.14159 and 6.0 are all floats.
 -  An integer is a whole number, without a fraction, while a float is a real number that can contain a fractional part.

If you mix _data types_, you will get a _syntax error_. For example:

 ```py
print (7 + "8")
 ```

 You will get an error like this:

 ```py
TypeError: unsupported call last): 1, in <module> operand type(s) for +: 'int' and 'str'
 ```
In this case, an _integer_ has been mixed with a _string_. It's like telling a human to add a the letter A with the number 12. It does not compute; it's a syntax error.

> Tip: You can always check the _data type_ by using the `type ()` function, see below:

```py
print(type(2.3))
print (type(5))
```

This code will return the following data:

```py
<class 'float'>
<class 'int'>
```

> Note: Integers and floats are compatiable. For example: `print(7+5.2)` will work but that is only because Python converts the integer into a float. This process is known as __implicit conversion__. See more about this below.

#### Variables

__Variables__ are names that we give to certain values in our programs. Think of variables as _containers for data_. 

```py
base = 5
height = 3
area = base * height/2

print(area)
```
In the above example, "base = 5" is a _variable_. The formular of creating a variable is __variable = value__.

Generally, you can name variables whatever you like but there are some restrictions.
 - Don't use keywords or functions that Python
reserves for its own (like print).
- Don't use spaces.
- Must start with a letter or an underscore (_)
- Must be made up of only letters, numbers,
and underscores (_)

| Variable | Valid/Invalid |
| ----------- | ----------- |
| i_am_a_variable | valid
| i_am_a_variable2 | valid |
| 1_is_a_number | invalid b/c variables must start with an underscore or letter |
| apples_&_oranges | invalid b/c special character is used |

__Remebmer that__:
- Capitalization matters:
  - name
  - NAME
  - Name
- These all are valid and qualify as _different_ and unique variable names.

__Assignment__ is the process of storing a value inside a variable.

__Expression__ is a combination of numbers, symbols or other variables that produce a result when evaluated.

A use case of variables in action in automation for IT would be:
- Say we have a script that performs a specific operation on a file.
- We can extend that script to perform the same operation on any file _but only if the program used a variable_ to store the file name.

#### Expressions, Numbers, and Type Conversions

__Implicit Conversion__ automatically converts one data type into another.

__Explicit Conversion__ is the manual conversion of one data type into another.

Explicit conversion code includes:
- `str()` - converts a value (often numeric) to a string data type
- `int()` - converts a value (usually a float) to an integer data type
- `float()` - converts a value (usually an integer) to a float data type 

We can utilize the `str()` function to explicitly convert the variable and make the print function compatiably work. For example:

```py
total = 2048 + 4357 + 97658 + 125 + 8
files = 5
average = total / files
print("The average size is:" + str(average))
```

##### Example Code:

```py
# The following lines assign the variable to the left of the = 
# assignment operator with the values and arithmetic expressions 
# on the right side of the = assignment operator.
hotel_room = 100
tax = hotel_room * 0.08
total = hotel_room + tax
room_guests = 4
share_per_person = total/room_guests 
 
# This line outputs the result of the final calculation stored
# in the variable "share_per_person"
print("Each person needs to pay: " + str(share_per_person)) # change a data type
```

```py
# The following 5 lines assign strings to a list of variables.
salutation = "Dr."
first_name = "Prisha"
middle_name = "Jai"
last_name = "Agarwal"
suffix = "Ph.D."
 
print(salutation + " " + first_name + " " + middle_name + " " + last_name + ", " + suffix) 
# The comma as a string ", " adds the conventional use of a comma plus a 
# space to separate the last name from the suffix.
 
# Alternatively, you could use commas in place of the + connector:
print(salutation, first_name, middle_name, last_name,",", suffix)
# However, you will find that this produces a space before a comma within a string.
```

```py
print("5 * 3 = " + (5*3)) 
 
# Resolution: 
# print("5 * 3 = " + str(5*3))
#
# To avoid a type error between the string and the integer within the
# print() function, you can make an explicit data type conversion by
# using the str() function to convert the integer to a string.
```

```py
numerator = 7
denominator = 0   # Possible resolution: Change the denominator value 
result = numerator / denominator
print(result)
 
# One possible assumption for a number divided by zero error might
# include the issue of a null value as a denominator (could happen when
# using a loop to iterate over values in a database). In such cases, the
# desired outcome may be to leave the numerator value intact. The
# numerator value can be preserved by reassigning the denominator with 
# the integer value of 1. The result would then equal the numerator.
```


# Expressions and Variables Functions

#### Defining Functions

```py
def greeting(name, department):
    print("Welcome, " + name)
    print("You are part of " + department)

    return = greeting("Ben" + "the NOC Team")
```


- To define a function, we use the def keyword. In this example, the __function's name__ is _greeting_. 

- After the name, we have the __parameters__ of the function which are written between parentheses. In this example, we only have two __parameters__, name and department, followed by a colon at the end of the line.

- After the colon, we have the __body__ of the function. That's _where we state what we want our function to do_.  he body of a function can have as many lines as we want.

- Note how the body is indented to the right. _We can add as many lines as we'd like_ to the body of the function but each line must be indented the same number of spaces to the right. We could use two or eight or any other number _as long as they're all consistent_.

```py
def area_triangle(base, height):
    return base*height/2

area_a = area_triangle(5,4)
area_b = area_triangle(7,3)
sum = area_a + area_b
print ("The sum of both areas is: " + str(sum))
```

__None__ is a very special data type in Python used to indicate that things are empty or that they return nothing. Wow. That was a lot to learn about functions and the return values. 

Code: You only have a duration in seconds, and you wish to convert to hours and mintues.
```py
def convert_seconds(seconds):
    hours = seconds // 3600
    minutes = (seconds - hours * 3600) // 60
    remaining_seconds = seconds - hours * 3600 - minutes * 60
    return hours, minutes, remaining_seconds

hours, minutes, seconds = convert_seconds(5000)
print(hours, minutes, seconds)
```

- That __double slash__ operator ( // ) is called __floor division__. A floor division divides a number and takes the integer part of the division as the result. For example, five slash slash two is two instead of 2.5 (5 / 2 = 2.5, but 5 // 2 = 2 because it is the integer value not the float value.)
- In the above seconds converter code, the first operation is calculating how many hours are in a given amount of seconds.

#### Return Value

Sometimes we don't want a function to simply run and finish. We may want a function to manipulate data we passed it and then return the result to us. This is where the concept of return values comes in handy. We use the return keyword in a function, which tells the function to pass data back. When we call the function, we can store the returned value in a variable. Return values allow our functions to be more flexible and powerful, so they can be reused and called multiple times.

Functions can even return multiple values. Just don't forget to store all returned values in variables! You could also have a function return nothing, in which case the function simply exits.

#### Princples of Code Reuse


```py
name = "Kay"
number = len(name) * 9

print ("Hello " + name + ". Your luck number is " + str(number))

name = "Cameron"
number = len(name) * 9

print ("Hello " + name + Your lucky number is + str(number))
```

_When you find code __duplication__ in your scripts_, it's a good idea to check if you can clean things up a bit by using a function. For exemple:

```py
def lucky_number(name):
    number = ten(name) * 9
    print ("Hello " + name + ". Your lucky number is " + str(number))
lucky_number("Kay")
lucky_number("Cameron)
```

First, we've defined a __function__ called lucky number, which carries out our calculation and prints it for us. Then we call the function twice, once with each name. Since we've grouped the calculation and print statements into a function, our code is not only easier to read but it's also now reusable. We can execute the code inside the lucky number function as many times as we need it, by just calling it with a different name. So we don't have to write it out again and again for each new name.

#### Code Style

__Self-documenting code__ is written in a way that's readable and doesn't conceal its intent. This principle can be applied to all aspects of writing code from picking your variable names to writing clear concise expressions.

Bad Example:
```py
def calculate(d):
    q = 3.14
    z = q * (d ** 2)
    print(z)
calculate(5)
```

Better Example (__Refactoring__):

```py
def circle_area(radius)
    pi = 3.14
    area = pi * (radious ** 2)
    print(area)
circle_area(5)
```
Which code is easier to understand? If you want to add more clarity, you can add a __comment__.

```py
def circle_area(radius)
    pi = 3.14

# Pi is caclucated by the float 3.14
    area = pi * (radious ** 2)
    print(area)
circle_area(5)
```
