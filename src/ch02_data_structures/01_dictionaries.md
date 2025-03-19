# Dictionaries

Python has this thing called dictionaries. This is a data structure that associates keys with values.

I like the name dictionary because it's intuitive. You have a word you want to look up, that's the key, and you have some data you want to look up, the definition. That's the value.

Another analogue example is a phone book.

```python
pb = {
    "mary": 1111,
    "sally": 2222,
    "eric": 3333,
    "joe": 4444,
}

# look up joe's number
print(pb["joe"])

# change sally's number
pb["sally"] = 5555

# add a new entry to pb
pb["alice"] = 6666

# trying to read a nonexistent key is an error!
print(pb["bob"])

# we can check if a key exists with the in operator

if "bob" in pb:
    print(pb["bob"])
else:
    print("no entry for bob :(")

# we can get the size of the dictionary with len, just like lists
print(len(pb))
```