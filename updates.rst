.. include:: definitions.inc

.. _updates:

Important Updates and Changelogs
================================

From 11 Apr 2014, |J| will **not** include any packages inside its package. This helps install and update |J| faster but still maintaining default features.
|J| will automatically download and install necessary packages (Java SE) at startup since users install |J| usually already connected to the internet.

Development Build
-----------------

* No updates specifically for development channel

Stable Build
------------

* New feature, Run main class. Can be accessed via *Development Section... > Builds: Run Main Class* (more details on :ref:`javatar_shell`)
* Java's compilation errors and stack traces highlighting in console
* Multi-thread :ref:`build_system`
* Build now put all .class files in "bin" directory and support dependencies (more informations about dependencies in :ref:`projects`)
* Project/Package/Class Build improvements (now support multiple files building and error logs)
* New build type, Working Classes
* Fix internal shell did not work on Windows
* :ref:`package_channels` must be specified 'dev' in order to subscribe to development channel instead of anything else except 'stable'
* Building system now completely changed to internal building system (more details on :ref:`build_system`)
* Macro improvements
* Some code tweaks