# Project 1 Rubric

### Q1: Add Item (10 pts)
- +5: Creates item correctly
- +5: Adds item to `store_items` correctly

### Q2: List Items (10 pts)
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

- +3: Loops through each item
- +7: Prints in correct format
    - +3: 'n)'
    - +2: item name, item price
    - +2: Combines strings correctly

### Q3: Check Item Index (10 pts)
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

- +5: Checks lower bound correctly
- +5: Checks upper bound correctly

### Q4: Modify Item (5 pts)
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

- +5: Changes item correctly

### Q5: Delete Item (5 pts)
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

- +5: Deletes correct item from `store_items`

## Part 2: Amazon
All questions in part 2 are in the `amazon.py` file. While the `seller.py` file was for the seller, the `amazon.py` file is
for buyers. You will notice that the `amazon.py` file looks pretty similar to the `seller.py` file, but is missing a lot of things. This is because it is missing the code to glue all of the functions together. This is something you will have to
implement yourself. Luckily, you have already completed the `seller.py` file, and can use that as reference.

### Q6: Display Choices (15 pts)
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

- +3: Loops through items correctly
- +7: Prints items in correct format
    - +3: 'n)'
    - +2: item name, item price
    - +2: Combines strings correctly
- +5: Prints options after items correctly

### Q7: Check choice (10 pts)
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

- +5: Checks lower bound correctly
- +5: Checks upper bound correctly

### Q8: Add Item to Cart (10 pts)
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

- +5: Access correct item
- +5: Adds an item to cart correctly

### Q9: Display Cart (15 pts)
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

- +3: Loops through items correctly
- +7: Prints items in correct format
    - +3: 'n)'
    - +2: item name, item price
    - +2: Combines strings correctly
- +5: Calculates and prints total price correctly

### Q10: Checkout (10 pts)
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

- +5: Prints items correctly
- +5: Prints additional messages correctly

### Q11: Putting it all together: Process Choice (20 pts)
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

         See the process_command function in seller.py as an example for this function.
     """
     "***YOUR CODE HERE***"
```

- +5: Runs `add_item_to_cart` if choice is choice is item index
- +5: Runs `display_cart` for appropriate choice
- +5: Runs `checkout` for appropriate choice
- +5: Returns correct value

### Q12: Putting it all together: Main (20 pts)
Lastly, let's complete the `main` function to tie it all together. Be sure to read the comments to see where you should be
adding your lines. You will see at the top of the function where the `store_items`, and the `cart` variables are created. Do not modify any of these lines. All of your lines should come after it. The responsibility of the `main` function is to
continuously ask the user for input, so long as the user has not chosen the `checkout` option. Feel free to take a look at the
`main` function in `seller.py` for reference.

- +5: Uses while loop
    - +3: Correct condition
- +5: Runs `display_choices`
- +5: Prompts users for `input`
- +5: Runs `process_choice` with user input
