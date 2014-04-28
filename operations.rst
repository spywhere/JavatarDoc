.. include:: definitions.inc

.. _operations:

Operations
==========

Operations help you do class or package, obviously, operations such as organize imports or rename class easier.
Currently, |J| has 2 operations...

Correct Class
-------------

|J| will search for current package and your class name based on file name and location of current file and correct it on first class definition.

Organize Imports
----------------

|J| will automatically imports all necessary packages and remove unused packages for you. This is done within 7 sub-steps.

 1. |J| gathering imports informations from current file
 2. |J| let's you select a package that has the same class
 3. |J| imports "default imports" and Java's packages
 4. |J| asks you to enter package name for missing classes
 5. |J| asks for package name that you want to enter manually
 6. |J| clear all imports in current file
 7. |J| imports all packages that has been processed within step 1-4