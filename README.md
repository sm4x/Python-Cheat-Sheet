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
#### Sepecial Characters

| Pattern      | Description |
|:-------------|:-------------|
|`"."`| Matches any character except a newline. "See Flags" below.|
|`"^"`| Matches the start of the string.|
|`"$"`| Matches the end of the string or just before the newline at the end of the string.|
|`"*"`| Matches 0 or more (greedy) repetitions of the preceding RE. Greedy means that it will match as many repetitions as possible.|
|`"+"`| Matches 1 or more (greedy) repetitions of the preceding RE.|
|`"?"`| Matches 0 or 1 (greedy) of the preceding RE.|
|`*?`,+?`,`??`| Non-greedy versions of the previous three special characters.|
|`{m,n}`| Matches from m to n repetitions of the preceding RE.|
|`{m,n}?`| Non-greedy version of the above.|
|`"\\"`| Either escapes special characters or signals a special sequence.|
|`[]`| Indicates a set of characters. A "^" as the first character indicates a complementing set. (NOT)|
|`"\|"`| A\|B, creates an RE that will match either A or B. Multiple Instances possible.|
|`(...)`| Matches the RE inside the parentheses. The contents can be retrieved or matched later in the string.|
|`(?aiLmsux)`| The letters set the corresponding flags defined below.|
|`(?:...)`| Non-grouping version of regular parentheses.|
|`(?P<name>...)`| The substring matched by the group is accessible by name.|
|`(?P=name)`| Matches the text matched earlier by the group named name.|
|`(?#...)`| A comment; ignored.|
|`(?=...)`| Matches if ... matches next, but doesn't consume the string.|
|`(?!...)`| Matches if ... doesn't match next.|
|`(?<=...)`| Matches if preceded by ... (must be fixed length).|
|`(?<!...)`| Matches if not preceded by ... (must be fixed length).|
|`(?(id/name)yes\|no)`| Matches yes pattern if the group with id/name matched, the (optional) no pattern otherwise.|

#### Special Sequences
| Sequence | Description |
|:---------|-----------------------------------------------------------------------------|
|`\number` | Matches the contents of the group of the same number.
|`\A`| Matches only at the start of the string.|
|`\Z`| Matches only at the end of the string.|
|`\b`| Matches the empty string, but only at the start or end of a word.|
|`\B`| Matches the empty string, but not at the start or end of a word.|
|`\d`| Matches any decimal digit; equivalent to the set `[0-9]` in bytes patterns or string patterns with the ASCII flag. In string patterns without the ASCII flag, it will match the whole range of Unicode digits.|
|`\D`| Matches any non-digit character; equivalent to `[^\d]`.|
|`\s`| Matches any whitespace character; equivalent to `[ \t\n\r\f\v]` in bytes patterns or string patterns with the ASCII flag. In string patterns without the ASCII flag, it will match the whole range of Unicode whitespace characters.|
|`\S`| Matches any non-whitespace character; equivalent to `[^\s]`.
|`\w`| Matches any alphanumeric character; equivalent to `[a-zA-Z0-9_]` in bytes patterns or string patterns with the ASCII flag. In string patterns without the ASCII flag, it will match the range of Unicode alphanumeric characters (letters plus digits plus underscore). With LOCALE, it will match the set `[0-9_]` plus characters defined as letters for the current locale.|
|`\W`| Matches the complement of `\w.`|
|`\\`| Matches a literal backslash.|

#### Flags

| Flag | Shortcut | Description |
|:-----|:---------|:------------|
| `A` | ASCII | For string patterns, make make `\w`, `\W`, `\b`, `\B`, `\d`, `\D` match the corresponding ASCII character categories (rather than the whole Unicode categories, which is the default). For bytes patterns, this flag is the only available behaviour and needn't be specified.|
| `I` | IGNORECASE | Perform case-insensitive matching.|
| `L` | LOCALE | Make `\w`, \W, \b, \B, dependent on the current locale.|
| `M` | MULTILINE | `"^"` matches the beginning of lines (after a newline) as well as the string. `"$"` matches the end of lines (before a newline) as well as the end of the string.|
| `S` | DOTALL | `"."` matches any character at all, including the newline.|
| `X` | VERBOSE | Ignore whitespace and comments for nicer looking RE's.|
| `U` | UNICODE | For compatibility only. Ignored for string patterns (it is the default), and forbidden for bytes patterns.|

**Note:** A, L, and U are mutually exclusive.  If you want to pass multiple arguments (`re.DOTALL` , `re.IGNORECASE`, `re.VERBOSE`), combine them with the `|` bitwise operator.






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
