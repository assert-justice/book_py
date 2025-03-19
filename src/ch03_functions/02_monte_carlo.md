# Monte Carlo Sims

Now that we have functions, let's use them to solve problems!

We'll be working with random numbers so we need to import a module from the Python standard library. What does that mean? Well Python provides a lot of functionality in its standard library. This is code written by other people that we can import into our program with the `import` keyword. We're going to be using the random module, which has a function called random that returns a random float between 0 and 1.

```python
import random

for i in range(10):
    print(random.random())
```

Let's write a function that flips a coin.

```python
import random
def coin():
    if random.random() < 0.5:
        return "heads"
    else:
        return "tails"

for i in range(10):
    print(coin())
```

Suppose I tell you a box has two coins in it, and at least one of them is heads up. What are the chances one of them is showing tails?

I promise this problem is less trivial than it sounds.

```python
import random
def coin():
    if random.random() < 0.5:
        return "heads"
    else:
        return "tails"

def trial():
    while True:
        a = coin()
        b = coin()
        if a == "tails" and b == "tails":
            pass
        else:
            return a == "tails" or b == "tails"

had_tails = 0
num_trials = 100
for i in range(num_trials):
    if trial():
        had_tails += 1
print(had_tails/num_trials)
```