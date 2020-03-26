# Homework 4

## Questions
(10 points total, divide score by half to make out of 5 on gradebook)

### Q1: Replace File
```
def replace_file(filename, contents):
    """Replace the file with the specified `filename` with `contents`.

    >>> import helpers.helper as helper
    >>> filename = helper.prepare_test_files()
    >>> contents = 'new contents'
    >>> replace_file(filename, contents)
    >>> with open(filename) as f:
    ...     assert f.read().strip() == contents
    >>> helper.cleanup(filename)
    """
    "*** YOUR CODE HERE ***"
```

- +1: Opens file correct file
- +1: Opens file with file mode 'w'
- +1: Writes contents to file
- +1: Closes file

### Q2: Add Lines
```
def add_lines(filename, lst):
    """For each item in `lst`, write that item in a new line to the end of the
    file specified by `filename`.

    **NOTE**: Be careful where you insert your new line.

    >>> import helpers.helper as helper
    >>> filename = helper.prepare_test_files()
    >>> lst = ['these', 'words', 'are', 'new', 'contents']
    >>> add_lines(filename, lst)
    >>> with open(filename) as f:
    ...     line = f.readline().strip()
    ...     assert line == filename, 'Expected {}, got {}'.format(filename, line)
    ...     for e in lst:
    ...         line = f.readline().strip()
    ...         assert line == e, 'Expected {}, got {}'.format(e, line)
    >>> helper.cleanup(filename)
    """
    "*** YOUR CODE HERE ***"
```
Using Ok, test your code with:
```
python3 ok -q add_lines
```

- +1: Opens file correct file
- +1: Opens file with filemode 'a'
- +1: Loops through elements in lst
- +1: Writes each element in lst to the file
- +1: Correctly prepends new line character to each line written
- +1: Closes the file

