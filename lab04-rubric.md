# Lab 4

## Questions
(20 points total.)

### Q1: Debugging Quiz
Using Ok, take the debugging quiz with the following command:
```
python3 ok -q debugging -u
```

- +6: Complete. Check the `tests/debugging.py` and make sure that the `locked`
fields are `False`, and that the answers are not encrypted.

Example:
```
'cases': [
  {
    'answer': 'h(x + y * 5)', <-- ****Not encrypted****
    'choices': [
      'f("hi")',
      'g(x + x, x)',
      'h(x + y * 5)'
    ],
    'hidden': False,
    'locked': False, <-- ****Not locked****
    'question': r"""
    In the following traceback, what is the most recent function call?
    Traceback (most recent call last):
        File "temp.py", line 10, in <module>
          f("hi")
        File "temp.py", line 2, in f
          return g(x + x, x)
        File "temp.py", line 5, in g
          return h(x + y * 5)
        File "temp.py", line 8, in h
          return x + 0
      TypeError: must be str, not int
    """
  },
```
```
{
  'answer': '020e452a94b2d2347bf98f8857c9c626', <-- ****Encrypted****
  'choices': [
    'the code attempted to add a string to an integer',
    'the code looped infinitely',
    'there was a missing return statement'
  ],
  'hidden': False,
  'locked': True, <-- ****Locked****
  'question': r"""
  In the following traceback, what is the cause of this error?
  Traceback (most recent call last):
      File "temp.py", line 10, in <module>
        f("hi")
      File "temp.py", line 2, in f
        return g(x + x, x)
      File "temp.py", line 5, in g
        return h(x + y * 5)
      File "temp.py", line 8, in h
        return x + 0
    TypeError: must be str, not int
  """
},
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
- +1: Correctly casts `string` to int, divides answer by `num`, and prints the result
- +1: Wraps above in a `try` clause
- +1: Catches `ValueError`, prints correct message
- +1: Catches `ZeroDivisionError`, prints correct message
- +1: `else` clause prints 'No errors'
- +1: `finally` clause prints 'Finished'

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
- +1: Initializes dictionary
- +1: Loops through all elements in lst
- +2: Correctly calculates bucket based on size (`bucket = e // size * size`)
- +1: Correctly checks if key is in dictionary
- +1: Correctly inserts key value pair if key is not in dictionary (`d[bucket] = 1`)
- +1: Correctly increments counter if key is in dictionary
- +1: Returns correct dictionary
