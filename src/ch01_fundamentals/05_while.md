# While

Before we learn the new keyword `while` let's spend a little more time with `if`. Consider:

```python
i = 0

if i < 3:
    print(i)
    i = i+1
```

What will that print? You might be tempted to say 1 but the answer is actually 0. i is printed and *then* incremented. What does the below print?

```python
i = 0

if i < 3:
    print(i)
    i = i+1

if i < 3:
    print(i)
    i = i+1

if i < 3:
    print(i)
    i = i+1

if i < 3:
    print(i)
    i = i+1
```

It prints 

```
0
1
2
```

Why not 3? Because, of course, 3 is not less than 3 so the last block is not executed.
Now, wouldn't it be helpful if, instead of all these if statements, we had a way to run code over and over again until a condition became false? Behold:

```python
i = 0

while i < 3:
    print(i)
    i = i+1
```

This prints exactly the same thing.