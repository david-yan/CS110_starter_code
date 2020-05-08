## Practice Final 1

### Q1 Checked Conversion

Given string as an input, attempts to convert the string to a dollar and cents value. The expected format of the string is the following:
${dollars}.{cents}

The function should return a float representing the number of dollars, and cents rounded up to the hundreds decimal. If the string is in any other format, return `None`.

Take a look at the tests for clarifying examples.
```
def string_to_value(string):
  """
  >>> string_to_value('$42.42')
  42.42
  >>> string_to_value('42.42')
  None
  >>> string_to_value('$42.4242')
  42.43
  >>> string_to_value('$42.4')
  42.4
  """
  
  ### ANSWER ###
  if string[0] != '$':
    return None
  try:
    # string[1:] takes all characters in string except the first
    value = float(string[1:])
    return int(value * 100) / 100
  except:
    return None
```

### Q2 Write if not exists

Given a list of filenames, for each filename create a file with said filename, and write the filename to that file if the file does not exist.

*Hint*: Remember how `open()` behaves if you try to open a non-existent file in read-mode.

```
def write_if_not_exists(filenames):
  ### ANSWER ###
  for filename in filenames:
    try:
      # open() errors if you try to open a non-existant file in read-mode (default)
      f = open(filename)
      f.close()
    except:
      with open(filename, 'w') as f:
        f.write(filename)
```

### Q3 File Line Reader
```
class LineReader:
  def __init__(self, filename):
    with open(filename) as f:
      contents = f.read()
      self.lines = contents.split('\n') # split by newline character
      self.index = 0
  
  def next_line(self):
    if self.index < len(self.lines):
      self.index += 1
      return self.lines[self.index - 1]
    return None
    
  def next(self):
    # Don't need to check lower bound because self.index starts at 0
    return self.index < len(self.lines)
    
  def seek(self, index):
    if index >= 0 and index < len(self.lines):
      self.index = index
    return self.index
    
  def remaining_lines(self):
    output = ''
    while self.next():
      output += self.next_line() + '\n'
    return output
```

### Q4 Palindrome
Returns `True` if the `string` argument is a palindrome, `False` otherwise.

A palindrome is a word that is spelled the same backwards.

*Do not use the `reversed()` or `reverse()` functions.*

```
def palindrome(string):
  """
  >>> palindrome('a')
  True
  >>> palindrome('ab')
  False
  >>> palindrome('aba')
  True
  >>> palindrome('abba')
  True
  """
  
  ### ANSWER ###
  for i in range(len(string) // 2)):
    left = string[i]
    right = string[len(string) - i - 1]
    if left != right:
      # If we've found any corresponding characters that don't match, it isn't a palindrome
      return False
    # Otherwise it is
    return True
```

### Q5 Remove duplicates
Given a list, remove all of the duplicates in the list. Return the resulting list.

```
def remove_duplicates(lst):
  """
  >>> remove_duplicates([1, 2, 1, 3, 1, 2, 1])
  [1, 2, 3]
  """
  
  ### ANSWER ###
  items = {} # Dictionary to mark unique elements in list
  
  #### --EITHER-- ####
  to_remove = []
  for i in range(len(lst)):
    if not items[lst[i]]:
      to_remove.append(i)
      items[lst[i]] = True
  
  for i in range(len(to_remove) - 1, -1, -1):
    lst.pop(i)
  return lst
  
  #### --OR-- ####
  for i in range(len(lst) - 1, -1, -1):
    if not items[lst[i]]:
      lst.pop(i)
      items[lst[i]] = True
  return lst
```


### Q6 Valid parentheses
Given a string, return `True` if the parentheses are in a valid format, meaning all of the opened parentheses are closed, and there are no lingering closing parentheses.

```
def valid_parentheses(string):
  """
  >>> valid_parentheses('(')
  False
  >>> valid_parentheses(')')
  False
  >>> valid_parentheses('()')
  True
  >>> valid_parentheses('((())())')
  True
  """
  
  ### ANSWER ###
  left = 0
  for c in string:
    if c == '(':
      left += 1
    if c == ')':
      if left == 0: # seeing right parenthesis before left
        # ')(' is not valid
        return False
   return left == 0
```

## Practice Final 2

### Q1 What would Python print?

```
bar = Foo(1, 2)
bar.foo('foo')

### ANSWER ###
foo?foo
```

```
bar = Bar(3, 1)
bar.foo('bar')

### ANSWER ###
Error
```

```
foo = Bar(1, 5)
foo.bar(2)

### ANSWER ###
5
```

```
foo = Bar(4, 1)
bar = Foo(1, 0)
bar.bar(foo)

### ANSWER ###
foo?0
```

```
foo = Bar(4, 1)
bar = Foo(1, 2)
bar.bar(foo)

### ANSWER ###
foo?2
```


### Q2 Is Prime?
Complete the function `is_prime(number)` that returns `True` if `number` is a prime number, `False` otherwise.

```
def is_prime(number):
  """
  >>> is_prime(1)
  False
  >>> is_prime(2)
  True
  >>> is_prime(4)
  False
  >>> is_prime(7607)
  True
  >>> is_prime(5649)
  False
  """
  
  ### ANSWER ###
  for factor in range(2, number):
    if number % factor == 0:
      return False
  return True
```
