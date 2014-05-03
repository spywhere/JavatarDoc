.. include:: definitions.inc

.. _javatar_grammar:

|J| Grammar
===========

|J| grammar (*.javatar-grammar) is used to assigned a name to Java elements such as keywords, strings or similar just like `TextMate's grammar`_.
This allow |J| to get informations about document more accurate.

.. _TextMate's grammar: http://manual.macromates.com/en/language_grammars

|J| Grammar will use to parse the document only once. Then scope selector can be use to get all informations needed.

Example Grammar
---------------

A |J| grammar format is a JSON file which contains key and value for parser to parse the document. Here is the example grammar...

.. code-block:: json

	{
		"compilation_unit": [
			{
				"include": "StringLiteral"
			}
		],
		"repository": {
			"StringLiteral": {
				"name": "StringLiteral",
				"parse": [
					{
						"match": "\""
					},
					{
						"name": "String"
						"match": "[^\"]*"
					},
					{
						"match": "\""
					}
				]
			}
		}
	}

At the root of grammar there are only 2 key/value pairs:

``compilation_unit``
~~~~~~~~~~~~~~~~~~~~

This is the root of grammar represent the whole document. Its value is a list of rules just like ``parse`` rule key (covered later).

``repository``
~~~~~~~~~~~~~~

An object (or dictionary) for holding more rules. You can references a rule in this section by using ``include`` rule key (covered later).

Rules
-----
rules are used to match a portion of the document. Here is all rule keys you can use...

``name``
~~~~~~~~

Name will be assigned to Java element which scope selector will search using this name.

``match``
~~~~~~~~~

A regular expression which use to match/parse a portion of the document.

``parse``
~~~~~~~~~

A list of rules which will continue only when all rules are return success, indicate that parsing is done properly.

Here is the example in general grammar format ([x] indicate a symbol).

.. code-block:: grammar

	[Variable]
		[DataType] [Identifier] ;

and here is the example converted into a Rule.

.. code-block:: json

	{
		"Variable": {
			"name": "Variable",
			"parse": [
				{
					"include": "DataType"
				},
				{
					"include": "Identifier"
				},
				{
					"match": ";"
				}
			]
		}
	}

``parse_any``
~~~~~~~~~~~~~

A list of rules which will continue when "one" of all rules is return success.

Here is the example in general grammar format.

.. code-block:: grammar

	[DataType]
		int
		float

and here is the example converted into a Rule.

.. code-block:: json

	{
		"DataType": {
			"name": "DataType",
			"parse_any": [
				{
					"match": "int"
				},
				{
					"match": "float"
				}
			]
		}
	}

``include``
~~~~~~~~~~~

This use to reference another rules to parse. Just like you paste a rule here.

Here is the example.

.. code-block:: json

	{
		"PrimitiveArrayInitializer": {
			"name": "PrimitiveArrayInitializer",
			"parse": [
				{
					"match": "new"
				},
				{
					"include": "DataType"
				},
				{
					"match": "\\[\\d+\\];"
				}
			]
		},
		"DataType": {
			"name": "DataType",
			"parse_any": [
				{
					"match": "int"
				},
				{
					"match": "float"
				}
			]
		}
	}

Is same to this.

.. code-block:: json

	{
		"PrimitiveArrayInitializer": {
			"name": "PrimitiveArrayInitializer",
			"parse": [
				{
					"match": "new"
				},
				{
					"name": "DataType",
					"parse_any": [
						{
							"match": "int"
						},
						{
							"match": "float"
						}
					]
				},
				{
					"match": "\\[\\d+\\];"
				}
			]
		}
	}

``optional``
~~~~~~~~~~~~

This indicate that this rule is optional for matching/parsing.

Let's take a look at this example ({x} indicate that x is optional).

.. code-block:: grammar

	[AdditiveExpression]
		[Number] {+ [AdditiveExpression]}

and here is the example converted into a Rule.

.. code-block:: json

	{
		"AdditiveExpression": {
			"name": "AdditiveExpression",
			"parse": [
				{
					"include": "Number"
				},
				{
					"optional": true,
					"parse": [
						{
							"match": "\\+"
						},
						{
							"include": "AdditiveExpression"
						}
					]
				}
			]
		}
	}