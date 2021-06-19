# PEP 8 - Style guide for python code 

Source <br>
[link 1](https://www.python.org/dev/peps/pep-0008/)
[link 2](https://pep8.org/)

Code Layout
- Indentation
- Tabs or Space
- Maximum line length
- Line break
- Blank lines
- Source file encoding
- Imports
- Module level dunder names

> Indentation

Use 4 spaces per indentation level.

```python
# Aligned with opening delimiter.
foo = long_function_name(var_one, var_two,
                         var_three, var_four)

# More indentation included to distinguish this from the rest.
def long_function_name(
        var_one, var_two, var_three,
        var_four):
    print(var_one)

# Hanging indents should add a level.
foo = long_function_name(
    var_one, var_two,
    var_three, var_four)
```

> Tabs or Spaces?

Spaces are the preferred indentation method.

```python
with open('/path/to/some/file/you/want/to/read') as file_1, \
     open('/path/to/some/file/being/written', 'w') as file_2:
    file_2.write(file_1.read())

```

> Should a line braak before or after a binary operator?

```python
# Yes: easy to match operators with operands
income = (gross_wages
          + taxable_interest
          + (dividends - qualified_dividends)
          - ira_deduction
          - student_loan_interest)

```

> Blank lines

Surround top-level functin and class definitions with two blank lines.

Methos definitins inside a class are surrounded by a single blank lines.

```python
CONSTANT = 20


def top_level_function:
	pass


class Class_name:

	def Method_name():
		pass

print(name)

```

> Source file encoding

All identifiers in the Python standard library must use ASCII only identifiers, and should use english words wherever feasible. In addition, string literals and comments must also be in ASCII.

> Imports

Imports should useually be on separate lines

```python
import os
import sys

```

Import are always put at the top of the file, just after any module comments and docstrings, and before module globals and constants.

Import should be group in the following order:
1. standard library imports
2. related third party imports
3. local applicatin/ library specific imports
You should put a blank line between each group of imports.

> Module level dunder names

Module level dunders should be placed after the module docstring but befor any import statements except from __future__ imports.

```python
"""This is the example module.

This module does stuff.
"""

from __future__ import barry_as_FLUFL

__all__ = ['a', 'b', 'c']
__version__ = '0.1'
__author__ = 'Cardinal Biggles'

import os
import sys

```

> String Quotes

Single-quoted strings and double-quoted strings are same in python. Pick a rule and stick to it.

> Whitespace in expressions and statements

```python
# Immediately inside parentheses, brackets or braces:
spam(ham[1], {eggs: 2})

# Between a trailing comma and a following close parenthesis:
foo = (0,)

# Immediately before a comma, semicolon, or colon:
if x == 4: print x, y; x, y = y, x

# However in a slice the colon
ham[1:9], ham[1:9:3], ham[:9:3], ham[1::3], ham[1:9:]
ham[lower:upper], ham[lower:upper:], ham[lower::step]
ham[lower+offset : upper+offset]
ham[: upper_fn(x) : step_fn(x)], ham[:: step_fn(x)]
ham[lower + offset : upper + offset]

# Immediately before the open parenthesis that starts the argument list of a function call:
spam(1)

# Immediately before the open parenthesis that starts an indexing or slicing:
dct['key'] = lst[index]

# More than one space around an assignment (or other) operator to align it with another.
x = 1
y = 2
long_variable = 3

```

> Other recommendations

Avoid trailing whitespace anywhere

Always surround these binary operators with a single space on either side: assignment (=), augmented assignment (+=, -= etc.), comparisons (==, <, >, !=, <>, <=, >=, in, not in, is, is not), Booleans (and, or, not).

If operators with different priorities are used, consider adding whitespace around the operators with the lowest priority(ies). Use your own judgment;

```python
i = i + 1
submitted += 1
x = x*2 - 1
hypot2 = x*x + y*y
c = (a+b) * (a-b)

```

Don't use spaces around the = sign when used to indicate a keyword argument or a default parameter value.

```python
def complex(real, imag=0.0):
    return magic(r=real, i=imag)

```

Function annotations should use the normal rules for colons and always have spaces around the -> arrow if present.

```python
def munge(input: AnyStr): ...
def munge() -> AnyStr: ...
```

When combining an argument annotation with a default value, use spaces around the = sign
```python
def munge(sep: AnyStr = None): ...
def munge(input: AnyStr, sep: AnyStr 
```

Compound statements (multiple statements on the same line) are generally discouraged.

```python
if foo == 'blah':
    do_blah_thing()
do_one()
do_two()
do_three()
```

> When to user trailing commas

Trailing commas are usually optional, except they are mandatory when making a tuple of one element 

```python
FILES = ('setup.cfg',)
```

```python
FILES = [
    'setup.cfg',
    'tox.ini',
    ]
initialize(FILES,
           error=True,
           )
```

> Comments

Comments should be complete sentences. If a comment is a phrase or sentence, its first word should be capitalized, unless it is an identifier that begins with a lower case letter

**Block Comments**
 Each line of a block comment starts with a # and a single space

**Inline Comments**
Use inline comments sparingly. Don't state the obvious.

```python
x = x + 1                 # Compensate for border
```

> Documentation String

Write docstrings for all public modules, functions, classes, and methods. Docstrings are not necessary for non-public methods, but you should have a comment that describes what the method does. This comment should appear after the def line.

```python
"""Return a foobang

Optional plotz says to frobnicate the bizbaz first.
"""

```

> Naming Conventions

Naming styles
Name to avoid
Package and module names
Class names
Type variable names
Exception names
Global variable names
Function names
Function and method argumets
Constants

> Progamming recommendations

```python
# Use is not operator rather than not ... is.
if foo is not None:
	pass

# Always use a def statement instead of an assignment statement that binds a lambda expression directly to an identifier
def f(x): return 2*x

# for all try/except clauses, limit the try clause to the absolute minimum amount of code necessary. 
try:
    value = collection[key]
except KeyError:
    return key_not_found(key)
else:
    return handle_value(value)

# Be consistent in return statements. Either all return statements in a function should return an expression, or none of them should. 

def foo(x):
    if x >= 0:
        return math.sqrt(x)
    else:
        return None

def bar(x):
    if x < 0:
        return None
    return math.sqrt(x)

# startswith() and endswith() are cleaner and less error prone.
if foo.startswith('bar'):

# Object type comparisons should always use isinstance() instead of comparing types directly:
if isinstance(obj, int):

```

> Function Annotations




