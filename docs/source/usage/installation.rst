Installation
=============
``ckan-wit`` is a metadata library for opendata portal. It is recommended as it’s a higher-level tool that simplifies metadata aggregation for common use cases across CKAN-compatible opendata portals.
This installation process applies to the proof-of-concept for which the library is being built and therefore sticks to some pythonic environment settings to show how it can be installed and used.

.. note::
    Hey buddy, please, before you go any further, make ensure you have Python >= 3.6 and that it's available from your command line. You can check this by simply running::

    $ python3 --version

Set up a Project Directory
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Simply create a directory where you want the project to reside::

 $ mkdir my_project

Setting up a ``virtual environment``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Set up your VENV where all the requirements.txt and environmental variables will reside.::

 $ pip install --user pipenv

.. note::
    Don't forget to activate the virtual environment

Installing the requirements/external dependencies with ``pip``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Once set, with your venv still activated, simply do::

 (my_virtualenv)$ pip install aiohttp[speedups]
 (my_virtualenv)$ pip install requests

Or, directly from the git-repo::

 (my_virtualenv)$ pip install -r https://github.com/Ethel-Ecc/ckan-wit-documentation/trunck/requirements.txt

Installing ``ckan-wit`` with ``pip``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
The library is installed from the python packaging index::

    (my_virtualenv)$ pip install -i https://test.pypi.org/simple/ ckan-wit

You can also install a specific version of the tool by simply doing::

    (my_virtualenv)$ pip install -i https://test.pypi.org/simple/ ckan-wit==0.1.0      # where 0.1.0 is the version number.

This installs the latest version of ckan-wit into the virtual environment you have setup.

FirstSteps
~~~~~~~~~~~~
After a successful install, simply import the package into your web application ::

 >>> import ckan_wit.src.wit_main as wit

Start using it as::

 >>> def index_page():
       resp = wit.ckan_wit_main() # returns all aggregated and filtered resources, currently supported by the library.
       return  resp

 >>> index_page()

OR, use simple dictionary object and slice operations to return geographic-specific resources. To return resources that are found from open data portals in Africa, simply do::

 >>> def index_page():
        resp = wit.ckan_wit_main()
        resp = resp['Africa'] # returns resources that are found from open data portals from Africa.

     >>> index_page()

To return resources that are found from open data portals in Europe, do::

 >>> def index_page():
        resp = wit.ckan_wit_main()
        resp = resp['Europe'] # returns resources that are found from open data portals from Africa.

     >>> index_page()


To return resources that are found from open data portals in America, do::

 >>> def index_page():
       resp = wit.ckan_wit_main()
       resp = resp['Americas'] # returns resources that are found from open data portals from America.

 >>> index_page()

To return resources that are found from open data portals in Asia, do::

 >>> def index_page():
       resp = wit.ckan_wit_main()
       resp = resp['Asia'] # returns resources that are found from open data portals from Asia.

 >>> index_page()

See more from the getting started page ...
