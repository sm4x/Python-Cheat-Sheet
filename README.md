# Python-Cheat-Sheet
## Data Types
### Base types

* integer
* float
* boolean
* string 
* bytes

### Container Types

| Data Type  |  Ordered |  Mutability  |
|:-----------|---|---|
| list|||
|tuple|||
|str bytes|||
|dict|||
|set|||
|frozenset|||
## Comments

### Single line comment
```{python}
# This is a comment
```
### Multi-line comment
```{python}
'''
This is
a multi-line
comment
'''
```
| Operator  |   |   |   |
|:---|:---|---|---|
|+|Addition|   |   |
|-|Subtraction|   |   |
|*|Multiplication|   |   |
|/|Division|   |   |
|//|Integer Division|   |   |
|%|Modulus   |   |   |

### Comparison Operators
| Operator  | Functionality|
|:---|:---|
|==|Equal to|
|!=|Not equal to|
|<|Less than|
|>|Greater than|
|<=|Less than or equalto|
|>=|Greater than or qual to|
## Regular expressions
### Import module
```{python}
import re
```
### Regular Expression object
```{python}
re_object = re.compile(r'{regular expression}) # usually raw strings because of frequent backslash (\) use
```
#### Regular expression 
```{python}
re_object.search({text})      # returns match object
re_object.findall({text})     # returns list
mo.group()                    # returns the match object's matched string
```
### Pattern matching

|Operator||
|:---|:---|
|\d|numeric digits [0..9]|
|\D|NOT (numeric digits [0..9])|
|\w|letter,numeric digits [0..9], _|
|\W|NOT (letter,numeric digits [0..9], _)|
|\s|space, tab, newline|
|\S|NOT (space, tab, newline)|
|?| 0 or 1 times|
|*| 0 or more times|
|+| 1 or more times|
|{x}| x number of times|
|{x,y}|min x and max y number of times|
|{x,y}?| nongreedy match|
|[a-zA-Z]|Character classes a..z and A..Z|
|^[a-zA-Z]| NOT (a..z and A..Z)|
|:---|:---|
|^Pattern|String must start with Pattern|
|Pattern$|String must end with Pattern|
|^Pattern$|Entire String must match Pattern|
|.|wildcard - any character except newlines|
|.*|match everything except newline|

```{python}
re_object = re.compile(r'First Name: (.*) Last Name: (.*)')
re_object.findall('First Name: John Last Name: Doe')
[('John'),('Doe')]
```

## Command Line Arguments
```{python}
import sys
print(sys.argv)
```

## Virtual Environments
### Create Virtual Environment
```{bash}
python -m venv .venv
```

### Activate Virtual Environment
```{bash}
source .venv/bin activate
```
### Dectivate Virtual Environment
```{bash}
deactivate
```
### Upgrade pip


```{bash}
pip install --upgrade pip
```
