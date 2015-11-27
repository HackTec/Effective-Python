##第一条: 知道你正在使用哪个版本的Python

在本书中，主要的代码的例子使用Python3.4的语法(于2014年3月17日发布)。本书也会以Python2.7(于2010年7月3日发布)的语法提供一些例子来强调重要的不同之处。我的大多数建议适用于所有流行的Python运行环境中：CPython，Jython,IronPyhon,PyPy等等。

许多电脑预安装了多个标准的CPython运行环境的版本。然而，默认的python命令行的含义可能并不明确。python通常是python2.7的别名，但是有些时候它也可能是更老的版本，比如python2.6或者python2.5。为了正确的判断你正在用哪个版本的python，你可以使用 `--version`的标志。

	$python —version
	Python 2.7.8
	
Python 3通常可以使用名字`python3`来获取

	$ python3 —version 
	Python 3.4.2
	
你也可以通过检查`sys`内建模块里面的值来判断你正在使用的python版本。

	import sys 
	print(sys.version_info)
	print(sys.version)
	
	>>>
	
	sys.version_info(major=3, minor=4, micro=2, releaselevel=‘final’, serial=0) 3.4.2 (default, Oct 19 2014, 17:52:17)
	[GCC 4.2.1 Compatible Apple LLVM 6.0 (clang-600.0.51)]
	
	
`Python 2` 和 `Python 3`都被Python社区积极的维护着。除了一些bug修复、安全的改进，以及让从`Python 2`过度到`Python 3`更容易的补丁之外，`Python 2`的发展已经停止。一些有用的工具诸如2to3和six的存在使得`Python 2`更容易适应`Python 3`的向前兼容。

`Python 3`在持续的获取新的特性以及改进，而这些并不会被加到`Python 2`中。在写这本书的时候，大多常见的Python开源库已经兼容了`Python 3`。我强烈建议你用`Python 3`作为你的下一个Python项目。

##请记住

* 有两种主要的Python版本被经常的使用：`Python 2`和`Python 3`。
* 有很多流行的Python的运行环境：CPython,Jython,IronPython,PyPy。
* 确认你系统上的命令行的运行环境是你想要的。
* 更愿意`Python 3`能作为你下一个项目的语言，因为它是Python社区的主要焦点。

