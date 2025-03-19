# Expressions

An expression is a bit of code that evaluates to something.

## Literals

Let's look at our Hello World program again:

```python
print("Hello World!")
```

The string "Hello World!" appears in our source code, it's not read from a file or input from the user or something like that. That makes it a literal. Here is another example.

```python
print(10)
```

Likewise, the value `10` is embedded in the source code itself. We'll see the alternative... right now actually.

## Operators

```python
print(5 + 5)
```

It shouldn't be any great wonder what the above prints when we run it. Here we have two literal values and we are adding them with the plus sign. The plus sign is an example of an operator, it performs an operation. In this case the operation is addition. Let's look at some more examples.

```python
print(5 + 5) # prints 10
print(5 - 5) # prints 0
print(5 * 5) # prints 25
print(5 / 5) # prints 1.0
```

No surprises here. The only curious one is the last one, you'll notice it prints `1.0` instead of just `1`. Why? Well in Python when you divide one number by another the result is always a float, even if the input numbers were integers.

```python
print(5 / 2) # prints 2.5
```

Similarly if you add or multiply a float with an integer the result is a float. This is an example of something called Type Coercion, and it's otherwise pretty rare in Python. JavaScript and PHP are infamous for it though. Just file that away somewhere.

```python
print(5 + 5 * 2)    # prints 15
print( (5 + 5) * 2) # prints 20
```

Order of operations is respected. So multiplication and division go before addition and subtraction. You can use parentheses to ensure part of the expression is evaluated first.

Finally there are the comparison operators.

```python
print(5 == 5) # prints True
print(5 != 2) # prints True
print(2 < 5)  # prints True
print(2 > 5)  # prints False
print(5 <= 5) # prints True
print(9 >= 5) # prints True
```

The `==` operator checks for equality. If two numbers are the same it evaluates to the boolean value `True`. Otherwise `False`.

`!=` means not equals. It evaluates to `True` if the two things are *not* equal, otherwise `False`. We'll spend more time with the comparison operators soon, when we get to if statements.
