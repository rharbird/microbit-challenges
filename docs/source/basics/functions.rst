************
Functions I
************

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


