## User input

Besides having your program printing to the user, you can also ask for input from the user. This way you can write **interactive programs** that can perform calculations based on user provided values. Python comes with a variety of different function to prompt for input. One of which is `input()`, which can be used as shown below:

    name = input("Please enter your first name: ")
    print("Hello,", name)


The string `"Please enter your first name: "` that follows the function `input`, is immediately displayed on the users screen when `input` is executed. After which `input` will patiently wait for the user to fill in any value and until they press **enter**. The provided value is now assigned a name. In the example above it is coincidentally assigned the name `name`. After which it is printed on the next line using the variable `name` within the print statement.

The `input` function always gives you the user provided value as a string. But sometimes you might want the user to provide a number, so you can perform a calculation. Then you'd have to use one of the conversions demonstrated above. For instance:

    seat_count = input("How many seats should be reserved?")
    seat_count = int(seat_count)
