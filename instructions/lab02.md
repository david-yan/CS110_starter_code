# Lab 2: Python at its Basics

## Starter Files
Download [lab02.zip](https://github.com/david-yan/CS110_starter_code/blob/master/lab02.zip?raw=true). 

Inside the archive, you will find the following files:
- lab01.py : An empty file where code for Q1-Q5 should go.
- example_tests.py : A file that contains the circumference and area functions, with example tests.
- jimmy_hw.py : A file that contains Jimmy's homework. Relevant to Q6.
- ok : Autograder for Jimmy.
- lab01.ok : Autograder for Jimmy.

## Testing Your Code
For the purposes of making sure that you know how to define your own functions, you will be responsible for testing your
own code. Be sure to read the instructions carefully as they will detail exactly how your functions are supposed to behave.
We have provided a file, `example_tests.py`, that contains the two functions mentioned in class, and ways to manually test
them as reference. 

If you have any questions about the instructions, be sure to ask on Piazza.

## Submitting
To submit, please go to [okpy](https://okpy.org/usf/cs110/sp20/lab01/) (you will need to log in with your usfca.edu email),
and click `Create a new submission`. The instructions will direct you on how you should submit the assignment. You can create
multiple submissions, and for grading, you most recent submission will be used.

The submissions will always be open up to 3 days after the assigned due date to account for slip days. If you want to create
a submission after the deadline to get comments, but do not want to use slip days, please indicate clearly in your submission.

## Questions

### Writing Your Own Functions
All code for these questions should be added to the `lab01.py` file.

### Q1: Dog years
Define a function such that given a dog's age as an integer, calculate and return the dog's age in human years. Each year
for a dog is equivalent to 7 years for a human.

Example test:
In `lab01.py`:
```
def dog_years(years):
  ...
print(dog_years(7)) # Test the function here
```
Testing:
```
lab01$ python3 lab01.py
49
```

### Q2: Divisible?
Define a function such that given two numbers, returns True if the first number is divisible by the second. 

Tip: The modulo operator, `%`, should be very useful here. When applied to two numbers, it returns the remainder of dividing
the first number with the second.
Example:
```
>>> 4 % 4
0
>>> 5 % 4
1
```
Tip: Remember the `==` operator returns `True` if the values on both sides are equivalent.

### Q3: How much should I Venmo you?
Define a function such that given the total price of a bill, the rate of tax, the rate of tip, and the number of people at
your table, calculate and return the amount that each person should pay if you were to divide the bill evenly, as a string
in the form: `"$<dollars>.<cents>"`.

Tip: For getting the amount of cents, some clever use of the divide operator, `/`, and the modulo operator, `%`, will be
needed.

### Q4: Celcius to Fahrenheit
Define a function that converts celcius to fahrenheit. The conversion for celcius to fahrenheit is as follows:
```
F = (9 / 5) * C + 32
```

### Q5: Fahrenheit to Celcius
Define a function that does the exact opposite of Q4.

### Someone help Jimmy.

### Q6: Help Jimmy with his homework
Poor Jimmy has been having trouble with his homework. His logic looks pretty good, but he has a slew of syntax errors.
Find a fix all of his syntax errors such that all his test cases pass.

To test Jimmy's code:
```
python3 ok
```

## Submission
To submit, please navigate to [okpy](https://okpy.org/usf/cs110/sp20/lab02/), and click `Create a new submission`. Please
upload your entire `lab02` folder for your submission.
