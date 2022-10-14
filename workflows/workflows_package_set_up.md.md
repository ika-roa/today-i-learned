# Workflow for setting up new packages

This workflow is for projects that
1.  Provide a local library to reuse in other projects locally. This will require us to run “python setup.py develop” or better “pip install -e .”
2.  Provide a library which will be used on other systems you control. Again using “pip install -e .”
3.  Provide a library which will be published publicly, here we will need to additionally make use of something like the packaging library.

## Workflow:

1. Create new project folder from template
2.  Adapt project-specific files
    1. setup.cfg -> package name / short description
    2. README.md -> package description
    3. environment.yml
3. Open gitlab / github
4. Create new project
5. Open git bash
6. git init --initial-branch=main
7. git remote add origin  \<url\>
8. git add .
9. git commit -m "Initial commit"
10. git push -u origin main

## Useful links

- https://ianhopkinson.org.uk/2022/02/understanding-setup-py-setup-cfg-and-pyproject-toml-in-python/
