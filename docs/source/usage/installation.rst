Installation
=============
CKAN-WIT is a metadata library for opendata portal. It is recommended as it’s a higher-level tool that simplifies metadata aggregation for common use cases across
CKAN-compatible opendata portals.
This installation process applies to the proof-of-concept for which the library is being built and therefore sticks to some pythonic environment settings to show how it can be
installed and used.

.. note::
    Hey buddy, please, before you go any further, make ensure you have Python >= 3.6 and that it's available from your command line. You can check this by simply running::

    $ python3 --version

Set up a Project Directory
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Simply create a directory where you want the project to reside::

   $ mkdir my_project

Setting up a Virtual Environment
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Set up your VENV where all the requirements.txt and environmental variables will reside.::

    $ pip install --user pipenv

.. note::
    Don't forget to activate the virtual environment

Installing the requirements.txt file from git
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

 Once set, with your venv still activated, simply do::

    $ pip install -r https://github.com/Ethel-Ecc/ckan-wit-documentation/trunck/requirements.txt

Installing the CKAN-WIT
~~~~~~~~~~~~~~~~~~~~~~~~~
The tools is installed from the python packaging index::

    $ pip install -i https://test.pypi.org/simple/ ckan-wit
ma
This installs the latest version of ckan-wit into the virtual environment you have setup.
After a successful install, simply import the package into your web application ::

 >>> import ckan_wit.src.wit_main as pkg

Start using it as::

 >>> def index_page():
    resp = pkg.ckan_wit_main()
    return  resp

 >>> index_page()

See more from the getting started page ...
