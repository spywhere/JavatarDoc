.. include:: definitions.inc

.. _actions_history:

Actions History
===============

Actions History tracks how you use |J| and helps solve the problem. By provides useful informations as request by developer (only when you submit an issue).
A |J| Action History Report will looks similar to this when using it properly...

.. code-block:: none

	## Javatar Report
	### System Informations
	* Javatar Version: `1.0.0`
	* Sublime Version: `3059`
	* Package Path: `/Users/USER_NAME/Library/Application Support/Sublime Text 3/Packages`
	* Javatar Channel: `stable`
	* Sublime Channel: `stable`
	* Is Debug Mode: `False`
	* Platform: `osx`
	* As Packages: `True`
	* Package Control: `True`
	* Architecture: `x64`
	* Javatar's Parent Folder: `Javatar`
	* Is Project: `True`
	* Is File: `True`
	* Is Java: `True`

	### Action List
	1. Startup
	2. Reset all settings
	3. Reset all snippets
	4. Reset all default packages
	5. Read settings
	6. Load snippets
	7. Check news
	8. Ready
	9. Javatar snippet AbstractClass.javatar loaded
	10. Analyse snippet [file=Packages/Javatar/snippets/AbstractClass.javatar]
	11. Javatar snippet Class.javatar loaded
	12. Analyse snippet [file=Packages/Javatar/snippets/Class.javatar]
	13. Javatar snippet Enumerator.javatar loaded
	14. Analyse snippet [file=Packages/Javatar/snippets/Enumerator.javatar]
	15. Javatar snippet Interface.javatar loaded
	16. Analyse snippet [file=Packages/Javatar/snippets/Interface.javatar]
	17. Load Java default packages
	18. Javatar default package Proto.javatar-packages loaded
	19. Analyse package [file=Packages/Javatar/Java/Proto.javatar-packages]
	20. Javatar default package JavaSE8.javatar-packages loaded
	21. Analyse package [file=Packages/User/JavaSE8.javatar-packages]
	22. Check packages update


|J| **do not** automatically send these informations. You have to reply an issue with these informations yourself.

Actions History can be disabled by settings ``enable_actions_history`` to ``false``.
