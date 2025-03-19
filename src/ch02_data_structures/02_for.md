# For Loops

While loops are kind of annoying for simple things like looping through lists. Fortunately there is a better way.

```python
l = [3, 5, 7, 9, 11]

i = 0
while i < len(l):
    print(l[i])
    i += 1
```

```python
l = [3, 5, 7, 9, 11]

for val in l:
    print(val)
```

You can even use for to loop through the keys of a dictionary.

```python
pb = {
    "mary": 1111,
    "sally": 2222,
    "eric": 3333,
    "joe": 4444,
}

for name in pb:
    print(name, pb[name])
```

Let's use a for loop to reverse a dictionary. That is, make a new dictionary where the phone numbers are the keys and the names are values.

```python
pb = {
    "mary": 1111,
    "sally": 2222,
    "eric": 3333,
    "joe": 4444,
}

dial = {}

for name in pb:
    number = pb[name]
    dial[number] = name

print(dial)
```

Another thing you can loop over are ranges.

```python
for i in range(5):
    print(i)
```