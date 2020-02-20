# Lab 3: Control statements

## Starter Files
Download [lab03.zip](https://github.com/david-yan/CS110_starter_code/blob/master/lab03.zip?raw=true). Inside the archive,
you will find starter files for the questions in this lab.

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
To submit, please go to [okpy](https://okpy.org/usf/cs110/sp20/lab03/) (you will need to log in with your usfca.edu email),
and click `Create a new submission`. The instructions will direct you on how you should submit the assignment. You can create
multiple submissions, and for grading, you most recent submission will be used.

### Be sure to submit your entire lab03 directory.
We will be checking the `tests/control.py` file to ensure that you did Q1.

The submissions will always be open up to 3 days after the assigned due date to account for slip days. If you want to create
a submission after the deadline to get comments, but do not want to use slip days, please indicate clearly in your submission.

## Required Questions

### What Would Python Display?

### Q1: Control
Use Ok to test your knowledge of booleans with the following questions. If you get stuck or need to take a break, don't
worry! Press `Ctrl+C` to exit, your progress will be saved.
```
python3 ok -q control -u
```

### Coding Practice

From the following snippet of code (in `lab03.py`), fill in the parts that say `### YOUR CODE HERE ###` with the correct
code to complete the function.

### Q2: Two of Three
```
def two_of_three(x, y, z):
    """Return a*a + b*b, where a and b are the two smallest members of the
    positive numbers x, y, and z.

    >>> two_of_three(1, 2, 3)
    5
    >>> two_of_three(5, 3, 1)
    10
    >>> two_of_three(10, 2, 8)
    68
    >>> two_of_three(5, 5, 5)
    50
    """
    "*** YOUR CODE HERE ***"
```
Use Ok to test your code:
```
python3 ok -q two_of_three
```

### Q3: Second Largest
```
def second_largest(lst):
    """Returns the second largest number in lst.
    >>> second_largest([2, 1])
    1
    >>> second_largest([1, 2, 3, 4, 5])
    4
    >>> second_largest([3, 5, 2, 6, 1])
    5
    >>> second_largest([5, 2, 3, 4, 5])
    5
    """
    "*** YOUR CODE HERE ***"
```
Use Ok to test your code:
```
python3 ok -q second_largest
```

### Q4: Number of Sevens
```
def num_sevens(x):
    """Returns the number of times 7 appears as a digit of x.

    >>> num_sevens(3)
    0
    >>> num_sevens(7)
    1
    >>> num_sevens(7777777)
    7
    >>> num_sevens(2637)
    1
    >>> num_sevens(76370)
    2
    >>> num_sevens(12345)
    0
    """
    "*** YOUR CODE HERE ***"
```
Use Ok to test your code:
```
python3 ok -q num_sevens
```
