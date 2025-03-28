# Show installed packages in Linux
## Find out which packages are installed (if exact name is unknown)
### Show all installed packages
`apt --installed list`
### Show manually installed packages
`apt --installed list | grep -v automatic`
## Information about installed package (if name is known)
### Show version of installed package
`dpkg -s <package>`
### Show installed and available version of package
`apt-cache policy <package>`
### Show available version of package
`apt show <package>`