# Remove conda package

Use the terminal or an Anaconda Prompt for the following steps.

#### To remove a package such as SciPy in an environment such as myenv
`conda remove -n myenv scipy`

#### To remove a package such as SciPy in the current environment
`conda remove scipy`

#### To remove multiple packages at once, such as SciPy and cURL 
`conda remove scipy curl`

#### To confirm that a package has been removed 
`conda list`