
### Q1: Owner Constructor
```
def _______(___):
    """Fill in the blank above and add parameters to the function to define
    the constructor to the Owner class.

    The constructor should:
    - Take a string, `name`, as a parameter
    - Have the instance fields `name`, and `pet`
        - The `name` instance field should be the parameter provided
        - The `pet` instance field should start out as None

    >>> owner = Owner('Alice')
    >>> owner.name
    'Alice'
    >>> print(owner.pet)
    None
    """
    "*** YOUR CODE HERE ***"
```
Using Ok, test your code with:
```
python3 ok -q owner
```

### Q2: Adopt
```
def adopt(___):
    """Fill in the blank above for the parameters to the instance method,
    `adopt`. This method should take an instance of Dog as its parameter.
    Take a look at the test for an example.

    The `adopt` instance method sets the `pet` instance field to the
    parameter value.

    The method should not return anything.

    >>> dog = Dog('Toby')
    >>> owner = Owner('Alice')
    >>> owner.name
    'Alice'
    >>> print(owner.pet)
    None
    >>> owner.adopt(dog)
    >>> owner.pet.name
    'Toby'
    """
    "*** YOUR CODE HERE ***"
```
Using Ok, test your code with:
```
python3 ok -q adopt
```

### Q3: Train Pet
```
def train_pet(___):
    """Fill in the blank above for the parameters to the instance method,
    `train_pet`. This method should take no parameters when its run. Take a
    look at the test for an example.

    The `train_pet` instance method trains the pet to sit by repeatedly
    asking it to sit, and responding according to the pet's actions.

    - If the owner does not have a pet:
        - return '<owner name> really wants a pet.'
    - Otherwise repeatedly ask the pet to sit.
        - If the pet does nothing, train it.
        - If the pet ignores you, give it a treat.
        - If the pet sits, you're done!

    The method should not return anything.

    >>> dog = Dog('Toby')
    >>> owner = Owner('Alice')
    >>> owner.adopt(dog)
    >>> owner.train_pet()
    >>> owner.pet.sit()
    'Toby sits'
    """
    "*** YOUR CODE HERE ***"
```
Using Ok, test your code with:
```
python3 ok -q train_pet
```
