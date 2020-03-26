# Homework 3: Dictionaries

## Questions
(10 points total. Divide by score by 2 and mark out of 5 on gradebook.)

### Q1: Create Item
```
def create_item(name, price):
    """Create and return an item as a dict instead of a list. The key, 'name' should
    be mapped to the name of the item, and the key, 'price' should be mapped
    to the price.

    >>> create_item('Zoom.us', 750)
    {'name': 'Zoom.us', 'price': 750}
    """
    "*** YOUR CODE HERE ***"
```
- +1: Initializes a dictionary
- +1: Inserts correct key value pair into dictionary
- +1: Returns dictionary

### Q2: Get Value
```
def get_value(d, key):
    """Get the value of the specified key in dict, d.

    >>> d = {'key1': 'val1', 'key2': 'val2'}
    >>> get_value(d, 'key2')
    'val2'
    """
    "*** YOUR CODE HERE ***"
```
- +1: Gets and returns the correct value from the dictionary

### Q3: Histogram
```
def histogram(lst):
    """Given a list, return a dictionary in histogram format where the
    keys are each unique element in the list, and the value is the number
    of times that element appears in the list.

    >>> histogram([1, 1, 2, 3, 3, 1])
    {1: 3, 2: 1, 3: 2}
    >>> histogram([1, 'a', 'a'])
    {1: 1, 'a': 2}
    """
    "*** YOUR CODE HERE ***"
```
- +1: Initializes a histogram dictionary
- +1: Loops through all elements in lst
- +1: Checks if the element is already in the histogram
- +1: Inserts correct key value pair if the key does not exist
- +1: Increments value of correct key if the element exists
- +1: Returns result
