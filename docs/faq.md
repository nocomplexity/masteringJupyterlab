# FAQs

I hate FAQs sections. But too often information provided in FAQ sections can save you a lot of time.
So anyone who has a good suggestion for organizing information in this section: Feel free to make this open publication better! (See the help section for contributing.) 

## Running shell commands in python code

Running shell commands in Python scripts is complicated. It can get more complicated if you run shell commands from a Python cell in your notebook. This is due to the fact that the notebook uses the module `os.subprocess` extensively internally. 

```{tip} 
So avoid running shell scripts and/or python scripts that invoke a shell. 
Sooner or later you hit misery. In future this will be solved...hopefully.

```

```{note}
But mind: Most **good written** python programs that use shell scripts do run without problems in a notebook. It only get problematic when multiple pipes are created from the [pipes library](https://docs.python.org/3/library/pipes.html)
```

There are good ways to run *simple* shell commands in python code in your notebook:
1. Use a construct like:

```python
import subprocess
import sys

def install(package_name):
    subprocess.check_call([sys.executable, '<flag>', '<cli-command>', '<option>', <input>])

#E.g. to run pip as shell CLI command in using some python code:
    subprocess.check_call([sys.executable, '-m', 'pip', 'install', package_name])
```


2. Use the `Ipython` magic command for running shell scripts. E.g. to run  a shell script in a cell , just do:

```
!<command or shell script>
```


## Can you use FreeBSD

[FreeBSD](https://www.freebsd.org/) is a great innovative free and open (FOSS) unix operating system. It is a platform that is great for internet hosting and performing number crunching compute tasks.

So it makes sense to install Jupyter Server on FreeBSD. In this way you can use JupyterLab hosted from your own BSD box.

But:
```{caution}
Installation of the Jupyter ecosystem (Python packages and required dependencies) is not a walk in the park on FreeBSD. Also many heavily used machine learning Python packages are not (yet) ported to FreeBSD. 
```

So if you like simple: Rethink if your use case really requires using FreeBSD for server JupyterLab and related Jupyter tools. It can be done, but it requires extra effort. And when you do it, publish your installation steps, so others can reuse it and make it better!


