## Format

We've already demonstrated how to print variables in a string. For example:

    temperature = 1000
    print("The temperature is", temperature, "degrees.")

There is also another, better, way of printing variables in a string:

    print(f"The temperature is {temperature} degrees.")

The `f` that precedes the quotation marks of the string denotes that this is a **formatted string**. In which the accolades, `{}`, signify a placeholder that contains a variable. Upon printing the part of the string in accolades is replaced for the the value that variable has at the time of printing.

This is especially useful when printing multiple variables:

    temperature = 1000
    pressure = 1.013
    print(f"It is {temperature} degrees and the air pressure is {pressure} bar.")

You can also perform arithmetic or other actions within the curly braces `{}`, though that is often times better done ahead of printing.
