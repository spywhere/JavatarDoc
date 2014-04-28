.. include:: definitions.inc

.. _build_system:

Build System
============

|J|'s build system use its internal shell to build your classes.
|J| build parameters are based on default |st|'s JavaC build settings.
You can change the build command via |J| settings file.

While building, |J| will show building progress in |st|'s status bar.
If it found any error while building, |J| will show you a new view contains all errors and will keep on printing until building is complete.
To cancel building in progress, just close a error logs view and |J| will stop building your classes immediately.

.. note:: |J| cannot be stopped if there is no error occurred