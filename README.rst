Oculy: Modular data viewer
==========================

Installation
------------

First, all you need is to clone the repository of oculy on your local machine::

    git clone https://github.com/MatthieuDartiailh/oculy.git

Now that you cloned oculy, you are to to build your package. You may need to install the build
package first::

    pip install build

OThis should create a `build/` folder as well as a `dist/` folder
(don't forget to add these to your `.gitignore`, if they aren't in there already.

you can now build your package by running::

 python -m build --wheel

from the folder where the `pyproject.toml` resides. In `dist/` folder you will find a wheel
named `oculy-0.0.0-py2.py3-none-any.whl`. That file contains your package, and this is all
you need to distribute it. You can install this package anywhere by copying it to the relevant
machine and running::

    pip install oculy-0.0.0-py2.py3-none-any.whl

When developing you probably do not want to re-build and re-install the wheel every time you
have made a change to the code, and for that you can use an editable install. This will install
your package without packaging it into a file, but by referring to the source directory. You can
do so by running::


    pip install -e .

from the directory where the `pyproject.toml` resides. Any changes you make to the source code
will take immediate effect.
Now you can run oculy by typing either::

    oculy

or::

    python -m oculy

The second option allow you to see the program console output and can be useful to debug issues.
