# Function Scope

Variables in functions are treated differently.

```python
a = 10

def foo():
    print(a)

foo()
a = 20
foo()
```