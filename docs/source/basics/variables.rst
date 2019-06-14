**********
Variables
**********

A variable can be thought of as a box that the computer can use to store a value. The value held in that box can change or ‘vary’.  All variables are made up of three 
parts: a name, a type and a value. In the figure below there are three variables of different types:

.. figure:: assets/variable.jpg
   :scale: 60 %

   Image from: <https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Variables>

The variable ``name`` contains the string ``Bob``, the variable ``winner`` contains the value ``True`` and the variable ``score`` contains the value ``35``.

In Python we must give the variables we want to use a name and once we have done that we can start to use them, assigning and manipulating values::

	from microbit import *

	myCount = 0

	while True:
    	   if button_a.was_pressed(): 
	   myCount = myCount + 1
	   sleep(2000)
	   print("Number of presses: " + str(myCount))

Here we have used the variable ``myCount`` to count the number of button presses for button ``A``.  Can you tell what else this snippet of code does?