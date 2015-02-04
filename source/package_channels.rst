.. include:: definitions.inc

.. _package_channels:

Package Channels
================

Stable Channel
--------------

Stable channel is a default channel for every user who installed |J|. This channel will release only fully working features and hide all incomplete features.

Development Channel
-------------------

Development channel is a optional channel for user who want to try upcoming features which may not fully working or need improvements.
All upcoming features will appear in *Development Section* only.

.. note:: Stable channel update notes also apply on development channel as well.

Package Updates Notifications
-----------------------------

In order to notice important notes to all users, in stable channel or development channel or both, |J| use custom notification system which will notice you **only once** when |J| is ready to use.
You can opt out this notification by settings ``message_id`` to ``-1`` in |J|'s user settings file, note that you can see update notes in README file or you will miss further important update notes.

.. note:: From |J| 1.0.0 and later, Package Channels has no effect on features except for *Development Section*. There will be no package channel on newer version of |J|.
