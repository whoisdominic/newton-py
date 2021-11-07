# Newton-Python

## Why

Boiler that includes commands and some useful python code

Create virtual enviornment

```bash
python3 -m venv env
```

Activate enviornment

```bash
source env/bin/activate
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
