# Character Tally

```python
text = """I know someone who kisses the way
a flower opens, but more rapidly.
Flowers are sweet. They have
short, beatific lives. They offer
much pleasure. There is
nothing in the world that can be said
against them.
Sad, isn’t it, that all they can kiss
is the air.
 
Yes, yes! We are the lucky ones.
"""
# I Know Someone, by Mary Oliver

tally = {}

for c in text:
    if c == " ":
        pass
    elif c in tally:
        tally[c] += 1
    else:
        tally[c] = 1

char = ''
freq = 0
for key in tally:
    if tally[key] > freq:
        freq = tally[key]
        char = key
print(char, freq)
```