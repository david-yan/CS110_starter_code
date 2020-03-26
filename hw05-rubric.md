# Homework 5

## Questions
(10 points total, divide score by half to make out of 5 on gradebook)

### Q1: Read All
```
def read_all(filename):
    """Opens the file with filename, prints it's contents, and
    closes the file.

    >>> read_all('test_file1')
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin eget.
    """
    "*** YOUR CODE HERE ***"
```

- +1: Opens file correct file with filemode 'r'
- +1: Reads and returns contents of file
- +1: Closes file

### Q2: File Word Count
```
def read_all_with(filename):
    """Opens the file with filename, prints it's contents, and
    closes the file, using the `with` method described in class.

    >>> read_all('test_file1')
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin eget.
    """
    "*** YOUR CODE HERE ***"
```
- +1: Opens file in `with` clause with filemode 'r'
- +1: Reads file in `with` clause
- +1: Doesn't call `f.close()` in `with` clause

### Q3: Readline N
```
def readline_n(filename, n):
    """Reads and returns the nth line in the file, filename.

    >>> readline_n('test_file2', 3)
    \'Nullam dapibus elit quis enim porta, et feugiat purus maximus.\\n\'
    >>> readline_n('test_file2', 2)
    \'Proin ut ex sed diam tempor laoreet eu et eros.\\n\'
    """
    "*** YOUR CODE HERE ***"
```
- +1: Opens file with filemode 'r'
- +2: Reads correct line (either loop or `readlines()`)
- +1: Returns correct line
