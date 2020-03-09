Quickstart
===========


Basic Concepts
//////////////

- Once ``ckan-wit`` is installed, simple object and array parameters can be used to manipulate the results.
- When no parameters are passed to ``wit-resources``, all packages ``aggregated responses`` supported by the library will be returned.

 For direct usage in a python interpreter::

 >>> import ckan_wit.src.wit_main as wit
 >>> wit.ckan_wit_main()  #  returns all aggregated and filtered infos
 >>> wit.ckan_wit_main().Europe  #  returns all meta infos from all europe specific portals.


Getting Started
----------------
**A Simple Flask WebApplication Using CKAN-WIT**

    [placeHolder]::

    >>> #Content will be added soon.


HowTo's
--------
    [placeHolder]::

    >>> import ckan_wit.src.wit_main as m
    >>> wit.ckan_wit_main()["wit_resources"]["AFRICA"]["total_metadata"]

