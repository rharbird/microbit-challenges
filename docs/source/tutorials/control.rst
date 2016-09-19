*******
Control
*******
Sometimes you need to control what happens in your program, do you need to repeat something over and over again? 
Loops will help you there. Perhaps you only want something to happen if a particular event has occurred? Take a look at conditions
to help you there. Of course, in any program you will likely use all of these to make your micro:bit function and that's where 
things get interesting.


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


While loops
-----------
One of the most common things you might want to do with a ``while`` loop is to do something forever, that is until the micro:bit
is turned off or reset. Maybe you have programmed your micro:bit with your favourite game or perhaps it is collecting 
temperature data in the corner of a classroom. Here is an example of some code to repeat forever::

	from microbit import *
	
	while(True):
	    display.scroll("Hello UCL)

This code will repeatedly display the message `Hello UCL`. You will likely have at least one ``while(True):`` loop in your program
to keep the microbit going.

But what if you want to do an action only whilst something is happening? Perhaps you would like to display an image
if the temperature on the microbit goes below a certain value so you'll need to test the temperature::

	from microbit import *
	
	while(temperature() < 18):
	    display.scroll(Image.SAD)
	    sleep(1000)

	display.clear()

Conditions
==========
Choices, choices, choices. Sometimes you want to trigger an action if something specific has happened. We can use an ``if ... else`` statement for that.
In this example we display a flashing heart if button ``A`` is pressed and a happy face if button ``B`` is pressed. If no buttons are pressed then we display a ghost:: 

	from microbit import *
	import love
	
	while(True):
	    if button_a.is_pressed():
		love.badaboom()
	
	    elif button_b.is_pressed():
		display.show(Image.HAPPY)
	
	    else:
		display.show(Image.GHOST)

	    sleep(100)

Notice how we have shortened ``else if`` to become ``elif``, you don't have to do this if you don't want to, it just saves typing.


