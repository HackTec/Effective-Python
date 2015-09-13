##Item 2: Follow the PEP8 Style Guide

Python Enhancement Proposal #8, otherwise known as PEP8, is the style guide for how to format Python code. You are welcome to write Python code however you want, as long as it has valid syntax. However, using a consistent style makes your code more approachable and easier to read. Sharing a common style with other Python programmers in the larger community facilitates collaboration on projects. But even if you are the only one who will ever read your code, following the style guide will make it easier to change things later.

PEP8 has a wealth of details about how to write clear Python code. It continues to be updated as the Python language evolves. It’s worth reading the whole guide online (<http://www.python.org/dev/peps/pep-0008/>). Here are a few rules you should be sure to follow:

**Whitespace:** In Python, whitespace is syntactically significant. Python programmers are especially sensitive to the effects of whitespace on code clarity.

* Use spaces instead of tabs for indentation.

* Use four spaces for each level of syntactically significant indenting. • Lines should be 79 characters in length or less.
* Continuations of long expressions onto additional lines should be indented by four extra spaces from their normal indentation level.

* In a file, functions and classes should be separated by two blank lines. • In a class, methods should be separated by one blank line.
* Don’t put spaces around list indexes, function calls, or keyword argument assignments.

* Put one—and only one—space before and after variable assignments.

**Naming:** PEP8 suggests unique styles of naming for different parts in the language. This makes it easy to distinguish which type corresponds to each name when reading code.

* Functions, variables, and attributes should be in lowercase_underscore format.

* Protected instance attributes should be in _leading_underscore format.

* Private instance attributes should be in __double_leading_underscore format.

* Classes and exceptions should be in CapitalizedWord format. • Module-level constants should be in ALL_CAPS format.
* Instance methods in classes should use self as the name of the first parameter (which refers to the object).

* Class methods should use cls as the name of the first parameter (which refers to the class).

**Expressions and Statements:** The Zen of Python states: “There should be one—and preferably only one—obvious way to do it.” PEP8 attempts to codify this style in its guidance for expressions and statements.

* Use inline negation (if a is not b) instead of negation of positive expressions (if not a is b).

* Don’t check for empty values (like [] or '') by checking the length (if len(somelist) == 0). Use if not somelist and assume empty values implicitly evaluate to False.

* The same thing goes for non-empty values (like [1] or 'hi'). The statement if somelist is implicitly True for non-empty values.

* Avoid single-line if statements, for and while loops, and except compound statements. Spread these over multiple lines for clarity.

* Always put import statements at the top of a file.

* Always use absolute names for modules when importing them, not names relative to the current module’s own path. For example, to import the foo module from the bar package, you should do from bar import foo, not just import foo.

* If you must do relative imports, use the explicit syntax from . import foo.

* Imports should be in sections in the following order: standard library modules, third-party modules, your own modules. Each subsection should have imports in alphabetical order.

**Note**

The Pylint tool (<http://www.pylint.org/>) is a popular static analyzer for Python source code. Pylint provides automated enforcement of the PEP8 style guide and detects many other types of common errors in Python programs.

##Things to Remember

* Always follow the PEP8 style guide when writing Python code.

* Sharing a common style with the larger Python community facilitates collaboration with others.

* Using a consistent style makes it easier to modify your own code later.