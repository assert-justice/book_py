# Anatomy of a Function

we have already been exposed to some functions in Python, namely print and len. Now we get to write our own!

## Passing Arguments
```python
def greet(name):
    print("hello", name, "!")

greet("alice")
```

## Returning Values

```python
def doubler(x):
    return x * 2

a = 10
b = doubler(a)
print(b)
```

## More Examples!

```python
def count(ls, val):
    tally = 0
    for v in ls:
        if v == val:
            tally += 1
    return tally
```

```python
def mul_list(ls, factor):
    res = []
    for v in ls:
        res.append(v * factor)
```