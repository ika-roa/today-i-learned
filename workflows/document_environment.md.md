# Document the project environment

1.  Open anaconda prompt
2.  `conda activate environment`
3.  `conda install / pip install package`
4.  Record all dependencies and their versions
    - `conda env export -f environment.lock.yml`
    - This creates a file environment.lock.yml that recursively states all dependencies and their version as well as the Python version that was used to allow anyone to deterministically reproduce this environment in the future.
5. Besides a concrete environment file (lock.yaml) that exhaustively lists all dependencies, it’s also common practice to define an environment.yml where you state your abstract dependencies. 
    - `conda env export --from-history -f environment.yml`
    - These abstract dependencies comprise only libraries which are directly imported with no specific version
6. Regularly update and commit changes to these files in Git