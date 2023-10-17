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

### Logical Operators
| Operator  | Functionality|
|:---|:---|
|and|Logical And|
|or|Logical Or|
|not|Logical Not|

## Object Oriented Programming
### Classes

```{python}
class ClassName
    variable = value               # class variable shared by all instances

    list_variable = []             # mistaken use of a class variable

def __init__(self, name) -> None:  # Instantiation operation
    self.name = name               # instance variable unique to each instance
```
### Inheritance
```{python}
class DerivedClassName(modname.BaseClassName): # base class defined in 
                                               # another module
```
#### Superclass-call

```{python}
class C(B):
    def method(self, arg):
        super().method(arg)    # This does the same thing as:
                               # super(C, self).method(arg)
```

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
## Control Flow

```{python}
if {condition}:
  expression
elif {another_condition}:
  another_expression
else:
  yet_another_expression
```
## Lists
### List Comprehension
The condition is optional.
```{python}
newlist = [expression for item in iterable if condition == True]
newlist = [x for x in iterable] 
```

## Files

* Files have a name and a path.
* The root folder is the lowest folder.
* In a file path, the folders and filename are separated by backslashes on Windows and forward slashes on Linux and Mac.
* Use the `os.path.join()` function to combine folders with the correct slash.
* The current working directory is the folder that any relative paths are relative to.
* `os.getcwd()` will return the current working directory.
* `os.chdir()` will change the current working directory.
* Absolute paths begin with the root folder, relative paths do not.
* The `.` folder represents "this folder", the `..` folder represents "the parent folder".
* `os.path.abspath() returns an absolute path form of the path passed to it.
* `os.path.relpath() returns the relative path between two paths passed to it.
* `os.makedirs()` can make folders.
* `os.path.getsize()` returns a file's size.
* `os.listdir()` returns a list of strings of filenames.
* `os.path.exists()` returns True if the filename passed to it exists.
* `os.path.isfile()` and `os.path.isdir()` return True if they were passed a filename or file path.

## Command Line Arguments
```{python}
import sys
print(sys.argv)
```
## Logging
* The `logging` module lets you display logging messages.
* Log messages create a "breadcrumb trail" of what your program is doing.
* After calling `logging.basicConfig()` to set up logging, call `logging.debug(‘This is the message')` to create a log message.
* When done, you can disable the log messages with `logging.disable(logging.CRITICAL)`
* Don't use `print()` for log messages: It's hard to remove the mall when you're done debugging.
* The five log levels are: `DEBUG`, `INFO`, `WARNING`, `ERROR`, and `CRITICAL`.
* You can also log to a file instead of the screen with the filename keyword argument in the `logging.basicConfig()` function.

## Modules


```{python}
import module                 
from module import keyword
from module import *        # import everyting from module 
import modules as m         # alias import
``````

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
