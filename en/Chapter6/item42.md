##Item 42: Define Function Decorators with functools.wraps

Python has special syntax for decorators that can be applied to functions. Decorators have
the ability to run additional code before and after any calls to the functions they wrap. This
allows them to access and modify input arguments and return values. This functionality
can be useful for enforcing semantics, debugging, registering functions, and more.

For example, say you want to print the arguments and return value of a function call. This
is especially helpful when debugging a stack of function calls from a recursive function.
Here, I define such a decorator:

    def trace(func):
    	def wrapper(*args, **kwargs):
    		result = func(*args, **kwargs)
    		print(‘%s(%r, %r) -> %r’ %
    			  (func.__name__, args, kwargs, result))
    		return result
    	return wrapper

I can apply this to a function using the @ symbol.
    
    @trace
    def fibonacci(n):
    	“““Return the n-th Fibonacci number”””
    	if n in (0, 1):
    		return n
    	return (fibonacci(n - 2) + fibonacci(n - 1))

The @ symbol is equivalent to calling the decorator on the function it wraps and assigning
the return value to the original name in the same scope.

    fibonacci = trace(fibonacci)

Calling this decorated function will run the wrapper code before and after fibonacci
runs, printing the arguments and return value at each level in the recursive stack.

    fibonacci(3)
    >>>
    fibonacci((1,), {}) -> 1
    fibonacci((0,), {}) -> 0
    fibonacci((1,), {}) -> 1
    fibonacci((2,), {}) -> 1
    fibonacci((3,), {}) -> 2

This works well, but it has an unintended side effect. The value returned by the decorator
—the function that’s called above—doesn’t think it’s named fibonacci.

    print(fibonacci)
    >>>
    <function trace.<locals>.wrapper at 0x107f7ed08>

The cause of this isn’t hard to see. The trace function returns the wrapper it defines.
The wrapper function is what’s assigned to the fibonacci name in the containing
module because of the decorator. This behavior is problematic because it undermines tools
that do introspection, such as debuggers (see Item 57: “Consider Interactive Debugging
with pdb”) and object serializers (see Item 44: “Make pickle Reliable with
copyreg”).

For example, the help built-in function is useless on the decorated fibonacci
function.

    help(fibonacci)
    >>>
    Help on function wrapper in module __main__:
    wrapper(*args, **kwargs)

The solution is to use the wraps helper function from the functools built-in module.
This is a decorator that helps you write decorators. Applying it to the wrapper function
will copy all of the important metadata about the inner function to the outer function.

    def trace(func):
    	@wraps(func)
    	def wrapper(*args, **kwargs):
    		# …
    	return wrapper
    @trace
    def fibonacci(n):
    		# …

Now, running the help function produces the expected result, even though the function is
decorated.

    help(fibonacci)
    >>>
    Help on function fibonacci in module __main__:
    fibonacci(n)
    	Return the n-th Fibonacci number

Calling help is just one example of how decorators can subtly cause problems. Python
functions have many other standard attributes (e.g., `__name__, __module__`) that must
be preserved to maintain the interface of functions in the language. Using wraps ensures
that you’ll always get the correct behavior.

##Things to Remember

* Decorators are Python syntax for allowing one function to modify another function
at runtime.
* Using decorators can cause strange behaviors in tools that do introspection, such as
debuggers.
* Use the wraps decorator from the functools built-in module when you define
your own decorators to avoid any issues.