# Running asyncio 


```{warning} 
Using `asyncio` in a notebook **is NOT trivial**

```

But it can be done.


If done wrong the error message: 
> *This event loop is already running*
appears.

For any `asyncio` functionality to run on Jupyter Notebook you cannot invoke a run_until_complete(), since the loop you will receive from `asyncio.get_event_loop()` will be active. 


So for correct working you must add the task to the current loop:

```python
import asyncio
loop = asyncio.get_event_loop()
loop.create_task(some_async_function())
```

See: https://blog.jupyter.org/ipython-7-0-async-repl-a35ce050f7f7 

```{note}
Use result()  Return the result of the Task. function of asyncio, see https://docs.python.org/3/library/asyncio-task.html#asyncio.run

```

## Using JupyterLab in combination with Python programs that use asyncio

Running or importing Python libraries that use `asyncio` or `zmq` sockets is unlikely to work.

But you can use Python programs that use `asyncio`.

Just do run your Python program which uses `asyncio` as script:
```
%%sx
./[your python program].py [argument(s)]
```


:::{tip} 
Capture the output in the notebook. In this way the Python program which has process running in parallel under `asyncio` do work. The Python program is simply executed by the shell. This prevents interference with core JupyterLab processes. 

:::