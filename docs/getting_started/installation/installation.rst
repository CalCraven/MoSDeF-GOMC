============
Installation
============
.. image:: https://img.shields.io/badge/license-MIT-blue.svg
    :target: http://opensource.org/licenses/MIT

Install with `mamba <https://github.com/mamba-org/mamba>`_ (Recommended)
------------------------------------------------------------------------
::

    $ conda create --name mosdef_gomc python=3.10

    $ conda activate mosdef_gomc

    $ conda install -c conda-forge mamba

    $ mamba install -c conda-forge mosdef-gomc python=3.10


Install with `conda <https://repo.anaconda.com/miniconda/>`_
------------------------------------------------------------
::

    $ conda install -c conda-forge mosdef-gomc


NOTE: conda has had some issues pulling the most recent packages, so a mamba installation is recommended.

Install an editable version from the source code
------------------------------------------------

It is good practice to use a pre-packaged Python distribution like
`Miniconda <https://docs.conda.io/en/latest/miniconda.html>`_,
which ensures all of the dependencies are installed::

    $ git clone https://github.com/GOMC-WSU/MoSDeF-GOMC
    $ cd mosdef_gomc
    $ conda env create -f environment.yml
    $ conda activate mosdef_gomc
    $ pip install -e .

.. note::
    The above installation instructions are for OSX and Unix.  If you are using Windows, please use a virtual machine or the Linux subsystem, as some components of this software and its dependencies may not be fully compatible with Windows.


Install pre-commit
------------------

The `pre-commit <https://pre-commit.com/>`_ packages are utilized to maintain uniform code formatting, which is auto-installed in the mosdef_gomc environment.

To check all the file, you can run::

     $ pre-commit run --all-files


Supported Python Versions
-------------------------

Python 3.9 and 3.10 are officially supported and tested during development and with the final product.
Python versions older than 3.9 may work, but there is no guarantee.

Testing your installation
-------------------------

MoSDeF-GOMC uses `pytest <https://docs.pytest.org/en/stable/>`_ to test the code for accuracy, possible errors, code changes, or if the existing implementation is correct.
The pytest package is auto-installed in the mosdef_gomc environment.

To run these unit tests, run the following from the base directory::

    $ pytest -v

Building the documentation
--------------------------

MoSDeF-GOMC documentation is all built using `sphinx <https://www.sphinx-doc.org/en/master/index.html>`_.
The sphinx package is auto-installed in the mosdef_gomc environment.

The ``docs`` can be built locally with the following commands when in the ``docs`` directory::

    $ make html
