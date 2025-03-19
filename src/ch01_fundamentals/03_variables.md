# Variables

```python
a = 10
print(a) # prints 10
```

Taking a look at the above, hopefully it's intuitive enough coming from a math background. Let's talk about it anyway.

Here we are creating a variable `a` and we are *assigning* it a value of `10`. Variables are like buckets. We have a bucket with `a` painted on the side and we can store a value in it, in this case the integer `10`. We can then refer to the value stored in `a` and print it out. So far so good.

```python
a = 10
print(a + 5) # prints 15
```

The above should also follow from our understanding. `a` contains a value we can use in expressions like any other. What do you think the following will print out?

```python
a = 10
a = 20
print(a)
```

In math the above would be nonsense. `a` can't both equal `10` and `20`! Well in Python, as well as most (but not all!) programming languages variables are not constant. They can be reassigned. This is how we can read the above code:

- Create a variable `a`.
- Set `a` to `10`.
- Dump out the old value of `a` and replace it with `20`.
- Print the current value of `a`, which is `20`.

Let's test our understanding. What will the following print out?

```python
a = 10
b = 20
c = a + b
print(c)
```

It prints out `30`! The variable `c` is set to the result of `a` plus `b`. Ok, now for a tricky one.

```python
a = 10
b = 20
c = a + b
b = 5
print(c) # what does it print?
```

It still prints `30`. Why? Let's step through it.

- Create a variable `a` and set it to `10`.
- Create a variable `b` and set it to `20`.
- Create a variable `c` and set it to the result of `a + b`, which is `30`.
- Reassign `b` to equal `5`. Note that the value of `c` has not changed.
- Print `c`

In other words `c = a + b` is only true at the moment that line is executed. It is *not* necessarily true after that. `c` doesn't know or care where it got its values from, it only knows it contains a `30`. Make sense? Ok, one more concept.

```python
a = 10
a = a + 5
print(a) # what does it print?
```
