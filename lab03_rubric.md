# Lab 3 Rubric

## Required Questions

### What Would Python Display?

### Q1: Control (5 pts)
- Check the `tests/control.py` file to see that the answers to the questions are revealed, and the `'locked'` field is
`False`

### Coding Practice

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
- +1: Uses `if` statement(s)
- +2: Correct condition to find largest number
- +2: Correct condition to find second largest number
- +1: Correct expression to calculate `a*a + b*b`


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
- +1: Uses some sort of loop
- +2: Correct implementation to loop through entire list
- +1: Keeps track of largest number
- +2: Keeps track of and finds second largest number

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
- +1: Uses `while` loop
- +2: Correct end condition for while loop
- +1: Calculates digit correctly
- +1: Checks if digit is 7
- +1: Counts number of 7s correctly
