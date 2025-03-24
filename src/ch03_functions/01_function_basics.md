# Anatomy of a Function

we have already been exposed to some functions in Python, namely print and len. Now we get to write our own!

```python
def greet(): # define the function
    print("hello!") # the indented body of the function
```

Here we have defined a function called greet with the `def` keyword. If you run the snippet above it doesn't do anything! We have defined our function but we haven't actually used it yet.

```python
def greet():
    print("hello!")

greet() # here we call the function
```

Now we have. We can call greet any number of times and it will do the same thing!

```python
def greet():
    print("hello!")

greet()
greet()
greet()
```

## Passing Arguments

A function that does exactly the same thing every time isn't that helpful. We want to be able to pass the function data to work with. We do that by giving the function a parameter.

```python
def greet(name):
    print("hello", name, "!")

greet("alice") # prints "hello alice !"
```

Between the parentheses in the function definition we've added the word name. This is a parameter. A parameter is a special kind of variable that holds an argument. An argument is a value that gets passed to a function. In the above example the argument is the string "alice" and the parameter is name.

Now we can call greet multiple times with different arguments and get different results!

```python
def greet(name):
    print("hello", name, "!")

greet("alice") # prints "hello alice !"
greet("bob") # prints "hello bob !"
```

## Returning Values

Now that we can pass data to a function, it would be useful to get data out. We can do this with the `return` keyword.

```python
def doubler(x):
    return x * 2

a = 10
b = doubler(a) # store the result of doubler in b
print(b) # prints 20
print(doubler(30)) # prints 60
```

In the above example we define a function called doubler. We give it a single parameter x. In the body of the function we multiply x by 2 and return it.

What happens if we forget to return from a function?

```python
def doubler(x):
    temp = x * 2

print(doubler(30)) # prints None
```

We get a `None` back! Forgetting a return statement is a common mistake for new programmers used to printing things, watch out for that.

## The Accumulator Pattern

A common thing to do is to create a variable to hold a value that we modify over and over as we loop over something, and then return that value at the end. We saw an example of that when we summed up the contents of a list in the last chapter. Let's see how we would do that with a function.

```python
def sum(ls):
    total = 0
    for num in ls:
        total += num
    return total

print(sum([1, 2, 3])) # prints 6
print(sum([3, 5, 7, 9, 11])) # prints 35
```

The next function scans through a list looking for a given value. It returns how many times that value appears in the list.

```python
def count(ls, val):
    tally = 0
    for v in ls:
        if v == val:
            tally += 1
    return tally
```

Accumulators don't have to be numbers. In the next example our accumulator starts as an empty list. We loop through a different list, take each number, double it, and add it to the accumulator. Finally we return the accumulator.

```python
def double_list(ls):
    res = []
    for v in ls:
        res.append(v * 2)
    return res

print(double_list([1, 2, 3])) # prints [2, 4, 6]
```

## Early Return

Typically return will appear at the end of a function when it's done doing it's thing. It doesn't have to however! When Python hits a return statement it immediately exits the function it's in. It's like an eject lever. In the next example we'll write a function to check whether any numbers in a list are even. If we find one we'll return `True` immediately, we don't need to check any more. If we get to the end of the list without finding any we'll return `False`.

```python
def has_even(ls):
    for v in ls:
        if v % 2 == 0:
            return True
    return False

print(has_even([1, 2, 3])) # prints True
print(has_even([3, 5, 7, 9, 11])) # prints False
```

Functions can call other functions. Let's refactor the above example a little.

```python
def is_even(x):
    return x % 2 == 0

def has_even(ls):
    for v in ls:
        if is_even(v):
            return True
    return False

print(has_even([1, 2, 3])) # prints True
print(has_even([3, 5, 7, 9, 11])) # prints False
```

In the above example we have delegated checking whether a number is even to a helper function. We'll be writing and using plenty of helper functions in the future.
