# Lab 5

## Starter Files
Download [lab05.zip](https://github.com/david-yan/CS110_starter_code/blob/master/lab05.zip?raw=true). Inside the archive,
you will find starter files for the questions in this homework, along with a copy of the [Ok](https://cs61a.org/lab/lab01/ok)
autograder.

## Submitting
To submit, please go to [okpy](https://okpy.org/usf/cs110/sp20/lab05/) (you will need to log in with your usfca.edu email),
and click `Create a new submission`. The instructions will direct you on how you should submit the assignment. You can create
multiple submissions, and for grading, you most recent submission will be used.

The submissions will always be open up to 3 days after the assigned due date to account for slip days. If you want to create
a submission after the deadline to get comments, but do not want to use slip days, please indicate clearly in your submission.

## Questions

### Q1: Try Read File
```
def try_read_file(filename):
    """Tries to read a file with the given `filename`.
    - If the file exists, read the file, and return its contents.
    - If the file doesn't exist, prevent the error from happening, and return None.

    >>> try_read_file('files/file1')
    \'Proin eleifend ante sit amet libero laoreet tempus.\\n\'
    >>> print(try_read_file('files/no_file'))
    None
    """
    "*** YOUR CODE HERE ***"
```

Using Ok, test your code with:
```
python3 ok -q try_read_file
```

### Q2: File Word Count
```
def file_word_count(filename):
    """Creates a word count of all the words that appear in the file with the
    corresponding `filename`. The word count is a dictionary where the key is
    the word, and the value is the count. A word is described as any group of
    characters delimited by a space or new line. You can assume that the file
    exists.

    **HINT**: Use the .split() function to split a string into a list a strings,
    divided by spaces and new lines.
    Example:
    'this is a string'.split()
    ['this', 'is', 'a', 'string']

    >>> expected = {'this': 5, 'is': 4, 'some': 3, 'text': 2, 'here': 1}
    >>> got = file_word_count('files/words')
    >>> assert len(expected) == len(got)
    >>> for word in expected:
    ...     assert expected[word] == got[word], 'Expected {} for word \\'{}\\', but got {}'.format(expected[word], word, got[word])
    """
    "*** YOUR CODE HERE ***"
```
Using Ok, test your code with:
```
python3 ok -q file_word_count
```

### Q3: Write Word Count
```
def write_word_count(filename, out):
    """Creates a word count of all the words that appear in the file with the
    corresponding `filename`, and then writes the dictionary to the file with
    filename specified by `out`.

    **HINT**: You can convert a dictionary into a string representation by
    casting it to a str.
    Example:
    str({'key1': 'value1', 'key2': 'value2'})
    "{'key1': 'value1', 'key2': 'value2'}"

    >>> import json
    >>> expected = {'this': 5, 'is': 4, 'some': 3, 'text': 2, 'here': 1}
    >>> write_word_count('files/words', 'word_count')
    >>> with open('word_count') as f:
    ...     contents = f.read().replace('\\'', '\\"')
    >>> got = json.loads(contents)
    >>> for word in expected:
    ...     assert expected[word] == got[word], 'Expected {} for word \\'{}\\', but got {}'.format(expected[word], word, got[word])
    """
    "*** YOUR CODE HERE ***"
```
Using Ok, test your code with:
```
python3 ok -q write_word_count
```
