Data Types
==========

We will use values of different types in our micro:bit programs, for example: we could capture acceleration values from the accelerometer. Alternatively, we might want to count the number of button presses the user has made or to show a message to the user telling them the temperature of the room. In order to do these things we need to be able to describe the data we want to use. Python, and most other programming languages, recognise several data types including:

* Integers - used for whole numbers.
* Floats - used for numbers that contain decimal points or for fractions.
* Strings - used for a combination of any characters that we want to treat as text such as letters, numbers and symbols.  
* Boolean - used for True and False.

In a simple program we might use all of these. Here are the data types we could use for a program storing information about our favourite micro:bit games:

.. image:: dataTypes.png

Variables
---------

A variable can be thought of as a box that the computer can use to store a value. The value held in that box can change or ‘vary’.  All variables are made up of three parts:

* a name
* a type
* a value

.. image variable.jpg

In Python we must give the variables we want to use a name and once we have done that we can start to use them, assigning and manipulating values::

	from microbit import *

	myCount = 0

	while True:
    	   if button_a.was_pressed(): 
		myCount = myCount + 1
	   sleep(2000)
	   print("Number of presses: " + str(count))

In this code, we count the number of button presses for button 'A' and print out the count every 2 seconds.



Operations
----------

Numbers
^^^^^^^
You can use numeric values with the basic arithmetic operators: ``+,-,*,/`` in the same way as you would with a calculator. 
Let's look at an example using arithmetic operators. Imagine that you want to convert the temperature you read from the microbit in Celsius to Fahrenheit, you could use code like this::
	celsiusTemp = temperature()
	fahrenheitTemp = celsiusTemp * 9 / 5 + 32  

The special operator ``%``, called ``mod`` is used to calculate the remainder when one value is divided by another. For example: maybe you'd like to know whether a number is odd or even, you could try dividing it by 2, if it is even then there will be no remainder::

	theNumber = 3
	if theNumber % 2 == 1:
	   print("The number is odd")
	else:
	   print("The number is even")

If the remainder is equal to 1 then this program will print the message "The number is odd", otherwise. the program will print the message "The number is even". You might have written this program in a different way, everybody's programs will be different even when there are only a few lines of code.


Strings
^^^^^^^
The main thing to note about strings is that you can add them together, or concatenate them, with a ``+`` symbol. The code::

	name = "Hayley"

	message = "Well done " + name + ". You are a winner!"

Will concatenate the items on the right hand side of the ``=`` and put the result in the variable called message.

You cannot join numbers and strings together; you must first convert the number to a string using the ``str()`` function if you want to do that::

	x = temperature
	if temperature < 6:
	   display.scroll("Cold" + str(temperature))


Comparisons
-----------
Often in programming we want to compare one value to another, a kind of test. We use these tests or comparisons in selection or loops. Here are some examples of comaparisons written in English::

	score is greater than 100
	name equals "Harry"
 	x acceleration is not equal to 0

Python has a set of comparison operators that allow us to write comparisons easily. They are shown in the table below:

.. tabularcolumns:: |L|l|

+--------------------------------+----------------------------------------+
| **Comparison Operator**        | **Meaning**                            |
+================================+========================================+
| ==                             | Equal to                               |
+--------------------------------+----------------------------------------+
| <, <=                          | Less than, less than or equal to       |
+--------------------------------+----------------------------------------+
| >, >=                          | Greater than, greater than or equal to |
+--------------------------------+----------------------------------------+
| !=                             | not equal to                           |
+--------------------------------+----------------------------------------+

Using Comparisons
^^^^^^^^^^^^^^^^^

.. figure:: booleanLogic.jpg 

	Image from <http://www.bbc.co.uk/education/guides/zy9thyc/revision>

The result of a comparison is either ``True`` or ``False``. True and False are special values known as Bolean values  and we can use can use them to determine what our programs will do. You may have already used some examples that do this. In this example, the micro:bit will show an arrow pointing in the direction
of the tilt in the x axis:: 

	from microbit import *
	
	while True:
	
	    x_acceleration = accelerometer.get_x()
	
	    if x_acceleration > 100:
	         display.show(Image.ARROW_E)
	
	    if  x_acceleration < 100:
	         display.show(Image.ARROW_W) 

Lists
-----

.. figure:: booleanLogic.jpg 
 
	Image from <http://www.bbc.co.uk/education/guides/zy9thyc/revision>

Lists are useful for storing several values together. Let's say we want to store a player's score, we could use a list like the one pictured above. Let's see how to write that in Python.



