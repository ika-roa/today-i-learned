# Setup files for packages

## Setup.py and setup.cfg
The setup.py and setup.cfg files are artefacts of the setuptools module which is designed to help with the packaging process. It is used by pip whose purpose is to install a package either locally or remotely. If we do not configure setup.py / setup.cfg correctly then pip will not work. In the past we would have written a setup.py file which contained a bunch of configuration information but now we should put that configuration information into setup.cfg which is effectively an ini file (i.e. does not need to be executed to be read). This is why we now have the minimal setup.py file.

## pyproject.toml
The pyproject.toml file was introduced as a way of separating configuration of the build system from a specific, optional library (setuptools) and also enabling setuptools to install  itself without already being installed.

From <[https://ianhopkinson.org.uk/2022/02/understanding-setup-py-setup-cfg-and-pyproject-toml-in-python/](https://ianhopkinson.org.uk/2022/02/understanding-setup-py-setup-cfg-and-pyproject-toml-in-python/)>