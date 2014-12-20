.. include:: definitions.inc

.. _javatar_snippets:

|J| Snippets
============

|J| snippets is a dynamic snippet which will change part of the file to correspond with package path and class name. By using parameters, you can specify which part of the file you want to fill the data to.

You can make your own snippets to use within |J| by create a new file ends with ``.javatar``

Snippet class tags (for more informations about snippet tags, see below) will be used as a type of classes which show in input panel when create a new file (``%type% Name:``), on error dialog (``%type% %name% already exists``) and in status bar when file was created (``%type% %name% is created within package %package%``).

Example of |J|'s snippets is inside |J|'s snippets folder (``PACKAGES_PATH/Javatar/snippets`` or inside .sublime-packages file)

Snippet Tags
------------

The following tags are used inside |J| snippet files (\*.javatar) which will be used by |J| to display proper command to the user

* %class:\*TYPE OF CLASS\*%
* %description:\*DESCRIPTION TO SHOW UNDER CREATION COMMAND\*%

Usage of snippet tags in action
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. image:: images/CreateNewSS.png

Snippet Parameters
------------------

The following parameters are used inside |J| snippet files (\*.javatar) which will be parsed by |J| and |st|.

* %package_path% = Package path
* %class% = Class name
* %file% = File path
* %file_name% = File name (equivalent to ``%class%.java``)
* %package% = Package code (for example ``package java.utils;`` or same as ``package %packages_path%;``)
* All |st|'s snippet parameters can be used within |J| snippets. For example: ${1} or ${2://Comment}
