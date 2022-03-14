## OpenEMP Documentation
[![CodeFactor](https://www.codefactor.io/repository/github/openemp/openemp-documentation/badge)](https://www.codefactor.io/repository/github/openemp/openemp-documentation)

This is the documentation for OpenEMP, accessible from here: https://docs.openemp.org

### Requirements:

- Python >= 2.7
- pip
- git
- [mkdocs](https://www.mkdocs.org/#installation)

### Getting Started

Setup your machine to run the documentation locally by executing the following:

First please make sure that [python](https://www.python.org/) is installed as well as the package manager [pip]()

make sure that all is set up

```shell script
$ python --version
Python 3.7.6
$ pip --version
pip 20.0.2 from /usr/local/lib/python3.7/site-packages/pip (python 3.7)
```

and then install the requirements:

```shell script
git clone https://github.com/openemp/openemp-documentation
cd openemp-documentation
pip install -r docs/requirements.txt
```

### Run documentation
 
to run the documentation execute the following from the project root folder
```shell script
mkdocs serve
```
you can now browse the documentation from `localhost:8000`

Note: You can edit the documentation and see it exposed instantly after saving your changes.

Please read more about how to enhance the OpenEMP mkdocs documentation from [here](https://www.mkdocs.org/user-guide/writing-your-docs/) 


### Let's Get in touch

please feel free to reach out to us in [Community](https://community.openemp.org) or via [email](mailto:contact@openemp.org)
