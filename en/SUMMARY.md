#Contents

* [Preface](Preface/Preface.md) 

* [Acknowledgments](Preface/Acknowledgments.md) 

* [About the Author](Preface/About_the_Author.md)

* [Chapter 1: Pythonic Thinking](Chapter1/Chapter1.md)

	- [Item 1: Know Which Version of Python You’re Using](Chapter1/Item1.md) 
	- [Item 2: Follow the PEP8 Style Guide](Chapter1/Item2.md)
	- [Item 3: Know the Differences Between bytes, str, and unicode](Chapter1/Item3.md) 
	- [Item 4: Write Helper Functions Instead of Complex Expressions](Chapter1/Item4.md) 
	- [Item 5: Know How to Slice Sequences](Chapter1/Item5.md)
	- [Item 6: Avoid Using start, end, and stride in a Single Slice](Chapter1/Item6.md) 
	- [Item 7: Use List Comprehensions Instead of map and filter](Chapter1/Item7.md) 
	- [Item 8: Avoid More Than Two Expressions in List Comprehensions](Chapter1/Item8.md) 
	- Item 9: Consider Generator Expressions for Large Comprehensions 
	- Item 10: Prefer enumerate Over range
	- Item 11: Use zip to Process Iterators in Parallel
	- Item 12: Avoid else Blocks After for and while Loops
	- Item 13: Take Advantage of Each Block in try/except/else/finally 
	
* Chapter 2: Functions

	- Item 14: Prefer Exceptions to Returning None
	- Item 15: Know How Closures Interact with Variable Scope 
	- Item 16: Consider Generators Instead of Returning Lists 
	- Item 17: Be Defensive When Iterating Over Arguments
	- Item 18: Reduce Visual Noise with Variable Positional Arguments 
	- Item 19: Provide Optional Behavior with Keyword Arguments
	- Item 20: Use None and Docstrings to Specify Dynamic Default Arguments 
	- Item 21: Enforce Clarity with Keyword-Only Arguments
	
* Chapter 3: Classes and Inheritance

	- Item 22: Prefer Helper Classes Over Bookkeeping with Dictionaries and Tuples 		- Item 23: Accept Functions for Simple Interfaces Instead of Classes
	- Item 24: Use @classmethod Polymorphism to Construct Objects Generically
	- Item 25: Initialize Parent Classes with super
	- Item 26: Use Multiple Inheritance Only for Mix-in Utility Classes 
	- Item 27: Prefer Public Attributes Over Private Ones
	- Item 28: Inherit from collections.abc for Custom Container Types
	
* Chapter 4: Metaclasses and Attributes

	- Item 29: Use Plain Attributes Instead of Get and Set Methods 
	- Item 30: Consider @property Instead of Refactoring Attributes 
	- Item 31: Use Descriptors for Reusable @property Methods
	- Item 32: Use __getattr__, __getattribute__, and __setattr__ for Lazy Attributes
	- Item 33: Validate Subclasses with Metaclasses 
	- Item 34: Register Class Existence with Metaclasses
	- Item 35: Annotate Class Attributes with Metaclasses 
	
* Chapter 5: Concurrency and Parallelism
	
	- Item 36: Use subprocess to Manage Child Processes
	- Item 37: Use Threads for Blocking I/O, Avoid for Parallelism 
	- Item 38: Use Lock to Prevent Data Races in Threads
	- Item 39: Use Queue to Coordinate Work Between Threads
	- Item 40: Consider Coroutines to Run Many Functions Concurrently 
	- Item 41: Consider concurrent.futures for True Parallelism
	
* Chapter 6: Built-in Modules

	- Item 42: Define Function Decorators with functools.wraps
	- Item 43: Consider contextlib and with Statements for Reusable try/finally Behavior
	- Item 44: Make pickle Reliable with copyreg
	- Item 45: Use datetime Instead of time for Local Clocks 
	- Item 46: Use Built-in Algorithms and Data Structures
	- Item 47: Use decimal When Precision Is Paramount 
	- Item 48: Know Where to Find Community-Built Modules
	
* Chapter 7: Collaboration

	- Item 49: Write Docstrings for Every Function, Class, and Module 
	- Item 50: Use Packages to Organize Modules and Provide Stable APIs
	- Item 51: Define a Root Exception to Insulate Callers from APIs 
	- Item 52: Know How to Break Circular Dependencies
	- Item 53: Use Virtual Environments for Isolated and Reproducible Dependencies 
	
* Chapter 8: Production

	- Item 54: Consider Module-Scoped Code to Configure Deployment Environments 
	- Item 55: Use repr Strings for Debugging Output
	- Item 56: Test Everything with unittest
	- Item 57: Consider Interactive Debugging with pdb 
	- Item 58: Profile Before Optimizing
	- Item 59: Use tracemalloc to Understand Memory Usage and Leaks Index