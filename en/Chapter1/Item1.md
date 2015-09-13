##Item 1: Know Which Version of Python You’re Using

Throughout this book, the majority of example code is in the syntax of Python 3.4 (released March 17, 2014). This book also provides some examples in the syntax of Python 2.7 (released July 3, 2010) to highlight important differences. Most of my advice applies to all of the popular Python runtimes: CPython, Jython, IronPython, PyPy, etc.

Many computers come with multiple versions of the standard CPython runtime preinstalled. However, the default meaning of python on the command-line may not be clear. python is usually an alias for python2.7, but it can sometimes be an alias for older versions like python2.6 or python2.5. To find out exactly which version of Python you’re using, you can use the --version flag.

```bash
$ python —version 
Python 2.7.8
```

Python 3 is usually available under the name python3.

```bash
$ python3 —version 
Python 3.4.2
```

You can also figure out the version of Python you’re using at runtime by inspecting values in the sys built-in module.

```bash
import sys 
print(sys.version_info)
print(sys.version)

>>>

sys.version_info(major=3, minor=4, micro=2, releaselevel=‘final’, serial=0) 3.4.2 (default, Oct 19 2014, 17:52:17)
[GCC 4.2.1 Compatible Apple LLVM 6.0 (clang-600.0.51)]
```

Python 2 and Python 3 are both actively maintained by the Python community. Development on Python 2 is frozen beyond bug fixes, security improvements, and backports to ease the transition from Python 2 to Python 3. Helpful tools like the 2to3
and six exist to make it easier to adopt Python 3 going forward.

Python 3 is constantly getting new features and improvements that will never be added to Python 2. As of the writing of this book, the majority of Python’s most common open source libraries are compatible with Python 3. I strongly encourage you to use Python 3 for your next Python project.


##Things to Remember

* There are two major versions of Python still in active use: Python 2 and Python 3.

* There are multiple popular runtimes for Python: CPython, Jython, IronPython, PyPy, etc.

* Be sure that the command-line for running Python on your system is the version you expect it to be.

* Prefer Python 3 for your next project because that is the primary focus of the Python community.