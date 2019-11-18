## Conditional Instructions

The preceding programs were scripts that were meant to be executed line for line from top to bottom. A sort of step by step guide. Programs get more interesting when we intend to write *exceptions*.

![embed](https://player.vimeo.com/video/287244672)

## Details

An `if`-statement in Python is structured as follows:

```
balance = 100
expense = 75
if balance - expense > 0:
    balance = balance - expense
    print("Transaction complete.")
print(f"Your balance is {balance}.")
```

A **condition** ultimately only has two possible outcomes. In Python these are `True` and `False` (these are called **boolean** values, after [George Boole](https://en.wikipedia.org/wiki/Boolean_algebra#Values)). In the code shown above the this boolean is the result of the expression `balance - expense > 0`. In this case the comparison operator `>` ('greater than') is used. This operator compares two parts, the first part is the result of `balance - expense` and the second part is `0`T. After which the result is evaluated into a boolean. Depending on the result, a `True` or `False` , the code within the if-statement is executed (the result was `True`) or skipped entirely (the result was `False`).

The `:` on the same line as the `if` signals that there's a **code block** that accompanies the `if`-statement. That's the particular part of code that is only executed if the condition is met. Such a block of code consists of multiple lines of code which are **indented** a set amount. Indenting code means you precede the lines with a certain amount of spaces or tabs. In the code above a number of 4 spaces is used to indicate which lines of code are associated with the `if`-statement. Since the second `print`-statement is not indented, it is no longer part of the previous code block and is therefore not dependent on the condition of the `if`-statement. It is executed *unconditionally*.

## More operators

Should you need more than the comparison operator:

- `==`  equal (note: a single `=` is used for assigning, double `=` is used for comparing!)
- `!=`  unequal
- `>` 	greater than
- `>=`	greater than or equal
- `<` 	smaller than
- `<=`	smaller than or equal

## Combining conditions

You can also combine multiple conditions. If you want to know whether a number is situated within a certain range (for example between 3 and 39), then you do so with the `and` operator:

    x = 15
    x_min = 3
    x_max = 39
    if x > x_min and x < x_max:
        print(f"the number {x} lies between {x_min} and {x_max}")

The following three operators are all operators you need to combine multiple conditions:

- `not` negation
- `and` combination (both must be `True` to be `True` together)
- `or` combination (either or both must be `True` to be `True` together)
