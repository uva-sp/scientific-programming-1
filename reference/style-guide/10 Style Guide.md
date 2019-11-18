# Style Guide

Programming code is preferably easy to read and understand. Note only for yourself, but also for collaborators. In this course it is important to not only take the functionality of the code into account ("how do I write code to do something") but also the quality of the code ("is my code readable"). Earlier, we already mentioned some guidelines on how to comment code. Below you can find more aspects on how to comment your code properly.

## Terminology

To start, some terminology:

- We often talk about "programs". A *program* is an entity, a piece of software designed to execute a task or an action. Think about a calculator on your phone, or Microsoft Word. Python itself is also a program. In this course, you write a variety of programs yourself. 
- We also often talk about "code". A piece of *code* is a fragment, often a part of a program. The word code is not countable (i.e. you cannot talk about "one code" or "two codes"). You can say "my code doesn't work", in that case it is evident that you talk about the code you just have been working on.
- A program consists of "lines" of code.

## Choice of Language

In this course, we work in English. Make sure you work in one language only: variable names and comments should both be in English. 

## Comments

It is just as easy to write a lot of comments in your code as writing too little comments. To determine where comments are really needed, we should put ourselves in the reader of the code. This could be someone else, someone that uses your code to write a nice program. But, it could also be yourself, a few months later, desparately trying to decipher your own code. What information does this reader need?

- Summaries of blocks of code. Often you have divided your code in functional blocks. Sometimes only a few lines of code. It is ususally not difficult to summarize and describe the functionality of that piece of code. 
- Warnings for potential problems. Maybe you came up with a temporal solution to a problem, of which you know it will not work for some cases (but for now its fine). In that case, it is handy to document your doubts with in a comment.
- Explanation of complex algorithms. Sometimes you write very complex code. In that case you can give an explanation of the algorithm or provide a link for more information.
- Source references. To avoid plagiarism, it is of course important to mention all sources used when fully or partially using other people's code. Even if you change this person's code it is important to still refer to the source.

### Example 1

Comments are not always necessary. When variable names are very clear, and operations relatively simple, it might not be necessary to add a comment. Sometimes comments are still useful though:

    # calculate the average grade for this student 
    average = sum / assignment_count + 1

(We now know the average is the average grade of the student. Depending on the rest of the program this comment can be useful.)

#### Writing Style

Also pay attention to your writing style: do not use capital letters or dots in your comments. Add a space after the hash. Comments should be written directly *above* the line or block of code it is about.

### Example 2

Usually, at the top of programs some general information is provided. This part often contains the names of the authors and a summary of the goal of the program. 

    # Name: Jane Lee
    # Collaborators: John Doe
    #
    # This program calculates the average values of a series
    # of numbers input by the user.

#### Writing Style

Note the writing style in this example. The summary in the comment above is too long for one line. If that is the case, the comment should be divided over multiple lines explicitly. Just add another line with a `#` in front of it. 

We have chosen to truncate after 60 characters. Lines should have a length of approximately 45-90 characters, as is the case in books. This makes your code and comments easy to read.

## Indentation

Indentation is about adding whitespace at the start of a new line. In Python it is often necessary to start a rule with spaces, for example when defining a function:

    def sum(x, y):
        result = x + y
        return result

Beware! You can fill in the extra whitespace with tabs or spaces. In many cases a tab is visible as 8 spaces, but sometimes also as 4 or 2 spaces. However, this becomes a problem when tabs and spaces are used interchangeably, it is then unclear how the code should be executed.

    def sum(x, y):
        result = x + y     # 4 spaces
            return result  # 1 tab became 8 spaces here

The `return` is shown slightly more to the right, although only one tab is used. The result is that the code is less readable. In addition, Python will not be able to understand your code and error messages probably pop up. Be consequent in using spaces, or tabs to indent your code.

Oh, and as mentioned before, if a line ends with a colon (`:`), all lines below should be indented if they belong to the rule with the colon.  

    def sum(arrayOfNumbers):
        result = 0
        for number in arrayOfNumbers:
            result = result + number
        return result

Here you see that the line `result = result + number` belongs to the `for`-loop. The `return` does not belong to the `for` loop and therefore has less whitespace in front of it. 

## Naming Conventions

Many elements in your code, such as variables and functions, have a *name*. Here we give some guidelines for naming your variables and functions.

### Functions

Names of functions can be as long as you like, but keep it reasonable (and readable). In this case it is important that the goal of the function is described as clear and precise as possible.

    def user_average_this_year():
        ...

You can see there are multiple words in this function name, divided by an underscore (`_`). This is conventional in Python, all function names are written with multiple words divided by underscores and without capital letters.

### Variables

Preferably, names of variables are shorter, they are generally used more often. Think about a length on one to two words, a few examples:

    wall_height = 2.34
    earth_circumference = 40007.86
    total_rainfall = 823.3

Making abbreviations of words is often not preferred. By doing so, your code will be harder to read (a lazy programmer could abbreviate the above examples as `wh`, `ecirc` and `t_rain` , how can you find out afterwards what was meant here?)

There are exceptions. When your program is about topics where abbreviations are conventional. Physics and mathematics, for example.

    v_rabbit = 0.002            # v is for "velocity"
    x_rabbit = 23.11            # x is for "displacement"

Still, it can be observed that explanations still have to be added. Thus, avoid abbreviations unless it is evident what the abbreviation stands for.

## Blank Lines and Extra Spaces

As is the case in other media where text plays an important role, blank lines and whitespace can be used to improve readability.

### Blank Lines

As described in the "comments" section, you can divide your program in logical code blocks. This way, it is possible to describe the different steps of an algorithm. Here, a program is split in three major parts:

    number = input("Please enter a number: ")
    while number < 0:
        number = input("Please enter a *positive* number: ")
    
    # calculations: uses a complex loop to handle special cases
    while(number > 0):
        number -= 1
    if number == 0:
        number += 1
    
    # output: might not print zero (e.g., if user put in a float)
    print(user_input)

The three components are respectively: the user's input, the calculation and the output. You will encounter these components very often in programs. Also, pay attention to the instructions in the comments: first an explanation of the algorithm, and then a warning that that part of the code might not always work (and more important: when this happens!). 

### Spaces Around Operators

Operators such as `+`, `==`, `%` and `**` are often used in formulas and equations. Use spaces around operators, in order to keep formulas readable:

    i = i + 1
    submitted += 1
    x = x * 2 - 1
    hypotenuse_squared = x * x + y * y
    c = (a + b) * (a - b)
