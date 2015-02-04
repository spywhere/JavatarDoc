.. include:: definitions.inc

.. _adv_creates:

Advanced Creations
==================

Relative Creations
------------------

In all create related commands, all packages and classes will be created relative to the current package unless specified by **~** (tilde) before package or class path.
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

Classes with main method
------------------------

To create a class with main method, just add ``AsMain`` at the end of your class name.
|J| will automatically add main method when the class is created.

Customized Classes
------------------

You can create a class with custom visibility (default class visibility is ``public``) by adding one of the keyword ``public``, ``private``, ``protected`` and ``default`` before your **class name**. If you want to create an abstract or final class just add ``abstract`` or ``final`` **after the visibility**.

Examples:
 * ``privateBattleShip``
    * Class "BattleShip" is created with "private" visiblity
 * ``protectedAbstractBattleShip``
    * Class "BattleShip" is created with "protected" visibility and "abstract" modifier
 * ``wargame.entity.defaultBattleShip``
    * Class "BattleShip" is created with "default" visibility in "wargame.entity" package

.. note:: The keyword **is** order-sensitive but not case-sensitive.

Inheritances Helper
-------------------

You can create a class included with inheritances of classes and interfaces by using special characters.

To extends a class, add ``:`` (colon) followed by a class name (or a list of class names separated by commas if it is a enumerator).

To implements an interface, add ``<`` (left angle bracket) followed by a list of interface names separated by commas.

If you are on Development Channel, Javatar will also automatically organize imports when class is created.

Examples:
 * ``BattleShip:BattleUnit``
    * Class "BattleShip" is inherited from "BattleUnit" class (has "extends" in the code)
 * ``BattleShip:BattleUnit<WaterUnit``
    * Class "BattleShip" is both inherited from "BattleUnit" class and "WaterUnit" interface
 * ``BattleShip<Carrier,WaterUnit:BattleUnit``
    * Class "BattleUnit" is inherited from "BattleUnit" class, "Carrier" interface and "WaterUnit" interface
 * ``wargame.entity.defaultAbstractBattleShip:BattleUnit<Carrier,WaterUnit``
    * Abstract class "BattleUnit" is created in "wargame.entity" package with "default" visibility and is inherited from "BattleUnit", "Carrier" and "WaterUnit" class/interface

Inheritances **is** case-sensitive but not order-sensitive.

.. note:: Despite, Javatar allows you to create "private" or "protected" classes. It does not make sense to create a private or protected class since another class can not see a new class you created.
