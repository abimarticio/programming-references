Python Virtual Environment
====

In this note, we document creating virtual environments to isolate project or repository dependencies. To do so, we can use the following command,

```shell script
$ virtualenv <environment name> --python=python3.7  # specifies python version to use
```

Then, to activate the virtual environment

```shell script
$ source <environment name>/bin/activate
```

The code above should have an output similar to this,

```shell script
$ pip list
Package    Version 
---------- ------- 
pip        20.1.1 
setuptools 49.2.0 
wheel      0.34.2 
```

The `pip list` command is used to show the libraries/packages installed. When a virtual environment is activate, it lists the libraries/packages in that virtual environment.

To list the dependencies of a project or a repository, we use the `pipreqs` command like so,

```shell script
$ virtualenv project-1-env --python=python3
$ source project-1-env/bin/activate
$ (project-1-env) cd <repository name>
$ pipreqs ./ --encoding=utf-8
INFO: Successfully saved requirements file in ./requirements.txt
```

The `requirements.txt` file now contains the dependencies of the project or repository.