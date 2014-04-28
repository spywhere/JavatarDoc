.. include:: definitions.inc

.. _adv_creates:

Advanced Creations
==================

In all create related commands, all packages and classes will be created relative to current package unless specified by **~** (tilde) before package or class path.
See examples below...

+-------------+--------------------------------------------------------------------+------------------------------------------------------------------+
| Input       | As Package                                                         | As Class                                                         |
+=============+====================================================================+==================================================================+
| Alpha       | ``Package "Alpha" is created in current package``                  | ``Class "Alpha" is created in current pacakge``                  |
+-------------+--------------------------------------------------------------------+------------------------------------------------------------------+
| ~Beta       | ``Package "Beta" is created in default package``                   | ``Class "Beta" is created in default pacakge``                   |
+-------------+--------------------------------------------------------------------+------------------------------------------------------------------+
| Alpha.Beta  | ``Package "Beta" is created in "(current package).Alpha" package`` | ``Class "Beta" is created in "(current package).Alpha" package`` |
+-------------+--------------------------------------------------------------------+------------------------------------------------------------------+
| ~Alpha.Beta | ``Package "Beta" is created in "Alpha"``                           | ``Class "Beta" is created in "Alpha"``                           |
+-------------+--------------------------------------------------------------------+------------------------------------------------------------------+