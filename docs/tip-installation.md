# Installation

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

```
conda install -c conda-forge jupyterlab
```

More detailed information for installing JupyterLab can be found [here](https://jupyterlab.readthedocs.io/en/stable/getting_started/installation.html)

