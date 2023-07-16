# A Binder Environment for the OPeNDAP Jupyter notebooks

1. Start the base environment

To use this environment _as is_: 
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/OPENDAP/jupyter-binder/HEAD)

2. Environment with content
To use this environment with content (such as Jupyter notebooks and/or data), 
first make this content available via a separate repository.

Then construct a URL from the base environment repository URL and the content repository URL, as follows:

`https://mybinder.org/v2/gh/datalad/datalad-binder/parameter-test?urlpath=git-pull?repo=<url-of-your-content-repo>`

This URL, when opened, will use nbgitpuller to automatically pull in content from the specified repository 
into the base Binder environment.


3. Configuration
The following files allow Binder to configure the base environment:

* `environment.yml` specifies the required tools/packages that will be installed via conda-forge
* `apt.txt` specifies the required tools/packages that will be installed via APT
* `postBuild` runs the commands after the `apt.txt` and `environment.yml` files are used.
* `jupyter_notebook_config.py` provides configuration information to the jupyter server.

4. References

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
