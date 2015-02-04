.. include:: definitions.inc

.. _javatar_grammar:

|J| Grammar
===========

|J| grammar (\*.javatar-grammar) is used to assigned a name to Java elements such as keywords, strings or similar just like `TextMate's grammar`_.
This allow |J| to get informations about document more accurate.

.. _TextMate's grammar: http://manual.macromates.com/en/language_grammars

|J| have it own parser that will parse your document using this grammar. Since |J| is using `GrammarParser`_, its grammars are also a `GrammarParser`_'s grammar.

More informations about how grammar works is on `GrammarParser`_ readme.

.. _GrammarParser: https://github.com/spywhere/GrammarParser
