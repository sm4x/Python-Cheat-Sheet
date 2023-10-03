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

| Pattern      | Description |
|:-------------|:-------------|
| "."          | Matches any character except a newline.|
| "^"          | Matches the start of the string.|
| "$"          | Matches the end of the string or just before the newline at the end of the string.|
| "*"          | Matches 0 or more (greedy) repetitions of the preceding RE. Greedy means that it will match as many repetitions as possible.|
| "+"          | Matches 1 or more (greedy) repetitions of the preceding RE.|
| "?"          | Matches 0 or 1 (greedy) of the preceding RE.|
| *?,+?,??     | Non-greedy versions of the previous three special characters.|
| {m,n}        | Matches from m to n repetitions of the preceding RE.|
| {m,n}?       | Non-greedy version of the above.|
|"\\\\"        | Either escapes special characters or signals a special sequence.|
|[]            | Indicates a set of characters. A "^" as the first character indicates a complementing set. (NOT)|
| "\|"         | A\|B, creates an RE that will match either A or B.|
|(...)         | Matches the RE inside the parentheses. The contents can be retrieved or matched later in the string.|
|(?aiLmsux)    | The letters set the corresponding flags defined below.|
|(?:...)       | Non-grouping version of regular parentheses.|
|(?P<name>...) | The substring matched by the group is accessible by name.|
|(?P=name)     | Matches the text matched earlier by the group named name.|
|(?#...)       | A comment; ignored.|
|(?=...)       | Matches if ... matches next, but doesn't consume the string.|
|(?!...)       | Matches if ... doesn't match next.|
|(?<=...)      | Matches if preceded by ... (must be fixed length).|
|(?<!...)      | Matches if not preceded by ... (must be fixed length).|
|(?(id/name)yes|no)| Matches yes pattern if the group with id/name matched, the (optional) no pattern otherwise.|




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

**Note:**
`re.compile(

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
