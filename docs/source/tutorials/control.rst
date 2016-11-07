******************
Control Structures
******************
Sometimes you need to control what happens in your program, do you need to repeat something over and over again? 
Loops will help you there. Perhaps you only want something to happen if a particular event has occurred? Take a look at conditions
to help you there. Of course, in any program you will likely use all of these to make your micro:bit do what you want and that's where 
things get interesting.

.. image:: control_structures_icons.jpg
   :align: left

You have already seen how to write instructions or statements sequentially and generated input and output. In the remainder of this chapter we will look at loops, selection and functions.

Loops
=====
There are two types of loops: ``for`` loops let you count the number of times you do something and ``while`` loops which let you
perform an action until a condition you've specified is no longer happening. 

For loops
---------
There are times when you want to do an action a specific number of times. For example: perhaps you'd like to turn on the
LEDs on two sides of the display to make a track. You can use a ``for`` loop to count for you like this::

	from microbit import *

	for i in range (5):
	   display.set_pixel(0,i,9) 	# set the pixel in column 0, row i to 9 
	   display.set_pixel(4,i,9)	# set the pixel in column 4, row i to 9 

Here is another example.  You could use a ``for loop`` to set all the LEDs on one at a time::

    from microbit import *

    display.clear()
    for x in range(0, 5):
        for y in range(0, 5):
            display.set_pixel(x,y,9)  

The ``for loop`` lets you execute a loop a specific number of times using a counter. The outer loop::

        for x in range(0,5):

will execute the loop five times substituting ``x`` for consecutive values in the range ``0`` to ``4`` each time. The loop will stop before it reaches 5, the final value in the range.

The inner loop::

        for y in range(0,5):

will execute the loop five times substituting ``y`` for consecutive values in the range ``0`` to ``4`` each time. Again, the loop will stop before it reaches the final value in the range.


While loops
-----------
One of the most common things you might want to do with a ``while`` loop is to do something forever, that is until the micro:bit
is turned off or reset. Maybe you have programmed your micro:bit with your favourite game or perhaps it is collecting 
temperature data in the corner of a classroom. Here is an example of some code to repeat forever::

	from microbit import *
	
	while True:
	    display.scroll("Hello UCL)

This code will repeatedly display the message ``Hello UCL``. You will likely have at least one ``while True:`` loop in your program
to keep the micro:bit going.

But what if you want to do an action only whilst something is happening? Perhaps you would like to display an image
if the temperature on the micro:bit goes below a certain value so you'll need to test the temperature::

	from microbit import *
	
	while temperature() < 18:
	    display.scroll(Image.SAD)
	    sleep(1000)

	display.clear()

Selection
=========
Choices, choices, choices. Sometimes you want to trigger an action if something specific has happened. We can use an ``if ... else`` statement for that.
In this example we display a flashing heart if button ``A`` is pressed and a happy face if button ``B`` is pressed. If no buttons are pressed then we display a ghost:: 

	from microbit import *
	import love
	
	while True:
	    if button_a.is_pressed():
		love.badaboom()
	
	    elif button_b.is_pressed():
		display.show(Image.HAPPY)
	
	    else:
		display.show(Image.GHOST)

	    sleep(100)

Notice how we have shortened ``else if`` to become ``elif``, you don't have to do this if you don't want to, it just saves typing.

Functions 
=========
Functions and methods are used in programming to 'parcel up' useful snippets of code and use them whenever we want. You have likely already used both functions and methods without us needing to talk about it. In this tutorial we will not discuss methods further but we will explain how to use functions and how to write your own. 

Using Functions
---------------
A great thing about functions is that we can use them in more than one program if we want to. In the same way we can use functions that other people have written too. In python, useful functions can be bundled up into modules (although you don't have to do this), the random module is a good example. To use functions in the random module we must first `import` the module. Once we've done that, we can use any of the functions in that module. Here are two examples of functions in the random module that you might .
nt to use.

Random number in a range
^^^^^^^^^^^^^^^^^^^^^^^^
Most of time, we will want to generate a random integer in a given range. The ``random.randint()`` function will allow us to do that::

	from microbit import *
	import random
	
	display.show(str(random.randint(1, 6)))

In the code above, a random number between 1 and 5 will be generated - the upper bound, 6 in this case,  is never included.


	
Random choice
^^^^^^^^^^^^^
In this code snippet, the function ``random.choice`` will check how many elements are in the names list, generate a random integer in the range 0 to the list length and return the list element for the random integer::

	from microbit import *
	import random
	
	names = ["Mary", "Yolanda", "Damien", "Alia", "Kushal", "Mei Xiu", "Zoltan" ]
	
	display.scroll(random.choice(names))


Writing your own Functions
--------------------------
Writing your own functions can help you to organise your code and keep it neat and tidy. Here is an example of a simple function that prints out a message::


	def showGreeting():
		print("Hello Friend!")

To use the function we've just written we can call it like this::

	showGreeting()

That's not a very interesting function is it? We can make functions more powerful by using `parameters` and `return values`. If we think of a function like a black box then a parameter is an input value and a return value is what we will get out of the other end. Let's say we wanted to write a small program that will greet some friends with a message containing their name and age. Our program might look like this::

	from microbit import *

	def printBirthday(name, age):
	    return "Happy Birthday " + name + ", you are " + str(age) + " years old"   


 	display.scroll(printBirthday("Tabitha", 8))
 	display.scroll(printBirthday("Henry", 9))
 	display.scroll(printBirthday("Maria", 11))
		
The function ``printBirthday`` composes the birthday message for us and returns a string. We have used the python function ``str()`` to turn ``age``, which is a number, into a string.  You don't have to use functions or return values in your functions unless you want to.	
