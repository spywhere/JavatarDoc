.. include:: definitions.inc

.. _build_system:

Build System
============

|J|'s build system using its internal shell to build your classes.
|J| builds parameters are based on default |st|'s JavaC build settings.
You can change the build command via a |J| settings file.

|J|'s build system support multi-threads building. By running multiple instance of build system to help build your class faster.
You can set how many threads you want to run in |J|'s user preferences.

While building, |J| will show building progress in |st|'s status bar.
If it found any error, |J| will show you a new view contains all errors and will keep on printing until building is complete.
To cancel building in progress, just close an error logs view and |J| will stop building your classes immediately.

.. note:: Building cannot be stopped if there is no error occurred.
