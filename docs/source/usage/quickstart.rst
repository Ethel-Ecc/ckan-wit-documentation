Quickstart
===========


Basic Concepts
//////////////

- A virtualenv will automatically be created, when one doesn't exist.
- When no parameters are passed to ``install``, all packages ``[packages]`` specified will be installed.
- To initialize a Python 3 virtual environment, run ``$ pipenv --three``.
- To initialize a Python 2 virtual environment, run ``$ pipenv --two``.
- Otherwise, whatever virtualenv defaults to will be the default.

Other Commands
//////////////

- ``graph`` will show you a dependency graph of your installed dependencies.
- ``shell`` will spawn a shell with the virtualenv activated. This shell can be deactivated by using ``exit``.
- ``run`` will run a given command from the virtualenv, with any arguments forwarded (e.g. ``$ pipenv run python`` or ``$ pipenv run pip freeze``).
- ``check`` checks for security vulnerabilities and asserts that PEP 508 requirements are being met by the current environment.


Getting Started
----------------
Here is some text for the information on how to use the CKAN-WIT tool.

         >>> print('hello')
         >>> hello


HowTo's
-------
The on how to do some basic functions will come in here.