#Preface


The Python programming language has unique strengths and charms that can be hard to grasp. Many programmers familiar with other languages often approach Python from a limited mindset instead of embracing its full expressivity. Some programmers go too far in the other direction, overusing Python features that can cause big problems later.

This book provides insight into the Pythonic way of writing programs: the best way to use Python. It builds on a fundamental understanding of the language that I assume you already have. Novice programmers will learn the best practices of Python’s capabilities. Experienced programmers will learn how to embrace the strangeness of a new tool with confidence.

My goal is to prepare you to make a big impact with Python.


#What This Book Covers

Each chapter in this book contains a broad but related set of items. Feel free to jump between items and follow your interest. Each item contains concise and specific guidance explaining how you can write Python programs more effectively. Items include advice on what to do, what to avoid, how to strike the right balance, and why this is the best choice.

The items in this book are for Python 3 and Python 2 programmers alike (see Item 1: “Know Which Version of Python You’re Using”). Programmers using alternative runtimes like Jython, IronPython, or PyPy should also find the majority of items to be applicable.


#Chapter 1: Pythonic Thinking

The Python community has come to use the adjective Pythonic to describe code that follows a particular style. The idioms of Python have emerged over time through experience using the language and working with others. This chapter covers the best way to do the most common things in Python.


#Chapter 2: Functions

Functions in Python have a variety of extra features that make a programmer’s life easier. Some are similar to capabilities in other programming languages, but many are unique to Python. This chapter covers how to use functions to clarify intention, promote reuse, and reduce bugs.


#Chapter 3: Classes and Inheritance

Python is an object-oriented language. Getting things done in Python often requires writing new classes and defining how they interact through their interfaces and hierarchies. This chapter covers how to use classes and inheritance to express your intended behaviors with objects.

#Chapter 4: Metaclasses and Attributes

Metaclasses and dynamic attributes are powerful Python features. However, they also enable you to implement extremely bizarre and unexpected behaviors. This chapter covers the common idioms for using these mechanisms to ensure that you follow the rule of least surprise.


#Chapter 5: Concurrency and Parallelism

Python makes it easy to write concurrent programs that do many different things seemingly at the same time. Python can also be used to do parallel work through system calls, subprocesses, and C-extensions. This chapter covers how to best utilize Python in these subtly different situations.


#Chapter 6: Built-in Modules

Python is installed with many of the important modules that you’ll need to write programs. These standard packages are so closely intertwined with idiomatic Python that they may as well be part of the language specification. This chapter covers the essential built-in modules.


#Chapter 7: Collaboration

Collaborating on Python programs requires you to be deliberate about how you write your code. Even if you’re working alone, you’ll want to understand how to use modules written by others. This chapter covers the standard tools and best practices that enable people to work together on Python programs.


#Chapter 8: Production

Python has facilities for adapting to multiple deployment environments. It also has built-in modules that aid in hardening your programs and making them bulletproof. This chapter covers how to use Python to debug, optimize, and test your programs to maximize quality and performance at runtime.


#Conventions Used in This Book

Python code snippets in this book are in monospace font and have syntax highlighting. I take some artistic license with the Python style guide to make the code examples better fit the format of a book or to highlight the most important parts. When lines are long, I use	characters to indicate that they wrap. I truncate snippets with ellipses comments (#…) to indicate regions where code exists that isn’t essential for expressing the point. I’ve also left out embedded documentation to reduce the size of code examples. I strongly suggest that you don’t do this in your projects; instead, you should follow the style guide (see Item 2: “Follow the PEP8 Style Guide”) and write documentation (see Item 49: “Write Docstrings for Every Function, Class, and Module”).

Most code snippets in this book are accompanied by the corresponding output from
running the code. When I say “output,” I mean console or terminal output: what you see when running the Python program in an interactive interpreter. Output sections are in monospace font and are preceded by a >>> line (the Python interactive prompt). The idea is that you could type the code snippets into a Python shell and reproduce the expected output.

Finally, there are some other sections in monospace font that are not preceded by a >>> line. These represent the output of running programs besides the Python interpreter. These examples often begin with $ characters to indicate that I’m running programs from a command-line shell like Bash.


#Where to Get the Code and Errata

It’s useful to view some of the examples in this book as whole programs without interleaved prose. This also gives you a chance to tinker with the code yourself and understand why the program works as described. You can find the source code for all code snippets in this book on the book’s website (http://www.effectivepython.com). Any errors found in the book will have corrections posted on the website.