
# A Binder Environment for the OPeNDAP Jupyter notebooks

## Start the base environment

To use this environment _as is_: 
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/OPENDAP/jupyter-binder/HEAD)

## Using the environment with content
To use this environment with content (such as Jupyter notebooks and/or data), 
first make the notebooks, etc., available via a separate repository.

Then construct a URL from this base environment repository URL and the content 
repository URL, do as follows:

`https://mybinder.org/v2/gh/OPENDAP/jupyter-binder/main?urlpath=git-pull?repo=https://github.com/OPENDAP/NASA-tutorials`

where `OPENDAP/jupyter-binder/main` says to use the `main` branch of this _environment_
repository, and the `urlpath=git-pull?repo=` part of the URL says to run the conent at
the URL given as the value of the keyword `repo`. This URL, when opened, will use the 
_nbgitpuller_ program to automatically pull in content from the specified repository 
into the base Binder environment.

## Configuration
The following files allow Binder to configure the base environment:

* `environment.yml` specifies the required tools/packages that will be installed via conda-forge
* `apt.txt` specifies the required tools/packages that will be installed via APT
* `postBuild` runs the commands after the `apt.txt` and `environment.yml` files are used.
* `jupyter_notebook_config.py` provides configuration information to the jupyter server.

## References

[mybinder.org status](https://mybinder.readthedocs.io/en/latest/about/status.html) How's the Binder site doing?

[Datalad binder repository](https://github.com/datalad/datalad-binder) A good example of an 'environment repo.'

[Running a public Jupyter Server](https://jupyter-server.readthedocs.io/en/latest/operators/public-server.html) This 
could provide key information about the odd login issue.

[Security in the Jupyter notebook server](https://jupyter-notebook.readthedocs.io/en/stable/security.html) This might
also provide information about the login problem.

[nbgitpuller documentation](https://nbgitpuller.readthedocs.io/en/latest/index.html#) This is the main page for the
nggitpuller tool used to access and start the 'content' repo. It includes a tool to make the link that triggers the
operation. 

[nbgitpuller](https://github.com/jupyterhub/nbgitpuller/tree/main) The nbgitpuller GitHub repo.

----
Copyright (C) 2023 OPeNDAP, Inc. This Jupyter Notebook is made available under the Creative Commons Attribution license 4.0.
