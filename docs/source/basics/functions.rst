************
Functions I
************

Functions and methods refer to useful snippets of code that serve a specific purpose and are usually used many times in your program. 
You have likely already used both functions and methods without necessarily realising it. 
In this section we will not discuss methods further, but we will explain how to use and write functions. 

Using Functions
================

A great thing about functions is that they can be used in more than one program and avoid code repetition. In the same way you can use functions that other people have 
written. 
In python, useful functions can be assembled into modules (although you don't have to do this) - the ``random`` module is a good example. 
To use functions in the random module you must first `import` the module. Once you've done that, you can use any of the functions in that module. Here are two examples 
of functions from 'random'.

The ``random.randint()`` function will allow us to generate a random integer in a given range::

	from microbit import *
	import random
	
	display.show(str(random.randint(1, 6)))

In the code above, a random number between 1 and 5 will be generated - the upper bound, 6 in this case, is never included.
	
In this code snippet, the function ``random.choice`` will check how many elements are in the names list, generate a random integer in the range 0 to the list length 
and return a list element at the index of the generated integer::

	from microbit import *
	import random
	
	names = ["Mary", "Yolanda", "Damien", "Alia", "Kushal", "Mei Xiu", "Zoltan" ]
	
	display.scroll(random.choice(names))


Writing your own Functions
============================

Functions can help you organise your code and keep it neat and tidy. Here is an example of a simple function that prints out a message::


	def showGreeting():
		print("Hello Friend!")

To use the function, it has to be *called* : ::

	showGreeting()

That's not a very interesting function, is it? You can make functions more powerful by using `parameters` and `return values`. If you think of a function like a black box 
then a parameter is an input value and a return value is what you will get at the other end. Let's say we wanted to write a small program that will greet some 
friends with a message containing their name and age: ::

	from microbit import *

	def printBirthdayGreeting(name, age):
	    return "Happy Birthday " + name + ", you are " + str(age) + " years old"   


 	display.scroll(printBirthdayGreeting("Tabitha", 8))
 	display.scroll(printBirthdayGreeting("Henry", 9))
 	display.scroll(printBirthdayGreeting("Maria", 11))
		
The function ``printBirthdayGreeting`` composes the birthday message for us and returns a string. ``str()`` is used to turn ``age``, 
which is a number, into a string.  You don't have to use functions or return values in your functions unless you want/need to.	

Practice Questions
===================

1. Write a function ``blink(x, y)``, that will blink a LED at coordinates specified by parameters x and y once.

2. Use the ``blink(x, y)`` function to blink all LEDs one after another.

3. Write a function button_count() that will return a tuple containing the number of times button A and button B were pressed. (fix)

4. Combine the two functions into a program that will allow user to set coordinates of blinking LED by pressing buttons.

5. Look at the scripts you wrote previously and check whether you could (or not) improve your code by using functions.