# Interlude: The Collatz Conjecture

Dun dun dunnnn. It's not too scary I promise. Consider the following given procedure:

- Take a number n
- If it is even divide it by 2
- Otherwise multiply it by 3 and add 1

You can repeat this process as many times as you like. What happens?

Well the Collatz Conjecture says that every number will eventually get to 1. It's a conjecture because mathematitians simply don't know how to prove one way or another. A whole bunch of numbers have been tried and they all eventually make it to one. Let's take this repeated procedure and turn it into a loop.

```python
n = 7
steps = 0
while n > 1:
    if n % 2 == 0:
        n = n // 2
    else:
        n = n * 3 + 1
    print(n)
    steps += 1
print("steps:", steps)
```
