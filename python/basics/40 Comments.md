## Comments

If a single file contains a sizable amount of Python-code, it is good practice to clearly denote *what is where* (for the reader of the code, not the user of the program). To that end you can add lines of commentary to your code. They look like this:

    # calculation
    x = x + 1

or

    # output
    print(x)

With a hashtag (`#`) you tell Python that it does not have to execute that line of code, but it is instead a comment. It is common practice to write a comment *above* the block of code it refers to.  By adding comments to your code, the code is easier to understand for you and possibly other people that use your code. 

Aside from a comment about small blocks of code throughout your program, it is also useful to describe the use of a program at the top of the file. For **exercise.py** the following **header comment** would suffice:

    # Exercise with Python Module 1
    # M. Stegeman
    # 24-8-2018

Now add comments to your file. Each time explaining a component of your program with a short descriptive text.