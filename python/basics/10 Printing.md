## Printing

After writing a program you can then execute it (*running* it). The computer then reads your code, line for line, and executes any instructions it encounters.

Make a text file **exercise.py** (remember how?) and add the following lines to it:

    print("Hello, world!")
    print("Hee, hello there.")
    print("Making quick progress.")
    print("Funny")
    print('Hey, does this still print?')
    print("Ivo's computer does not work today.")
    print('He said: "Hello."')

> Practicing for this course can be done by literally copying examples word for word. Don't use the *copy-paste* function though, because that way you don't make any mistakes and you'll learn less. Type out all examples you see and fix your mistakes if you get an error message!

Now start the program you've just carefully copied, word for word:

    python exercise.py

What's the result? Did you make any mistakes? Any errors? And did you see that the quotation marks are sometimes different (single and double)? The sequence of characters that you type after `print` has to be started and ended by quotation marks (of the same kind!). Such a sequence is called a **string**.

We can also print multiple times on the same line. By default `print` adds an **ENTER** each time you use it, so that the following `print` statement continues on a new line. But you can manually prevent that **ENTER** from being added:

    print("The temperature is", end="")
    print(8, end="")
    print("degrees Celsius")

That way the entire message is printed on a single line. Try it for yourself!

This can also be achieved by adding multiple values to a single print statement:

    print("The temperature is", 8, "degrees Celsius")

See how each value (argument) is separated by a comma?

## Calculations

Next, add the following lines to your `exercise.py`:

    print(1)
    print(1 + 1)
    print(1 + 1 + 1)
    print(3 + 2)
    print(8)
    print(5 + 8 + 8 - 8)
    print("5 + 8 + 8 - 8")

You can also perform basic math. The *result* of the calculation is displayed on the screen. Except the last line: that one shows the formula (*expression*) between parentheses. Just like earlier with the texts. The expression within the brackets is a string and not a formula that can readily be calculated.

> Do you get an error message if you run the program? Chances are that you've made a mistake copying the commands leaving Python confused what you meant in the first place. Take a close look to find where you've made that mistake. If you can't seem to find it, do ask for some assistance. Learning to understand error messages is an important part of this course. That's why we want you to make a mistake every now and then!

## Operators

Below you'll find a list of mathematical operators you can use to compose formulas.

| operator | explanation               |
| -------- | ------------------------- |
| `1 + 2`  | addition                  |
| `2 - 1`  | subtraction               |
| `1 * 2`  | multiplication            |
| `2 / 1`  | division                  |
| `2 % 1`  | modulo (remainder)        |
| `2 ** 1` | exponentiation            |


Note: when two whole numbers are divided by using two `/`-operator, the result will always be a whole number. SO `3//2` won't be `1.5` but `1`. That is why the `%`-operator fits in so nicely; it gives the remainder after division.
