***********
Data Types
***********

We will use values of different types in our micro:bit programs, for example: we could capture acceleration values from the accelerometer. Alternatively, we might 
want to count the number of button presses the user has made or to show a message to the user telling them the temperature of the room. In order to do these things 
we need to be able to describe the data we want to use. Python, and most other programming languages, recognise several data types including:

* Integers: whole numbers ``42`` 
* Floating point numbers: numbers that contain decimal points or for fractions ``3.1415``
* Complex numbers: numbers that depict both real and imaginary components  ``2+3j``
* Strings: sequences of characters delimited by quotation marks ``"Hello World!"``
* Booleans: used for True and False values ``True``

In a simple program we might use all of these. Here are the data types we could use for a program storing information about our favourite micro:bit games:

.. figure:: assets/dataTypes.png

   Image from: <http://www.bbc.co.uk/education/guides/zwmbgk7/revision/3>


Operations
===========

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

If the remainder is equal to 1 then this program will print the message "The number is odd", otherwise. the program will print the message "The number is even". You might have written this program in a different way, This shows that people think about problems in different ways and not two programs are likely to be the same. 


Strings
^^^^^^^
The main thing to note about strings is that you can add them together, or concatenate them, with a ``+`` symbol. The code::

	name = "Hayley"

	message = "Well done " + name + ". You are a winner!"

Will concatenate the items on the right hand side of the ``=`` and put the result in the variable called ``message``.

You cannot join numbers and strings together; you must first convert the number to a string using the ``str()`` function if you want to do that::

	x = temperature
	if temperature < 6:
	   display.scroll("Cold" + str(temperature))

Booleans
^^^^^^^^^

Logical operations
-------------------

+----------+--------------------------------+-------------------+
| Operator |  Evaluates to `True` if:       | Example           |
+==========+================================+===================+
| and      |  Both operands are true        | ``True and True`` |
+----------+--------------------------------+-------------------+
| or       |  At least one operand is true  | ``True or False`` |
+----------+--------------------------------+-------------------+
| not      |  Operand is false              | ``not False``     |
+----------+--------------------------------+-------------------+
	



Comparisons
-----------

.. figure:: assets/booleanLogic.jpg 
   :scale: 60 %

   Image from <http://www.bbc.co.uk/education/guides/zy9thyc/revision>

Often in programming we want to compare one value to another, a kind of test. We use these tests or comparisons in selection or loops. Here are some examples of comaparisons written in English::

	score is greater than 100
	name equals "Harry"
 	x acceleration is not equal to 0

Python has a set of comparison operators that allow us to write comparisons easily:

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

Rewriting the comparisons above in Python would be::

	score > 100
	name ==  "Harry"
 	acceleration  != 0


Using Comparisons
^^^^^^^^^^^^^^^^^

The result of a comparison is either ``True`` or ``False``. ``True`` and ``False`` are special values known as **Boolean values**  and we can use can use them to determine what our programs will do. You may have already used some examples that do this. In this example, the micro:bit will show an arrow pointing in the direction
of the tilt in the x axis:: 

	from microbit import *
	
	while True:
	
	    x_acceleration = accelerometer.get_x()
	
	    if x_acceleration > 100:
	         display.show(Image.ARROW_E)
	
	    if  x_acceleration < 100:
	         display.show(Image.ARROW_W) 

