# Lab 5

## Questions
(26 points total.)

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
- +1: Opens file in read mode
- +1: Reads contents and returns result
- +1: Closes file
- +1: Wraps above in `try`
- +1: `except` clause to catch error
- +1: `return None` on error

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
- +1: Opens file in read mode
- +1: Reads all file contents
- +1: Runs `.split()` on file contents
- +1: Loops through each word
- +1: Initializes dictionary
- +2: Correctly counts words in dictionary
- +1: Returns correct result

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
- +1: Runs `file_word_count` to get dictionary of word count
- +1: Opens file in 'w' mode
- +1: Writes dictionary, cast to `str`, to the file
- +1: Closes file

### Q4: Tri Asterisk
```
def tri_asterisk(depth, out):
    """Writes a triangle of asterisks that is `depth` long, and `depth` wide to
    the file with filename, `out`. See the test cases for examples.

    **HINT**: Try using a nested for loop, or a for loop in a for loop.
    **HINT**: Don't forget writing a new line character ('\n') at the end of each line.

    >>> tri_asterisk(2, 'two_deep')
    >>> with open('two_deep') as f:
    ...     print(f.read().strip())
    **
    *
    >>> tri_asterisk(10, 'ten_deep')
    >>> with open('ten_deep') as f:
    ...     print(f.read().strip())
    **********
    *********
    ********
    *******
    ******
    *****
    ****
    ***
    **
    *
    """
    "*** YOUR CODE HERE ***"
```
- +1: Opens file in 'w' mode
- +2: Loops over `range(depth)`
  - +1: Off but demonstrates right idea
- +3: Correctly constructs line at each iteration
  - +2: Off but demonstrates right idea
- +1: Writes new line character at end of each iteration
- +1: Closes the file
