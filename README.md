# pymy

## Overview
pymaibool is a library for adding ambiguity to bool.  

## Usage
```python
from pymaibool import pBool

# credibility: 50%
b = pBool(0.5)

print(b)
print(b)
print(b)
```
```
True
True
False
```

## Methods
### .get(true: Any, false: Any)
```python
# True
b = pBool(1)

print(b.get("yes", "no"))
```
```
yes
```
### .fix()
Fix the return to last return
```python
b = pBool(0.5)

for i in range(10):
    print(b)
    if i == 4:
        print("fix")
        b.fix()
```
```
True
False
False
True
True
fix
True
True
True
True
True
```

### .unfix()
Release fix()
```python
b = pBool(0.5)
# fix it
b.fix()

for i in range(10):
    print(b)
    if i == 4:
        print("unfix")
        b.unfix()
```
```
True
True
True
True
True
unfix
False
False
True
False
True
```

## version
0.1.0

## Github
https://github.com/toripppppy/pymai