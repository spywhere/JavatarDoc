.. include:: definitions.inc

.. _default_packages:

Default Package Detection
=========================

|J| will specify the default package with these steps...

 1. Source Folder specified in the current project file (when open project)
 2. Project folder in current project file (when open project or folder)
 3. Folder contains the current file (when open file)
 4. Specify current package as ``(Unknown Package)``

|J| will refuse to create packages or classes within an unknown package. In this case, mostly because current file is not on the disk yet.
