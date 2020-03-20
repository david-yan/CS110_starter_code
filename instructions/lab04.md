# Lab 4

## Starter Files
Download [lab04.zip](https://github.com/david-yan/CS110_starter_code/blob/master/lab04.zip?raw=true). Inside the archive,
you will find starter files for the questions in this homework, along with a copy of the [Ok](https://cs61a.org/lab/lab01/ok)
autograder.

## Submitting
To submit, please go to [okpy](https://okpy.org/usf/cs110/sp20/lab04/) (you will need to log in with your usfca.edu email),
and click `Create a new submission`. The instructions will direct you on how you should submit the assignment. You can create
multiple submissions, and for grading, you most recent submission will be used.

The submissions will always be open up to 3 days after the assigned due date to account for slip days. If you want to create
a submission after the deadline to get comments, but do not want to use slip days, please indicate clearly in your submission.

## Questions

### Q1: Debugging Quiz
Using Ok, take the debugging quiz with the following command:
```
python3 ok -q debugging
```

### Q2: Error Handler
```
def error_handler(string, num):
    """Tries the following:
    1. Converts the `string` parameter to an int.
    2. Divide the converted `string` with `num` and print the result

    - If the cast fails, print 'Cannot cast to int'
    - If the division causes an error, print 'Division failed'
    - If no error happens, print 'No errors'
    - At the very end, print 'Finished'

    >>> error_handler('not an int', 2)
    Cannot cast to int
    Finished
    >>> error_handler('1', 0)
    Division failed
    Finished
    >>> error_handler('1', 2)
    0.5
    No errors
    Finished
    """
    "*** YOUR CODE HERE ***"
```
Using Ok, test your code with:
```
python3 ok -q error_handler
```

### Q3: Histogram_buckets
```
def histogram_buckets(lst, size):
    """Creates a histogram from a list of integers where the bucket size
    is specified by the `size` parameter. Buckets start at 0. The key for
    the histogram is the beginning of the bucket, and the value is the number
    of items in the bucket.

    >>> histogram_buckets([3, 2, 5, 1, 4, 0, 1], 2)
    {2: 2, 4: 2, 0: 3}
    >>> histogram_buckets([5, 11, 23, 15, 24, 39, 12, 4, 17], 10)
    {0: 2, 10: 4, 20: 2, 30: 1}
    """
    "*** YOUR CODE HERE ***"
```
Using Ok, test your code with:
```
python3 ok -q histogram_buckets
```
