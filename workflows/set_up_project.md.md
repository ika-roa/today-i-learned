# Workflow for setting up new projects 

This workflow is for projects that
1.  Solve an immediate problem with no use outside of the current directory anticipated – in this case we don’t need to worry about setup.cfg, setup.py or even \_\_init__.py.
2.  Solve an immediate problem with the potential to spread code over several files and directories – we should now make sure we put an empty \_\_init__.py in each directory containing module files.

## Workflow:

1. Create new project folder from template
2.  Adapt project-specific files
    - README.md -> project description
    - environment.yml
    - JupyterLauncher.bat -> same environment name as in environment.yml
3. Open conda terminal, navigate to project folder (cd ...)
4. conda env create -f environment.yml
5. Activate new environment
6. To install local packages, navigate to package folder (cd ...)
    - pip install -e . for development mode --> package will be updated automatically
    - pip install . for normal mode --> package needs to be updated manually 
7.  check that newly created package is correctly installed (conda list)
8.  Open gitlab
9.  Create new project
10.  Open git bash
11.  git init --initial-branch=main
12.  git remote add origin  \<url\>
13.  git add .
14.  git commit -m "Initial commit"
15.  git push -u origin main

## Initial project template structure

```
├── .git                    <- git folder.
├── data                    <- input (create subfolders if necessary).
├── notebooks               <- Jupyter notebooks for analysis / primitive UI.
├── reports                 <- Analysis output.
│   └── figures             <- Generated plots and figures for reports.  
├── scripts                 <- Analysis and production scripts.
│   └── __init__.py         <-
├── tests                   <- Unit tests which can be run with `pytest`.
│   └── __init__.py         <-
├── .gitignore              <- Specifies files that should not be tracked by git.
├── environment.yml         <- The conda environment file for reproducibility.
├── JupyterLauncher.bat     <- Open notebooks in correct environment.
└── README.md               <- The top-level README for developers.
```

## Useful links

-   [https://ianhopkinson.org.uk/2022/02/understanding-setup-py-setup-cfg-and-pyproject-toml-in-python/](https://ianhopkinson.org.uk/2022/02/understanding-setup-py-setup-cfg-and-pyproject-toml-in-python/)