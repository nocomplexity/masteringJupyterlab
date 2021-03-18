# Magic commands tips

In this section some solutions for JupyterLab use for more demanding users.



## Get the cell output to use in a variable

IPython's output caching system defines several global variables:

-    [_] (a single underscore): stores previous output, like Python’s default interpreter.
-    [__] (two underscores): next previous.
-    [___] (three underscores): next-next previous.

Additionally, after each output x is created, there is a variable `_<x>` created with the output as its value. 

For example:


```python
x= [i for i in range(7)]
```


```python
x
```




    [0, 1, 2, 3, 4, 5, 6]




```python
y=_3 #the output of cell 2 , you could use also y=__
```


```python
y
```




    [0, 1, 2, 3, 4, 5, 6, 12]




```python
y.append(12)
```


```python
y
```




    [0, 1, 2, 3, 4, 5, 6, 12, 12]




```python
type(y)
```




    list



## Display docstrings 

You can place the ? character before or after (no space allowed) the object you are looking for docs.

Example:



```python
?print
```

```python
    Docstring:
    print(value, ..., sep=' ', end='\n', file=sys.stdout, flush=False)
    
    Prints the values to a stream, or to sys.stdout by default.
    Optional keyword arguments:
    file:  a file-like object (stream); defaults to the current sys.stdout.
    sep:   string inserted between values, default a space.
    end:   string appended after the last value, default a newline.
    flush: whether to forcibly flush the stream.
    Type:     builtin_function_or_method

```


## Display source code


To access the source code simply use ?? instead. 

Example to get the source code of the pprint command:


```python
??pprint
```

```python
source:
    @line_magic
    def pprint(self, parameter_s=''):
        """Toggle pretty printing on/off."""
        ptformatter = self.shell.display_formatter.formatters['text/plain']
        ptformatter.pprint = bool(1 - ptformatter.pprint)
        print('Pretty printing has been turned',
              ['OFF','ON'][ptformatter.pprint])
```
