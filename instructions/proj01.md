# Project 1: Amazon

## Background
In this project, you will be implementing an Amazon-like program! It will be split into two parts, one part for the seller,
and the second part for the buyer. By the end of this project, you will have a seller program that allows you to add,
modify, and delete items, and a buyer program that allows you to purchase items from the marketplace.

## Starter Files
Download [proj01.zip](https://github.com/david-yan/CS110_starter_code/blob/master/proj01.zip?raw=true). Inside the archive,
you will find the following files:
- `seller.py` - The code for the first part of this project.
- `amazon.py` - The code for the second part of this project.
- `common.py` - Helper file used for this project. Please do not modify this file.
- `ok` - Autograder program.
- `proj01.ok` - Configuration for the autograder. Please do not modify this file.

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

#### The following questions are meant to be completed in order.

## Part 1: Seller

### Q0: Exploring `seller.py`
Before we begin, let's explore the `seller.py` file. Look inside the file to find all of the functions that you will be
implementing listed at the top. Be sure not to modify the functions below the line indicated.

Try running the program with:
```
python3 seller.py
```
You will see a bunch of options displayed, and you can play and interact with the menus now, but none of the functionality
is there. You will be implementing those in the following questions!

### Q1: Add Item
The first thing we are going to implement is the `add_item` function. Given a `name`, and a `price`, add the item to the
list, `store_items`. An item is represented as a list where the first element is the name, and the second element is the
price. Therefore, your `store_items` will have lists within a list. See the tests for examples.

Here is the full description, as seen in the file.
```
def add_item(name, price, store_items):
    """ Adds new item to the store_items list with the given name and price.
        Each item should be stored as a list in the form: [name, price].
        See tests below for examples:

        >>> store_items = []
        >>> add_item('iPhone Galaxy XL', 799.99, store_items)
        >>> print(store_items)
        [['iPhone Galaxy XL', 799.99]]
        >>> add_item('Microsoft Macbook 10', 1299.99, store_items)
        >>> print(store_items)
        [['iPhone Galaxy XL', 799.99], ['Microsoft Macbook 10', 1299.99]]
    """
    "***YOUR CODE HERE***"
```

To test your code with the autograder tests, run the following:
```
python3 ok -q add_item
```

### Q2: List Items
Now that we can add items to our store, let's display them. Implement the `list_items` function to display your store items
in the specified format.

```
def list_items(store_items):
    """ Displays store items in a numbered list in the following format:
        0) <item name>: $<item price>
        1) <item name>: $<item price>
        ...
        See test below for an example.

        >>> store_items = [['iPhone Galaxy XL', 799.99], ['Microsoft Macbook 10', 1299.99]]
        >>> list_items(store_items)
        0) iPhone Galaxy XL: $799.99
        1) Microsoft Macbook 10: $1299.99
    """
    "***YOUR CODE HERE***"
```

After you finish implementing this, you should be able to add and see your items with the first two commands in the menu.
Manually test this with
```
python3 seller.py
```

To run the autograder tests for this question, run the following:
```
python3 ok -q list_items
```

### Q3: Check Item Index
To enable the `modify_item` and `delete_item` functions, we need to first be able to check if the given index is valid
given our list of `store_items`. Implement `check_item_index` to return `True` if the index provided is valid, and `False`
otherwise.

```
def check_item_index(item_index, store_items):
    """ Checks that the item index is valid.
        Returns:
        - True if index is in bounds of the list, no negative indices!
        - False otherwise

        >>> store_items = [['iPhone Galaxy XL', 799.99], ['Microsoft Macbook 10', 1299.99]]
        >>> check_item_index(0, store_items)
        True
        >>> check_item_index(1, store_items)
        True
        >>> check_item_index(2, store_items)
        False
        >>> check_item_index(-1, store_items)
        False
    """
    "***YOUR CODE HERE***"
```

To test your code with the autograder tests, run the following:
```
python3 ok -q check_item_index
```

### Q4: Modify Item
Now let's implement `modify_item`. Given an `item_index`, set the item with that index to have the new `name` and `price`
attributes provided.
```
def modify_item(item_index, name, price, store_items):
    """ Sets the item in store_items with item_index to have a new name, and price, as
        specified in the arguments.

        >>> store_items = [['iPhone Galaxy XL', 799.99], ['Microsoft Macbook 10', 1299.99]]
        >>> modify_item(0, 'Google S9', 849.99, store_items)
        >>> print(store_items)
        [['Google S9', 849.99], ['Microsoft Macbook 10', 1299.99]]
    """
    "***YOUR CODE HERE***"
```

After implementing this, you can test this manually by choosing option 2 when you run
```
python3 seller.py
```

To test your code with the autograder tests, run the following:
```
python3 ok -q modify_item
```

### Q5: Delete Item
Lastly for the seller file, let's implement the `delete_item` function. Given an `item_index` we want to remove the item
with that index from the `store_items`. 

** Hint: The `del` function should be very useful here. **
```
def delete_item(item_index, store_items):
    """ Deletes the item in store_items with the specified index.

        >>> store_items = [['iPhone Galaxy XL', 799.99], ['Microsoft Macbook 10', 1299.99]]
        >>> delete_item(1, store_items)
        >>> print(store_items)
        [['iPhone Galaxy XL', 799.99]]
    """
    "***YOUR CODE HERE***"
```

To test your code with the autograder tests, run the following:
```
python3 ok -q delete_item
```

Once you have implemented this, you should have complete functionality in your `seller.py` file!
See for yourself by running
```
python3 seller.py
```
And playing with the options.

## Submitting
To submit, please go to [okpy](https://okpy.org/usf/cs110/sp20/proj01/) (you will need to log in with your usfca.edu email),
and click `Create a new submission`. The instructions will direct you on how you should submit the assignment. You can create
multiple submissions, and for grading, you most recent submission will be used.

### Be sure to submit your entire proj01 directory.

The submissions will always be open up to 4 days after the assigned due date to account for slip days. If you want to create
a submission after the deadline to get comments, but do not want to use slip days, please indicate clearly in your submission.
