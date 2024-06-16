# Putting notebooks under version control

Simple is to use git.

The notebook format is plain json. This works well using git.

```{attention} 
**BUT** There are some things that are not perfect yet. So mind cleaning your output cells first or saving results.
Notebooks makes using of caching (It's html) so focus for version control on the real content in input cells.
Generated output cells stored in version control do not work well with git.

Git doesn’t show the output of versions between notebooks always correct. E.g. a git merge for nested JSON documents is error prone, and a git diff on notebooks with output cells is the best way to find differences.

```


Some simple solutions exist:

* `jupyterlab-git` A JupyterLab extension for version control using Git. See: https://github.com/jupyterlab/jupyterlab-git This is the only tool that you should be using in future. But older tools for classical notebooks still exist. E.g.:
* `nbdime` provides tools for diffing and merging of notebooks. See: https://nbdime.readthedocs.io/en/latest/index.html# 

Executed cells are not needed for version control.
You can clear all output cells manually before storing your notebook under version control.
But if you have multiple notebooks there is a simple tool that does this job well:
* nbstripout: strip output from Jupyter and IPython notebooks.
This tool Opens a notebook, strips its output, and writes the outputless version to the original file. Check: https://github.com/kynan/nbstripout for code and installation instruction of this tool.



