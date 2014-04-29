.. include:: definitions.inc

.. _javatar_packages:

|J| Packages
============

|J| required packages file (\*.javatar-packages) to correctly import necessary Java's packages. These files contain all classes, fields, methods and packages to use with |J|.

|J| Packages file is a JSON file. You can read more details about each key and value in Proto.javatar-packages located within |J|'s Java folder (can be accessed via *Preferences > Package Settings > Proto.javatar-packages* or via command palette by type ``Javatar Proto``).

However, their are 2 special keys that are not normally used within |J| Packages which are...

* ``experiment``
	* Set this to ``true`` to exclude this package from |J|'s packages list.
* ``always_import``
	* Set this to ``true`` to always import this package even no class is used (this will import as ``package.*``).

Both keys are boolean type and also optional to use.