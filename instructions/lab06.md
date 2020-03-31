# Lab 6

## Starter Files
Download [lab06.zip](https://github.com/david-yan/CS110_starter_code/blob/master/lab06.zip?raw=true). Inside the archive,
you will find starter files for the questions in this homework, along with a copy of the [Ok](https://cs61a.org/lab/lab01/ok)
autograder.

## Submitting
To submit, please go to [okpy](https://okpy.org/usf/cs110/sp20/lab06/) (you will need to log in with your usfca.edu email),
and click `Create a new submission`. The instructions will direct you on how you should submit the assignment. You can create
multiple submissions, and for grading, you most recent submission will be used.

The submissions will always be open up to 3 days after the assigned due date to account for slip days. If you want to create
a submission after the deadline to get comments, but do not want to use slip days, please indicate clearly in your submission.

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

Using Ok, test your code with:
```
python3 ok -q dog
```

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
Using Ok, test your code with:
```
python3 ok -q train
```

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
Using Ok, test your code with:
```
python3 ok -q give_treat
```

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
Using Ok, test your code with:
```
python3 ok -q sit
```

### Q5: Owner Constructor
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

### Q6: Adopt
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

### Q7: Train Pet
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
