That: Python Hidden Code
========================


Table of Contents
-----------------

- [Easter Eggs](https://github.com/mahanmarwat/that#easter-eggs)
- [Geek](https://github.com/mahanmarwat/that#geek)
- [Idioms](https://github.com/mahanmarwat/that#idioms)
- [Less Known Feature](https://github.com/mahanmarwat/that#less-known-feature)
- [Don't Do It](https://github.com/mahanmarwat/that#dont-do-it)
- [Command Line](https://github.com/mahanmarwat/that#command-line)
- [Extend Python](https://github.com/mahanmarwat/that#extend-python)
- [One Liner](https://github.com/mahanmarwat/that#one-liner)
- [Quotes](https://github.com/mahanmarwat/that#quotes)
- [Jokes](https://github.com/mahanmarwat/that#jokes)
- [Tools](https://github.com/mahanmarwat/that#tools)
- [Guides](https://github.com/mahanmarwat/that#guides)

Easter Eggs
-----------

#### 1. Zen of Python

```python
import this
```

#### 2. Open [Python xkcd](http://imgs.xkcd.com/comics/python.png) link in browser

```python
import antigravity
```

#### 3. Braces for code block

```python
from __future__ import braces
```

#### 4. Print `Hello world!` to `stdout`

```python
import __hello__
```

Geek
----

#### 1. Using braces in Python

```python
if x == 1: #{
    print('hello')
#}
```

#### 2. Unicode variable names

```python
ünÏcode = 'hello'
```

#### 3. Default value

```python
x = False
y = x or 5 # if x is False, y will hold the default value 5.
```

#### 4. Log the message, if debug is True

```python
debug and log('debug message.') # if debug is True, then the message will be logged.
```

#### 5.

```python
status_headers[:] = [status, headers]
```

#### 6. Comment out portion

```python
bottle.run(app, port=8891) #, debug=True, reloader=True)
```

#### 7. Ellipses...

```python
while ...:
    print(hello)
```

#### 8. No more zero `0000`

You can use exponents instead of typing long floating point numbers.

```python
total = 1e4 # 10000.0
```

#### 9. Rot13 cipher

```python
import codecs
codecs.encode('abc', 'rot13') # or 'rot-13'
```
`str.encode` doesn't support `rot13`.

#### 10. You can split the digit from string in encoding name on anything

`utf8`, `utf-8` and `utf_8` and even `utf+_+8` is one thing.

#### 11. Last result

```python
>>> 5 + 5
>>> _
10
```
This only works in interactive interpreter.

#### 12. Accessing private properties

```python
class Hello:
    __name = 'Python'
Hello._Hello__name # accessing private property __name
```

Idioms
------

#### 1. Reversing a sequence

```python
greet = 'Hello'
greet[::-1]
```

#### 2. Removing duplicate

```python
nums = [1, 2, 2, 3]
set(nums)
```

This will produce an unordered set.

To convert it back to a list you can do the following, although the order will still be lost:

```python
nums = [1, 2, 2, 3]
list(set(nums))
```

#### 3. Element with index

```python
list = ['hello', 'world']
for index, value in enumerate(list):
    print(index, value)
# 1 hello
# 2 world
```

Less Known Feature
------------------

#### 1. She bang

```python
#!/usr/bin/env python3
```

#### 2. Declare encoding

```python
# -*- coding: utf-8 -*-
```

or

```python
# coding: uft8
```

#### 3. `self` is not a keyword

We can use any name instead of self in class defination.

```python
class Hello:
	def __init__(this, name):
		this.name = name
```

#### 4. Python file as a module and script

```python
if __name__ == '__main__':
```

#### 5. Like `if` the other `for`, `while` and `try` have else statements too

```python
while True:
	print('hello')
else:
	print('not hello')
```

#### 6. Your own type

```python
new_str_type = type('new_str_type', (str,), {})
```

#### 7. `*args` and `**kwargs`

```python
list = [1, 2]
dict = {'name': 'hello'}
def hello(one, two, name=None):
	pass
hello(*list, **dict)
```

Don't Do It
-----------

#### 1. Don't use bare bone exception

```python
try:
	int(input)
except: # instead use except TypeError:
	pass
```

#### 2. Use `None` as default parameter

Be careful: Mutable default parameters may not behave the way you think.

```python
def hello(items=[]):
    items.append('hello')
    return items
first = hello()
second = hello() # you will get ['hello', 'hello'] here
```

If you expect a new object every time, use `None` as the default instead:

```python
def hello(items=None):
    if items is None:
        items = []
    items.append('hello')
    return items
first = hello()
second = hello() # now you get ['hello']
```

Command Line
------------

#### 1. Show month calendar

```bash
python -m "calendar" 2015 9
```

For options: `python -m "calendar" --help`

#### 2. Starts a server

```bash
python -m http.server --bind 127.0.0.1 8080
```
For options: `python -m http.server --help`

Extend Python
-------------

#### 1. Input cousin, `output` function

```python
output = print
```

#### 2. `multiline` function will remove the indent form the lines

```python
multiline("""Hello, How are you?
             Hello, How are you?
             Hello, How are you?""") # the function will remove the indent.
```
This one is fake yet.

#### 3. `|` command-line piping with Pipe module

```python
[1, 2, 3] | add
```

#### 4. Goto, Using goto module

```python
if x == 1:
    goto .end
```

One Liner
---------


Quotes
------


Jokes
-----


Tools
-----

#### 1. Interactive Python

- [ipython](https://github.com/ipython/ipython)

#### 2. Tool for installing Python packages

- [pip](https://github.com/pypa/pip)

Guides
------


Contributors
------------



License
-------

Licensed under [MIT](./LICENSE).
