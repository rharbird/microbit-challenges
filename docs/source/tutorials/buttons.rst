***********
Buttons 
***********

.. py:module:: microbit.button

The micro:bit has two buttons: labelled ``A`` and ``B``.

.. image:: microbit_button.jpg
   :scale: 50 %

You can use the buttons to get input from the user. Perhaps you'd like to start or stop your program with a button press 
or maybe you'd like to know how many times each button has been pressed. 

Basic Functions
================

Checking whether a button is pressed
------------------------------------

Sometimes we just want a program to wait until something happens, for example: we could ask the micro:bit to wait until, say, button 
``A`` is pressed and then print a message. We could do that like this::

	from microbit import *

        while True:
            if button_a.is_pressed():
                display.scroll("A")

Let's break this up into parts. The first bit::

	while True:

This is a standard way to tell the micro:bit to repeat whatever code follows it forever and ever and ever ..... you get the idea.
The next line looks similar to normal English::

        while True:
            if button_a.is_pressed():
                display.scroll("A")

This means, if button ``A`` is pressed then display an ``A`` on the LED screen.

Of course, we usually want to do something a bit more complicated than that. There is a way to check two things,
we can use an ``if`` with an ``else`` like this:: 

        while True:
            if button_a.is_pressed():
                display.scroll("A")
	    else:
		display.scroll(Image.ASLEEP)

This means, if button ``A`` is pressed then display an ``A`` on the LED screen, otherwise, display ``Image.ASLEEP``.

Counting the number of presses
------------------------------
Sometimes you might want to count the number of button presses in a time period. You can do this using the 
``get_presses()`` method.  Here is an example::

    from microbit import *

        while True:
	    sleep(3000)
            count = button_a.get_presses()
            display.scroll(str(count))

The micro:bit will sleep for 3 seconds and then wake up and check how many times button ``A`` was pressed. The number of presses is 
stored in a variable called ``count``. We can't print numbers directly on the LED screen so we convert ``count`` to a string and then display it. Can you think of another way to do this? (Hint: check whether the button has been pressed and add 1 to a counter if it has). 

Advanced Functions
===================

Checking for both buttons
-------------------------
It is possible to check a series of events by using ``if``, ``elif`` and ``else``. Say you wanted to check whether button ``A`` was pressed or button ``B`` was pressed or whether both buttons were pressed at the same time. We could do that like so::  

	from microbit import *

	while True:
	    if button_a.is_pressed() and button_b.is_pressed():
	        display.scroll("AB")
	        break
	    elif button_a.is_pressed():
	        display.scroll("A")
	    elif button_b.is_pressed():
	        display.scroll("B")
	    sleep(100)

.. note:: The keyword ``elif`` just means ``else if``. You can use the longer form ``else if`` if you want.

The code above displays the letter corresponding to the button. If both buttons are pressed at the same time it displays ``AB``.

Has the button been pressed?
----------------------------
The problem with using ``is_pressed()`` is that unless you are pressing the button at that precise moment then you won't 
detect whether the button was ever pressed or not.  

The ``was_pressed()`` function is useful is you want to write code that
occasionally checks whether the button has been pushed but then goes on to
do something else. While the code is doing the something else, it might be
the case that the user pushes the button and lets it go and, because you
haven’t checked to see if it’s pressed then, you might miss it. Well,
the following function will tell you whether a button has been pushed or
released since you last called that function - while your code is doing
something else. In this way you need never miss a button press again::

	from microbit import *

	while True:
	    if button_a.was_pressed(): 
	        display.scroll("A")
	    else:
		display.scroll(Image.ASLEEP)
	    sleep(1000)

What you’ll see is that the display will show an ``A`` for a second
if you press the button, and then ``Image.ASLEEP`` is displayed. If you
press the button while the program is delaying, then the ``A`` won’t
show up immediately, but they will show up when it next tests to see if
the button has been pressed. You’ll see this more clearly if you make
the delay bigger.

Now try using ``button_a.isPressed()`` instead of ``button_a.was_pressed()``. What you will find is 
that if you press the button while the code is delaying the micro:bit will never realise that you pressed it at all.
 
Ideas for Projects with the Buttons
===================================
* Change what is displayed when you press the button.
* Games that need user input… can you make one up?
