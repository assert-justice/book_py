# Lists

Before we talked about how variables are like buckets. Well a list is like a row of buckets, or like a shelf of numbered cubby holes. For all of the following examples we'll be using this list of integers.

```python
l = [3, 5, 7, 9, 11]
```

## Indices

We want to be able to use the contents of one of the cubby holes, read it and change it. We do that by using its index. You can see the first number in the list is 3. That's at index 0. In Python like most (but not all!) languages the index of the first element is 0. We use brackets to index a list like so:

```python
l = [3, 5, 7, 9, 11]

print(l[0]) # prints 3
print(l[1]) # prints 5
```

We can also change the contents of an element just like we would assign to a variable.

```python
l = [3, 5, 7, 9, 11]

print(l) # prints [3, 5, 7, 9, 11]

l[2] = 20

print(l) # prints [3, 5, 20, 9, 11]
```

We can get the length of a list with the `len` function. 

```python
l = [3, 5, 7, 9, 11]

print(len(l)) # prints 5
```

So far so good.

What happens if you try to access an element outside of a list? Well the short answer is that Python yells at you.

```python
l = [3, 5, 7, 9, 11]

print(l[5]) # error
```

As you write bigger and more complex programs you'll spend plenty of time looking at errors. Errors are your friend, they tell you where you messed up. The worst kind of bugs produce no errors at all. It should go without saying but when you get an error read it and try to understand what it means. Look it up if you have to.

## While Loops, again

Suppose we want to print out each element in a list, how would we go about it?

```python
l = [3, 5, 7, 9, 11]

i = 0
while i < len(l):
    print(i)
    i += 1
# prints 0-4
```

In the above snippet we haven't (yet) printed the list elements, we have printed their indices. Let's see it again.

```python
l = [3, 5, 7, 9, 11]

i = 0
while i < len(l):
    print(l[i])
    i += 1
# prints list elements
```

Suppose we want the sum of the array. We'll need another variable to keep track of the running total.

```python
l = [3, 5, 7, 9, 11]

i = 0
total = 0
while i < len(l):
    total += l[i]
    i += 1
print(total) # prints 35

avg = total / len(l)
print(avg) # prints 7.0
```

Let's take the array of numbers and double each one.

```python
l = [3, 5, 7, 9, 11]

print(l) # prints [3, 5, 7, 9, 11]

i = 0
while i < len(l):
    l[i] = l[i] * 2
    i += 1

print(l) # prints [6, 10, 14, 18, 22]
```

## Useful Methods

Lists are objects in Python. We'll get to objects and object oriented programming in time, but for now it's enough to know objects have methods. We can call methods on objects like functions and modify the object. Let's look at some examples.

### Append

Append adds stuff to the end of a list, like so.

```python
l = [3, 5, 7, 9, 11]

print(l) # prints [3, 5, 7, 9, 11]

l.append(13)

print(l) # prints [3, 5, 7, 9, 11, 13]
```

### Pop

Pop removes (or pops) the last element of the list.

```python
l = [3, 5, 7, 9, 11]

print(l) # prints [3, 5, 7, 9, 11]

val = l.pop()
print(val) # prints 11

print(l) # prints [3, 5, 7, 9]
```

## Fibonacci Sequence

```python
fib = [1, 1]
count = 10

while len(fib) < count:
    b = fib.pop()
    a = fib.pop()
    fib.append(a)
    fib.append(b)
    fib.append(a + b)

print(fib)
```