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

## Part 2: Amazon
All questions in part 2 are in the `amazon.py` file. While the `seller.py` file was for the seller, the `amazon.py` file is
for buyers. You will notice that the `amazon.py` file looks pretty similar to the `seller.py` file, but is missing a lot of things. This is because it is missing the code to glue all of the functions together. This is something you will have to
implement yourself. Luckily, you have already completed the `seller.py` file, and can use that as reference.

### Q6: Display Choices
Let's begin by writing the function that will print out the options for the buyer. This is similar to the `print_seller_menu`
function in `seller.py`, but is different in that it changes based on the items in the store. The function declaration and
description of the function are as follows:
```
def display_choices(store_items):
      """ Displays the buyer menu in the following format:
          Add item to cart:
          0) <item name>: $<item price>
          1) <item name>: $<item price>
          ...
          Or:
          N-1) Display cart.
          N) Checkout.
          See test below for example.

          >>> store_items = [['iPhone Galaxy XL', 799.99], ['Microsoft   Macbook 10', 1299.99]]
          >>> display_choices(store_items)
          Add item to cart:
          0) iPhone Galaxy XL: $799.99
          1) Microsoft Macboook 10: $1299.99
          Or:
          2) Display cart.
          3) Checkout.
      """
      "***YOUR CODE HERE***"
```
You will notice that this version of Amazon doesn't allow you to remove items from your cart :speak_no_evil:.

To test your code with the autograder tests, run the following:
```
python3 ok -q display_choices
```

### Q7: Check choice
Similar to how we had to implement `check_item_index` in `seller.py`, let's check that the choice provided is valid, given
the `store_items`. Note, this is different than `check_item_index` in that there are valid choices that are not item indices.
```
def check_choice(choice, store_items):
      """ Checks that the choice given is valid.
          Returns:
          - True if the choice is valid. (Remember display cart and che  ckout options!)
          - False otherwise.

          >>> store_items = [['iPhone Galaxy XL', 799.99], ['Microsoft   Macbook 10', 1299.99]]
          >>> check_choice(0, store_items)
          True
          >>> check_choice(1, store_items)
          True
          >>> check_choice(2, store_items)
          True
          >>> check_choice(3, store_items)
          True
          >>> check_choice(4, store_items)
          False
          >>> check_choice(-1, store_items)
          False
      """
      "***YOUR CODE HERE***"
```

To test your code with the autograder tests, run the following:
```
python3 ok -q check_choice
```

### Q8: Add Item to Cart
Before we put things together, let's first implement each function first. Implement `add_item_to_cart` which will add the item
in `store_items` with an index of `item_index` to `cart.
```
def add_item_to_cart(item_index, store_items, cart):
      """ Adds the item in store_items with index of item_index to the   cart.
          See test below for an example.

          >>> store_items = [['iPhone Galaxy XL', 799.99], ['Microsoft   Macbook 10', 1299.99]]
          >>> cart = []
          >>> add_item_to_cart(1, store_items, cart)
          >>> print(cart)
          [['Microsoft Macbook 10', 1299.99]]
          >>> add_item_to_cart(0, store_items, cart)
          >>> print(cart)
          [['Microsoft Macbook 10', 1299.99], ['iPhone Galaxy XL', 799.  99]]
          >>> add_item_to_cart(1, store_items, cart)
          >>> print(cart)
          [['Microsoft Macbook 10', 1299.99], ['iPhone Galaxy XL', 799.  99], ['Microsoft Macbook 10', 1299.99]]
      """
      "***YOUR CODE HERE***"
```
To test your code with the autograder tests, run the following:
```
python3 ok -q add_item_to_cart
```

### Q9: Display Cart
Implement `display_cart` that prints information about our cart as described in the comments:
```
def display_cart(cart):
      """ Displays the cart in the following format:
          <item name>: $<item price>
          <item name>: $<item price>
          ...
          Total price: $<total price>

          >>> cart = [['item 1', 1099.99], ['item 2', 799.99], ['item 3  ', 1299.99]]
          >>> display_cart(cart)
          item1: $1099.99
          item2: $799.99
          item3: $1299.99
          Total price: $3,199.97
      """
      "***YOUR CODE HERE***"
```

To test your code with the autograder tests, run the following:
```
python3 ok -q display_cart
```

### Q10: Checkout
Implement `checkout`, which will display the cart, and then a Goodbye message.
```
def checkout(cart):
      """ Displays the cart, then prints a Goodbye message in the follo  wing format:
          Here are the items you purchased:
          <item name>: $<item price>
          <item name>: $<item price>
          ...
          Total price: $<total price>
          Thank you! Have a great day! No returns!

          >>> cart = [['item 1', 1099.99], ['item 2', 799.99], ['item 3  ', 1299.99]]
          >>> checkout(cart)
          Here are the items you just purchased:
          item1: $1099.99
          item2: $799.99
          item3: $1299.99
          Total price: $3,199.97
          Thank you! Have a great day! No returns!
      """
      "***YOUR CODE HERE***"
```

To test your code with the autograder tests, run the following:
```
python3 ok -q checkout
```

### Q11: Putting it all together: Process Choice
Now let's put it all together, starting with `process_choice`. `process_choice` functions very similarly to `process_command`
in `seller.py`, and it should use all of the functions you completed above in Part 2. Given a `choice`, it should run the
appopriate function. Make sure you read through `process_command`, as it will be great reference for how to complete this
function.
```
def process_choice(choice, store_items, cart):
     """ Processes the choice, displaying the appropriate information   and running the
         appropriate function based on the choice provided.
         Return:
         - True if the user chose the Checkout option.
         - False otherwise.

         See the process_command function in seller.py as an example f  or this function.
     """
     "***YOUR CODE HERE***"
```
There are no autograder tests for this question.

### Q12: Putting it all together: Main
Lastly, let's complete the `main` function to tie it all together. Be sure to read the comments to see where you should be
adding your lines. You will see at the top of the function where the `store_items`, and the `cart` variables are created. Do not modify any of these lines. All of your lines should come after it. The responsibility of the `main` function is to
continuously ask the user for input, so long as the user has not chosen the `checkout` option. Feel free to take a look at the
`main` function in `seller.py` for reference.

There are also no autograder tests for this question.

Now that you are done, you can test everything with
```
python3 amazon.py
```
Run your code, and play around with you new pseudo-Amazon program!

## Submitting
To submit, please go to [okpy](https://okpy.org/usf/cs110/sp20/proj01/) (you will need to log in with your usfca.edu email),
and click `Create a new submission`. The instructions will direct you on how you should submit the assignment. You can create
multiple submissions, and for grading, you most recent submission will be used.

### Be sure to submit your entire proj01 directory.

The submissions will always be open up to 4 days after the assigned due date to account for slip days. If you want to create
a submission after the deadline to get comments, but do not want to use slip days, please indicate clearly in your submission.
