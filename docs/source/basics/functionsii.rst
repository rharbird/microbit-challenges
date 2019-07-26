**************
Functions II
**************

Now that you know how to use functions in practice, there are several more concepts that will help you understand behaviour of functions not only in Python,
but other languages as well.  

Scope
======

Global and Local Variables
---------------------------

Imagine you want to use the slightly modified ``printBirthdayGreeting()`` function from before and you want to increment age every time the function is called: ::

	name = "Johann"
	age = 32

	def printBirthdayGreeting():
		age += 1
	    return "Happy Birthday " + name + ", you are " + str(age) + " years old" 

	printBirthdayGreeting()	

Can you spot what is wrong? If you try to run it, you'll probably get this message: `` UnboundLocalError: local variable 'age' referenced before assignment``.

To understand this, we have to talk about scope. Scope is an 'area' in which a variable is defined, can be accessed and written to. From this point of view we know two 
types of variables: global and local. By default, all variables defined within a function are local - you cannot access them outside of the function. And since the scope
within the function is different from the global one, it's possible to use the same name for two different variables.

Can you explain what happened in the code snippet above now?

``age`` outside of ``printBirthdayGreeting()`` function is a global variable. However, when we want to access it inside the function, Python considers it to be a new
local variable. How do we solve this? We can declare the variable ``age`` as ``global``: ::

	name = "Johann"
	age = 32

	def printBirthdayGreeting():
		global age
		age += 1
		return "Happy Birthday " + name + ", you are " + str(age) + " years old"


This will let Python now, that the age variable we mean is the one in global namespace.

.. warning:: Using global variables is generally a bad practice and you should avoid it, since it makes the purpose of your functions less obvious and you can end up with 
			'spaghetti' code. A better way to do this is to pass variable age as one of the arguments of the function (example below).

Here is an example for a function that passes variables as arguments::

	def printBirthdayGreeting(name, age):
		age += 1
		return "Happy Birthday " + name + ", you are " + str(age) + " years old"


.. tip:: You will be hearing about 'best practices' a lot. How do you determine what is a best practice and what is not? In general, best practice is what makes your
	code more readable to others. You can look at style guides_ for a language you're coding in, but in the end it's always about good judgment, since no rule applies
	to all cases. 

.. _guides: https://www.python.org/dev/peps/pep-0008/

.. figure:: assets/code_quality.png
	:align: center

	Source: xkcd https://xkcd.com/1513/


Nonlocal variables
-------------------

A curious case arises with the use of nested functions. So let's say you want to change a local variable of the ``justAnExample()`` function using the nested
function: ::

	def justAnExample():
		def continuingExample():
			variable = "Inner function that changes everything!"

		variable = "Outer function"
		continuingExample()

		print(variable)

	justAnExample() 

You already know why this does not work. But how do you fix it? You cannot declare the variable global, because it's within a function - it's local and there 
is another local scope within the ``continuingExample()`` function. To resolve this situation, you can declare a variable to be ``nonlocal``: ::

	def justAnExample():
		def continuingExample():
			nonlocal variable
			variable = "Inner function that changes everything!"

		variable = "Outer function"
		continuingExample()

		print(variable)

	justAnExample() 

Now the code should print ``"Inner function that changes everything!"`` exactly the way we wanted.

.. note:: To learn more about namespace and scope in Python, look at the documentation_.

.. _documentation: https://docs.python.org/3/tutorial/classes.html

Passing parameters
===================

An important concept that will have a visible impact on the working of your functions is passing parameters. This describes the way a variable is treated as it's passed
in a function - in a pass-by-value scenario, the argument is treated as a new local variable and has no influence on the original variable (if a variable was passed as
an argument). In the case of pass-by-reference, the variable passed as an argument can be affected within a function. In Python, the method of parameter passing is 
a specific combination of the two - parameter are passed by `value of object reference`_.

For a good explanation of passing parameters and the difference between different techniques, I would recommend you to read this `blogpost by Robert Heaton`_.

.. _value of object reference: https://docs.python.org/3/tutorial/controlflow.html#defining-functions
.. _blogpost by Robert Heaton: https://robertheaton.com/2014/02/09/pythons-pass-by-object-reference-as-explained-by-philip-k-dick/
