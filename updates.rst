.. include:: definitions.inc

.. _updates:

Important Updates and Changelogs
================================

From 11 Apr 2014, |J| will **not** include any packages in its package. This helps install and update |J| faster, but still maintaining default features.
|J| will automatically download and install necessary packages (Java SE) at startup since users install |J| usually already connected to the internet.

Development Build
-----------------

* Javatar now has its own Java parser, you can play with it via *Development Section... > Parse Document* (more information about grammar on :ref:`javatar_grammar`)

Stable Build
------------

* Javatar now nest project settings inside "Javatar" key
* Javatar will automatically detect installed JDK and will automatically select the best one (more details on :ref:`jdk_detection`)
* New menu section, Javatar Settings
* New feature, Run main class. Can be accessed via *Development Section... > Builds: Run Main Class* (more details on :ref:`javatar_shell`)
* Build now put all .class files in "bin" directory and support dependencies (more information about dependencies in :ref:`projects`)
* Project/Package/Class Build improvements (now support multiple files building and error logs)
* Fix path not working properly
