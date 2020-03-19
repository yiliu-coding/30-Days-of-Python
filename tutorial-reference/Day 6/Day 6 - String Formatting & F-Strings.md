# Day 6 - String Formatting & F-Strings
Python has ways to make writing text a bit more programmic and helps systematically remove repeating youself.

Also, check out:
- [pyformat](https://pyformat.info/)
- [strftime.org](https://strftime.org/)

### String Formatting

Basic formatting:

`#`: Write a comment `# this is a comment`

`\n`: New Line

`\t`: Tab

`\\` or `//`: Allowed Slash

`\'`: Allowed Single Quote

`\"`: Allowed Double quote

`{{` or `}}`: Allowed signle curly bracket in formatted strings

`"your single-line text"`: Wrap a single quote (`'`) or double quote (`"`) around text / numbers to make it a string.

`\`: A `slash` in front of a `return`/`enter` will escape that. Allowing for multi-line strings without the triple quotes. Such as:
```python
"this is my string example\
when I close it here"
```


`""" your multi-line text"""`: Wrap 3x single quotes (```) or 3x double quotes (`"`) around a lot of text to allow for multi-line strings. Such as:
```python
"""this is my string example
when I close it here"""
```



#### The `.format()` method

_Empty_
```python
"{} {}".format("Hello", "World")
```

_Positional_
```python
"{0} {1} {0}".format("Hello", "World")
```

_Keyword_
```python
"{first} {second} {first}".format(first="Hello", second="World")
```

_Positional & Keyword_
```python
"{0} {second} {0}".format("Hello", second="World")

"{0} {1} {2['hello']}".format("Hello", "World", {'hello': 'sup'})
```

_Unpacking a Dictionary_
```python
data = {'name': 'Hodor', 'email': 'holdthe@door.com'}
txt = 'Name: {name}\nEmail: {email}'.format(**data)
print(txt)
```

_Numbers, Floats & Decimals_

Number / Integer
```python
"{:d}".format(32)
```
or
```python
"{}".format(32)
```

Float / Decimal
```python
"{:f}".format(32)
```

```python
pi = 3.14159265359
"{:f}".format(pi)
```

Limit to `n` decimal places. Replace `4` below with the number of decimal places to round to.
```python
pi = 3.14159265359
"{:.4f}".format(pi)
```



#### The `%` method

_Positional - Strings or Numbers_
```python
"%s %s %s %s" % ("Hello", 12, 131.312, {'hello': 'sup'})
```

_Keyword / Dictionary_
```python
"%(first)s %(second)s" % {"first":"Hello", "second":"World"}
```

_Keywords_ (Also known as named placeholders)
```python
data = {'name': 'Hodor', 'email': 'holdthe@door.com'}
txt = 'Name: %(name)s\nEmail: %(email)s' % data
print(txt)
```

_Numbers, Floats & Decimals_

Number
```python
"%d" % (32)
```
or
```python
"%s" % (32)
```

Float
```python
"%f" % (32)
```

```python
pi = 3.14159265359
"%f" % (pi)
```

Limit to `n` decimal places. Replace `2` below with the number of decimal places to round to.
```python
pi = 3.14159265359
"%.2f" % (pi)
```

#### `f` Strings (aka `f-string`)

_Strings or Number variables_
```python
first = "Hello"
second = "World"
third = 32.3122
fourth = "{:.2f}".format(third)
f"{first} {second} {first.upper()} {third} {fourth}"
```

_Dictionary_
```python
data = {'name': 'Hodor', 'email': 'holdthe@door.com'}
txt = f'Name: {data["name"]}\nEmail: {data["email"]}'
print(txt)
```

_Inline Math_
```python
hours = 21
seconds = 32
f"{hours} {seconds * 10} {seconds}"
```

_Inline Formatting_


```python
pi = 3.14159265359
f"{format(pi, '.2f')}"
```