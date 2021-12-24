# Newton-Python

Boiler that includes commands and some useful python code

## Useful commands

Create virtual enviornment

```bash
python3 -m venv env
```

Activate enviornment

```bash
source env/bin/activate
```

Freeze dependencies

```bash
pip freeze > requirements.txt.
```

## The Zen of Python, by Tim Peters

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than _right_ now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.

## Run REPL

```bash
python3
```

## Helpful commands

```python
type()
```

Python has a very easy way of determining the type of something: with the type() function.

Just pass any object into the `type()` method:

```python
name = "Adam"
type(name)
```

```python
dir()
```

`dir()` stands for directory.

If we check the type of str (notice, no quotes here) in the REPL, we’ll see all the methods available on strings in Python.

We’ll use some of these methods later in the day.

```python
help()
```

The last useful method is `help()`.
You can pass a type, method, or other object to help() to instantly see available documentation about the method, the parameters it expects, and what it returns.

```python
help(str.isupper)
```

#### Reverse an iterable
```python
iterableVar[::-1]
```

## Understanding slice notation

It's pretty simple really:

```python
a[start:stop]  # items start through stop-1
a[start:]      # items start through the rest of the array
a[:stop]       # items from the beginning through stop-1
a[:]           # a copy of the whole array
```
There is also the step value, which can be used with any of the above:

```python
a[start:stop:step] # start through not past stop, by step
```

The key point to remember is that the  `:stop`  value represents the first value that is  _not_  in the selected slice. So, the difference between  `stop`  and  `start`  is the number of elements selected (if  `step`  is 1, the default).

The other feature is that  `start`  or  `stop`  may be a  _negative_  number, which means it counts from the end of the array instead of the beginning. So:

```python
a[-1]    # last item in the array
a[-2:]   # last two items in the array
a[:-2]   # everything except the last two items
```

Similarly,  `step`  may be a negative number:

```python
a[::-1]    # all items in the array, reversed
a[1::-1]   # the first two items, reversed
a[:-3:-1]  # the last two items, reversed
a[-3::-1]  # everything except the last two items, reversed
```

Python is kind to the programmer if there are fewer items than you ask for. For example, if you ask for  `a[:-2]`  and  `a`  only contains one element, you get an empty list instead of an error. Sometimes you would prefer the error, so you have to be aware that this may happen.

### Relation to  `slice()`  object

The slicing operator  `[]`  is actually being used in the above code with a  `slice()`  object using the  `:`  notation (which is only valid within  `[]`), i.e.:

```python
a[start:stop:step]
```

is equivalent to:

```python
a[slice(start, stop, step)]
```

Slice objects also behave slightly differently depending on the number of arguments, similarly to  `range()`, i.e. both  `slice(stop)`  and  `slice(start, stop[, step])`  are supported. To skip specifying a given argument, one might use  `None`, so that e.g.  `a[start:]`  is equivalent to  `a[slice(start, None)]`  or  `a[::-1]`  is equivalent to  `a[slice(None, None, -1)]`.

While the  `:`-based notation is very helpful for simple slicing, the explicit use of  `slice()`  objects simplifies the programmatic generation of slicing.
