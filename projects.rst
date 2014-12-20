.. include:: definitions.inc

.. _projects:

Projects Settings
=================

The Project Settings section contains per-project settings.

.. tip:: All |J|'s settings can be set specifically for each project by setting it in project file instead of user preferences

Set Program Arguments
---------------------

By default, |J| will not pass parameters when running an application through the *Run Main Class* command (see :ref:`getting_started` for an example).
*Set Program Arguments* allows you to specify what arguments should be passed on main execution.

Dependencies
------------

|J| supports build and run project that have dependencies .jar files both global and specific projects.
To add a dependency to global projects (all projects), go to *Javatar Settings... > Dependencies...* and select *Add External .jar* or *Add Class Folder* and |J| will show a dialog to select a dependency you want to add.
To add a dependency to current project, same as for global projects, but using *Project Settings... > Dependencies...* menu instead.

Set Source Folder
-----------------

As default, |J| will specify a default package (mostly) based-on current working folder or folder contains current working files (more details in next section).
Many projects might use multiple folders and some of them are not source folder.
Set source folder helps solve this issue by letting you select which folder to specified as Source Folder (or default package as |J| use).

Set Default JDK
---------------
As default, |J| will use global JDK (more details on :ref:`jdk_detection`).
Set a default JDK for each project can be helpful since you might want some projects to use newer JDK version.

To set a default JDK for your project, go to *Project Settings... > Set Default JDK* and |J| will show a list of JDK you have and available to use.
