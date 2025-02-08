# Installation

The good news is you want to use or try JuypterLab: 
```{note}
No installation is needed! You can use many hosted instances.
```

:::{warning} 
If you care about privacy and data leakage you should never ever use a hosted JupyterLab version.
Large and small commercial JupyerLab hosting providers collect all kinds of telemetric data and other information of you that you do not want. 
:::


You can test Jupyterlab and build even directly your own notebooks using JupyerLite: [https://jupyterlite.github.io/demo](https://jupyterlite.github.io/demo)

Or see other options to try it out directly on the [project Jupyter - Try ](https://jupyter.org/try) page.

Of course, if you do not care about privacy and your freedom Google and numerous other companies offer also [full online notebook environments](https://colab.research.google.com/). Also [Microsoft Visual Studio  VSCode](https://code.visualstudio.com/docs/datascience/jupyter-notebooks) offers a great builtin environment for notebooks!

You can use JupyterLab as hosted environment using a hosted [JupyterHub](https://jupyter.org/hub) environment.

This works well for training classes, companies, research groups that need to work on an environment with lots of CPUs, memory and storage. And where maintenance tasks are managed by an skilled system administrator. 

But since most of the time you work with data that needs to stay secure the only option is installing JupyterLab on your own server or desktop.

Steps for installation of JupyterLab:

1- Create a new environment. Use conda, this is simple and battle field tested. Make a new environment with the latest 3.x stable Python version.

Assuming you have python installed: Use python the base version, minus the last fix number, so 3.8 instead of 3.8.3. Example:

```
conda create --name lab3 python=3.8 
```

2- Activate the new environment.
On unix:

```
source activate lab3
```

3- Installation:

To get jupyter lab on the latest python version: Use pip (not conda-forge!)
So do:
```
pip install -U jupyterlab
```

The conda version is not the latest version. **But** If you prefer the conda version do:
```
conda install -c conda-forge jupyterlab
```

## Starting the Jupyter Lab environment

To start a jupyter lab server now you can do:
```
jupyter lab 
```

More detailed information for installing JupyterLab can be found [here](https://jupyterlab.readthedocs.io/en/stable/getting_started/installation.html)

