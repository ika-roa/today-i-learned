# Types of projects

1.  **Coding to solve an immediate problem** with no use outside of the current directory anticipated – in this case we don’t need to worry about setup.cfg, setup.py or even \_\_init\_\_.py.
2.  **Coding to solve a bigger problem** with the potential to spread code over several files and directories – we should now make sure we put an empty \_\_init\_\_.py in each directory containing module files.
3.  **Coding to provide a local library** to reuse in other projects locally this will require us to run “python setup.py develop” or better “pip install -e .”
4.  **Coding to provide a library which will be used on other systems** you control. Again use “pip install -e .”
5.  **Coding to provide a library which will be published publicly**, here we will need to additionally make use of something like the packaging library.

From <[https://ianhopkinson.org.uk/2022/02/understanding-setup-py-setup-cfg-and-pyproject-toml-in-python/](https://ianhopkinson.org.uk/2022/02/understanding-setup-py-setup-cfg-and-pyproject-toml-in-python/)>