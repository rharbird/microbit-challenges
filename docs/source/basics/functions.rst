***********
Functions
***********

Functions and methods are used in programming to 'boxify' useful snippets of code that serve a specific purpose and use them wherever. 
You have likely already used both functions and methods without us needing to talk about it. 
In this tutorial we will not discuss methods further but we will explain how to use functions and how to write your own. 

Using Functions
================
A great thing about functions is that we can use them in more than one program if we want to. In the same way we can use functions that other people have written too. 
In python, useful functions can be bundled up into modules (although you don't have to do this), the random module is a good example. 
To use functions in the random module we must first `import` the module. Once we've done that, we can use any of the functions in that module. Here are two examples 
of functions in the module 'random' that is generally useful.

Random number in a range
-------------------------
Often we will need to generate a random integer in a given range. The ``random.randint()`` function will allow us to do that::

	from microbit import *
	import random
	
	display.show(str(random.randint(1, 6)))

In the code above, a random number between 1 and 5 will be generated - the upper bound, 6 in this case,  is never included.
	
Random choice
--------------
In this code snippet, the function ``random.choice`` will check how many elements are in the names list, generate a random integer in the range 0 to the list length and return the list element for the random integer::

	from microbit import *
	import random
	
	names = ["Mary", "Yolanda", "Damien", "Alia", "Kushal", "Mei Xiu", "Zoltan" ]
	
	display.scroll(random.choice(names))


Writing your own Functions
============================
Writing your own functions can help you to organise your code and keep it neat and tidy. Here is an example of a simple function that prints out a message::


	def showGreeting():
		print("Hello Friend!")

To use the function we've just written we can call it like this::

	showGreeting()

That's not a very interesting function is it? We can make functions more powerful by using `parameters` and `return values`. If we think of a function like a black box 
then a parameter is an input value and a return value is what we will get out of the other end. Let's say we wanted to write a small program that will greet some 
friends with a message containing their name and age. Our program might look like this::

	from microbit import *

	def printBirthdayGreeting(name, age):
	    return "Happy Birthday " + name + ", you are " + str(age) + " years old"   


 	display.scroll(printBirthdayGreeting("Tabitha", 8))
 	display.scroll(printBirthdayGreeting("Henry", 9))
 	display.scroll(printBirthdayGreeting("Maria", 11))
		
The function ``printBirthdayGreeting`` composes the birthday message for us and returns a string. We have used the python function ``str()`` to turn ``age``, 
which is a number, into a string.  You don't have to use functions or return values in your functions unless you want to.	

Scope
======

Global and Local Variables

Imagine you want to use the slightly modified ``printBirthdayGreeting()`` function from before and you want to increment age every time the function is called: ::

	name = "Johann"
	age = 32

	def printBirthdayGreeting():
		age += 1
	    return "Happy Birthday " + name + ", you are " + str(age) + " years old" 

Can you spot what is wrong? If you try to run it in a shell, you'll probably get this message: `` UnboundLocalError: local variable 'age' referenced before assignment``.

To understand this, we have to talk about scope. Scope is an area in which a variable is defined, can be accessed and written to. From this point of viex, we know two 
types of variables: global and local. By default, all variables defined within a function are local - you cannot access them outside the function. And since the scope
within the function is different from the global one, it's possible to use the same name for two different variables.

Can you explain what happened above now?

``age`` outside of ``printBirthdayGreeting()`` function is a global variable. However, when we want to access it inside the function, Python considers it to be a new
local variable. How do we solve this? We declare the variable ``age`` as ``global``: ::

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

For a really good explanation of passing parameters and the difference between different technqiues I would recommend you to read this `blogpost by Robert Heaton`_.

.. _value of object reference: https://docs.python.org/3/tutorial/controlflow.html#defining-functions
.. _blogpost by Robert Heaton: https://robertheaton.com/2014/02/09/pythons-pass-by-object-reference-as-explained-by-philip-k-dick/

