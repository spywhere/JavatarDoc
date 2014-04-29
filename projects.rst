.. include:: definitions.inc

.. _projects:

Projects Settings
=================

Project Settings section contains per-project settings.

.. tip:: All |J|'s settings can be set specifically for each project by setting it in project file instead of user preferences

Dependencies
------------

|J| support build and run project that have dependencies .jar files both global and specific projects.
To add a dependency to global projects (all projects), you need to add them manually by specified it in |J|'s user preferences since most projects have different dependencies.
To add a dependency to current project, go to *Project Settings... > Dependencies...* and select *Add External .jar* or *Add Class Folder* and |J| will show a dialog to select a dependency you want to add.

Set Source Folder
-----------------

As default, |J| will specified a default package (mostly) based-on current working folder or folder contains current working file (more details on next section).
Many projects might use multiple folders and some of them are not source folder.
Set source folder helps solve this issue by let you select which folder to specified as Source Folder (or default package as |J| use).