## Variables

A **value** is one of the core components of any program. In the examples above, you've seen sequences of characters and also numbers. Up until now we've only worked with **constant values** that are set whilst writing the actual program (for example the text `"Hello, world!"`). Though if we'd already know all values when implementing our programs, we would not need computers at all! Let's take full advantage of a computer's strength: calculating.

To be able to use results (values) from one calculation in another calculation we have to temporarily store these results. As a solution Python offers you to assign names to values. These name-value pairs are called **variables**. By using the `=` operator we can combine a name and a value, and consequently use that value elsewhere.


![embed](https://player.vimeo.com/video/287248523)

## Types

There exist a couple of different kinds of values in Python; we call them **types**. In the following table you can see three of the most important ones:

| example         | type  |                                                          |
| ----------------- | ----- | -------------------------------------------------------- |
| `'Hello, World!'` | str   | a sequence of characters: a **string**                        |
| `'3.2'`           | str   | once again a **string**, because of the quotation marks       |
| `17`              | int   | a whole number: an **integer**                       |
| `3.2`             | float | a decimal: a **float**, known as a floating point number |

You can also **convert** types from one into the other. For instance you could use `int()` to cast a value into an integer. But only if at all possible, else Python will start complaining:

| conversion                 | result                                                      |
| ------------------------- | -------------------------------------------------------------- |
| `print(int('32'))`        | `32`                                                           |
| `print(int('Hello'))`     | `ValueError: invalid literal for int(): Hello`                 |
| `print(int(3.99999))`     | `3` (Note! no error, but there is information loss) |
| `print(int(-2.3))`        | `-2`                                                           |
| `print(float(32))`        | `32.0`                                                         |
| `print(float('3.14159'))` | `3.14159`                                                      |
| `print(str(32))`          | `'32'`                                                         |
| `print(str(3.14159))`     | `'3.14159'`                                                    |

Did you notice that decimals are denoted in the American Style (with a point instead of a comma)? This is the case for most programming languages.
