# Lab 6

## Questions

### Q1: Dog Constructor
```
def _______(___):
    """Fill in the blank above and add parameters to the function to define
    the constructor to the Dog class.

    The constructor should:
    - Take a string, `name`, as a parameter
    - Have the instance fields `name`, `happiness`, and `training`
        - The `name` instance field should be the parameter provided
        - The `happiness` and `training` fields start with a value of 5

    >>> dog = Dog('Toby')
    >>> dog.name
    'Toby'
    >>> dog.happiness
    5
    >>> dog.training
    5
    """
    "*** YOUR CODE HERE ***"
```

- +5: Correct

### Q2: Train
```
def train(___):
    """Fill in the blank above for the parameters to the instance method,
    `train`. This method should take no parameters when its run. Take a look
    at the test for an example.

    The `train` instance method raises the dog's training level by one, but
    reduces its happiness by 1.

    The method should not return anything.

    >>> dog = Dog('Toby')
    >>> dog.happiness
    5
    >>> dog.training
    5
    >>> dog.train()
    >>> dog.happiness
    4
    >>> dog.training
    6
    """
    "*** YOUR CODE HERE ***"
```

- +5: Correct

### Q3: Give Treat
```
def give_treat(___):
    """Fill in the blank above for the parameters to the instance method,
    `give_treat`. This method should take no parameters when its run. Take a look
    at the test for an example.

    The `give_treat` instance method raises the dog's happiness by 1.

    The method should not return anything.

    >>> dog = Dog('Toby')
    >>> dog.happiness
    5
    >>> dog.give_treat()
    >>> dog.happiness
    6
    """
    "*** YOUR CODE HERE ***"
```

- +5: Correct

### Q4: Sit
```
def sit(____):
    """Fill in the blank above for the parameters to the instance method,
    `sit`. This method should take no parameters when its run. Take a look
    at the test for an example.

    The sit function will return something different based on the dog's
    happiness and training levels.
    If:
    - The dog's happiness is below 4, the dog will ignore you.
        - return '<dog's name> ignores you'
    - The dog's training is above 6, and the dog's happiness is at or
    above 4, the dog will sit.
        - return '<dog's name> sits'
    - The dog's training is at or below 6, and the dog's happiness is
    at or above 4, the dog does nothing.
        - return '<dog's name> does nothing'

    >>> dog = Dog('Toby')
    >>> dog.sit()
    'Toby does nothing'
    >>> dog.train() #happiness=4, training=6
    >>> dog.train() #happiness=3, training=7
    >>> dog.sit()
    'Toby ignores you'
    >>> dog.give_treat() #happiness=4, training=7
    >>> dog.sit()
    'Toby sits'
    """
    "*** YOUR CODE HERE ***"
```

- +5: Correct
