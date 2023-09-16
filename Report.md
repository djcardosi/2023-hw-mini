Ex 01

Q1: The runtime should be N*sleep_time. The program outputs both the measured runtime (via the time.ticks_ms and time.ticks_diff functions) and the runtime predicted via the mentioned expression.

Q2: Both are data types: ‘int’ signifies an integer, and ‘float’ a floating point number. The program will not run if an instance of ‘int’ or ‘float’ is removed, but the two may be interchanged without runtime errors, given that they are consistent for any single variable; incorrect uses, however, may affect the accuracy of the program due to rounding errors between data types.

Q3: The time.ticks_diff function makes use of modular arithmetic rather than normal subtraction, which is necessary given that the time.ticks_ms function uses a reference maximum value beyond which its values repeat or ‘wrap around’ (i.e. it returns values within a certain range, so subtraction does not always yield correct values for elapsed time).

Ex 02

Q1: Using the input() function would make the computer powering the Pico to also function as an input device, while storing the parameters in a file removes this dependence on the external computer.

Q2: Parameter storage via a JSON file separate from the code allows users to easily and quickly change the parameters’ values without having to change and replace the program code itself.

Q3: The os.path.isfile function exists in Python but not in MicroPython.

Ex 03

Q1: The decoding becomes much less accurate; the button’s state is checked less frequently, resulting in fewer recorded button presses and less resolution with which dots and dashes are distinguished from each other. Once sample_ms becomes greater than or equal to dot_dash_threshold_ms, there is effectively no resolution, and all button presses are interpreted as long.