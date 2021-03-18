# Passing variables to shell commands

Shell commands in the notebook are executed in a temporary subshell.

Communication in the other direction–passing Python variables into the shell–is possible using the `{varname}` syntax:

```python
message = "hello from Python"
```

and use in another cell:
```
!echo {message}
```

The cell output will be:

`hello from Python`

The curly braces contain the variable name, which is replaced by the variable’s contents in the shell command.

For more tips like this one: see the `%magic` IPython commands and the section with a quick overview in this publication.


