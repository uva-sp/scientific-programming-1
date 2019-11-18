## Loops

Occasionally it is useful to determine whether a whole sequence of numbers meets a certain condition. In that case, we would like to repeat a piece of code for all numbers in that sequence. Repetition, such a "simple task", is exactly the strong suit of a computer and has become a basic element in virtually all programming languages. We call this a **loop**.

## Repetition

If we want to repeat something for 10 times, it would look like this:

    for x in range(1, 11):
        print("hello")

We use the command `range()` with a start and an end to indicate how many times the loop should repeat. A Python `range` runs from the start *up to* the end, so it is not *inclusive*!

Aside from that, just as with the `if`-statement, the `for` ends with a `:`, to indicate which *lines* of code should be repeated. Which in this case would only be the `print` that is preceded by 4 spaces.

## Examples of loops

![embed](https://vimeo.com/album/5380755/embed)

## Step size of a loop

You can also declare the step size for a `range`. The range still runs from start up to the end, but instead of steps of 1, it will take steps the size that you've set. Like this:

    for number in range(1, 100, 10):
        ...

Each step in the `for`-loop will be 10 larger than the previous. Take a minute to think over the steps the above loop would make; or copy the code and add a `print` to it to study its behavior.

## Types of loops

Dependent on the type of application you can choose either type of loop that you've seen in the videos before. The `for` and `while` are practically interchangeable. This `for`-loop:

    for i in range(100):
        print("hi")

does the same as the following `while`-loop:

    i = 0
    while i < 100:
        print("hi")
        i = i + 1

Obviously, the `for`-loop is somewhat more compact and more readable. Therefore, this type of loop is used most often. Cases such as asking for user input are often times best implemented with a `while`-loop. As a general rule for which loop to choose; a `for`-loop is used if you know, or can calculate, exactly how often the loop should repeat. A `while`-loop is used when the amount of repetitions is uncertain.
