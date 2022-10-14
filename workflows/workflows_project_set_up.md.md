# Workflow for setting up new projects 

This workflow is for projects that
1.  Solve an immediate problem with no use outside of the current directory anticipated – in this case we don’t need to worry about setup.cfg, setup.py or even \_\_init__.py.
2.  Solve an immediate problem with the potential to spread code over several files and directories – we should now make sure we put an empty \_\_init__.py in each directory containing module files.

## Workflow:

1. Create new project folder from template
2.  Adapt project-specific files
    1. README.md -> project description
    3. environment.yml
    4. JupyterLauncher.bat -> same environment name as in environment.yml
4. Open conda terminal, navigate to project folder (cd ...)
5. conda activate setup_env
6. conda env create -f environment.yml
7. Activate new environment
8. To install local packages, navigate to package folder (cd ...)
    - pip install -e . for development mode --> package will be updated automatically
    - pip install . for normal mode --> package needs to be updated manually 
10.  check that newly created package is correctly installed (conda list)
11.  Open gitlab
12.  Create new project
13.  Open git bash
14.  git init --initial-branch=main
15.  git remote add origin  \<url\>
16.  git add .
17.  git commit -m "Initial commit"
18.  git push -u origin main


## Useful links

-   [https://ianhopkinson.org.uk/2022/02/understanding-setup-py-setup-cfg-and-pyproject-toml-in-python/](https://ianhopkinson.org.uk/2022/02/understanding-setup-py-setup-cfg-and-pyproject-toml-in-python/)