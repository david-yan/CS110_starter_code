# Lab 1: Expressions and Control Structures

## Starter Files
Download [lab01.zip](https://github.com/david-yan/CS110_starter_code/blob/master/lab01.zip?raw=true). Inside the archive,
you will find starter files for the questions in this lab, along with a copy of the [Ok](https://cs61a.org/lab/lab01/ok)
autograder.

## Running Tests
To test that your code is working correctly, run `python3 ok`. This will automatically run the test suite against your code.
Please make sure to check your output to ensure that all of the tests passed. If you have any problems running the tester,
please make a post on Piazza.

## Using OK
For ease of testing for both you and the grader, we will now be using a program called Ok for testing homeworks, labs, and
projects. A few important things to note about using Ok are the following:

To run all of the tests using Ok, run the following:
```
python3 ok
```

To run a test for a specified function, run the following command:
```
python3 ok -q <specified function>
```

By default, only tests that did not pass will show up. You can use the `-v` option to show all the tests, including tests
you have passed.
```
python3 ok -v
```

For more Ok commands, visit [here](https://cal-cs-61a-staff.github.io/ok-help/).

## Submitting
To submit, please go to [okpy](https://okpy.org/usf/cs110/sp20/lab01/) (you will need to log in with your usfca.edu email),
and click `Create a new submission`. The instructions will direct you on how you should submit the assignment. You can create
multiple submissions, and for grading, you most recent submission will be used.

The submissions will always be open up to 3 days after the assigned due date to account for slip days. If you want to create
a submission after the deadline to get comments, but do not want to use slip days, please indicate clearly in your submission.

## Required Questions

### What Would Python Display?

### Q1: Veritasiness
Use Ok to test your knowledge of booleans with the following questions:
```
python3 ok -q short-circuit -u
```

### Q2: Control
Use Ok to test your knowledger of loops and if statements with the following questions:
```
python3 ok -q control -u
```

### Coding Practice

### Q3: Absolute Value
From the following snippet of code (in `lab01.py`), fill in the parts that say `### YOUR CODE HERE ###` with the correct
code to complete the function.
```
def a_plus_abs_b(a, b):
    """Return a+abs(b), but without calling abs.
       abs(b) returns the absolute value of b.

    >>> a_plus_abs_b(2, 3)
    5
    >>> a_plus_abs_b(2, -3)
    5
    >>> # a check that you didn't change the return statement!
    >>> import inspect, re
    >>> re.findall(r'^\s*(return .*)', inspect.getsource(a_plus_abs_b), re.M)
    ['return output']
    """   
    if b >= 0:
        output = ### YOUR CODE HERE ###
    else:
        output = ### YOUR CODE HERE ###
    return output
```
Use Ok to test your code:
```
python3 ok -q a_plus_abs_b
```

### Q4: Sum Digits
Given a string of digits, find the sum of the digits.
```
def sum_digits(digits):
    """Sum all the digits of digits.
       type(digits) == str

    >>> sum_digits('10') # 1 + 0 = 1
    1
    >>> sum_digits('4224') # 4 + 2 + 2 + 4 = 12
    12
    >>> sum_digits('1234567890')
    45
    >>> a = sum_digits('123') # make sure that you are using return rather than print
    >>> a
    6
    """
    "*** YOUR CODE HERE ***"
```
Use Ok to test your code:
```
python3 ok -q sum_digits
```

### Q5: Contains Substring?
Given two strings called `search`, and `substr`, find if `substr` lies somewhere in `search`
```
def contains_substr(search, substr):
    """Return True if search contains substr within it.

    >>> contains_substr('abc', 'b')
    True
    >>> contains_substr('search this', 'search')
    True
    >>> contains_substr('search this', 'this')
    True
    >>> contains_substr('search this', 'arch th')
    True
    >>> contains_substr('search this', 's1earch')
    False
    >>> contains_substr('search this', '5earch')
    False
    >>> contains_substr('search this', 'thi5')
    False
    """
    "*** YOUR CODE HERE ***"
```
Use Ok to test your code:
```
python3 ok -q contains_substr
```

### Q6: Largest Factor
Given a number, `x`, find its largest factor that is smaller than `x`. (The modulo, `%`, operator may be useful here!)
```
def largest_factor(x):
    """Return the largest factor of x that is smaller than x.

    >>> largest_factor(15) # factors are 1, 3, 5
    5
    >>> largest_factor(80) # factors are 1, 2, 4, 5, 8, 10, 16, 20, 40
    40
    >>> largest_factor(13) # factor is 1 since 13 is prime
    1
    """
    "*** YOUR CODE HERE ***"
```
Use Ok to test your code:
```
python3 ok -q largest_factor
```

## Extra Credit Questions

### Q7: Another way of doing Q3
Just as variables can be strings, ints, and lists, variables can also be functions. By only modifying the blanks, finish
the function to achieve the same functionality as Q3.
```
from operator import add, sub

def a_plus_abs_b_extra(a, b):
    """Return a+abs(b), but without calling abs.

    >>> a_plus_abs_b_extra(2, 3)
    5
    >>> a_plus_abs_b_extra(2, -3)
    5
    >>> # a check that you didn't change the return statement!
    >>> import inspect, re
    >>> re.findall(r'^\s*(return .*)', inspect.getsource(a_plus_abs_b), re.M)
    ['return h(a, b)']
    """
    if b >= 0:
        h = _____
    else:
        h = _____
    return h(a, b)
```
Use Ok to test your code:
```
python3 ok -q a_plus_abs_b_extra
```

### Q8: Hailstone
Douglas Hofstadter's Pulitzer-prize-winning book, Gödel, Escher, Bach, poses the following mathematical puzzle.
1. Pick a positive integer x as the start.
2. If x is even, divide it by 2.
3. If x is odd, multiply it by 3 and add 1.
4. Continue this process until x is 1.
The number x will travel up and down but eventually end at 1 (at least for all numbers that have ever been tried
-- nobody has ever proved that the sequence will terminate). Analogously, a hailstone travels up and down in the
atmosphere before eventually landing on earth.

This sequence of values of x is often called a Hailstone sequence. Write a function that takes a single argument
with formal parameter name x, prints out the hailstone sequence starting at x, and returns the number of steps in
the sequence:
```
def hailstone(x):
    """Print the hailstone sequence starting at x and return its
    length.

    >>> a = hailstone(10)
    10
    5
    16
    8
    4
    2
    1
    >>> a
    7
    """
    "*** YOUR CODE HERE ***"
```
Use Ok to test your code:
```
python3 ok -q hailstone
```
