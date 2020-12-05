Python Virtual Environment
====

In this note, we document creating virtual environments to isolate project or repository dependencies. To do so, we can use the following command,

```
$ virtualenv <environment name> --python=python3.7  # specifies python version to use
```

Then, to activate the virtual environment

```
$ source <environment name>/bin/activate
```

The code above should have an output similar to this,

```
$ pip list
Package    Version 
---------- ------- 
pip        20.1.1 
setuptools 49.2.0 
wheel      0.34.2 
```

The `pip list` command is used to show the libraries/packages installed. When a virtual environment is activate, it lists the libraries/packages in that virtual environment.