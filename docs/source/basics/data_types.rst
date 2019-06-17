***********
Data Types
***********

In order to accurately capture various types of data, programming languages provide us with different data types to allow us to represent them properly.
Each case, whether it is gathering acceleration values from the accelerometer or counting the number of times a button was pressed, requires a different degree
of precision, which is why Python and most other programming languages recognise several data types for representing values, including:


+-----------------+------------------------------------------------------+--------------------+
| *Data Type*     | *Description*                                        | *Example*          |
+=================+======================================================+====================+
| Integers        | Whole numbers                                        | ``42``             |
+-----------------+------------------------------------------------------+--------------------+
| Floats          | Numbers with decimap point, fractions                | ``3.1415``         |
+-----------------+------------------------------------------------------+--------------------+
| Complex numbers | Numbers with both real and an imaginary component    | ``1 + 3j``         |
+-----------------+------------------------------------------------------+--------------------+
| Strings         | Sequences of characters delimited by quotation marks | ``"Hello World!"`` |
+-----------------+------------------------------------------------------+--------------------+
| Booleans        | Values representing true and false values            | ``False``          |
+-----------------+------------------------------------------------------+--------------------+

In a simple program you might use all of these. Here are the data types you could use for a program storing information about your micro:bit games:

.. figure:: assets/dataTypes.png

   Image from: <http://www.bbc.co.uk/education/guides/zwmbgk7/revision/3>


Operations
===========

Numbers
--------
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

If the remainder is equal to 1 then this program will print the message "The number is odd", otherwise. the program will print the message "The number is even". You 
might have written this program in a different way. This shows that people think about problems in different ways and not two programs are likely to be the same. 


Strings
--------
The main thing to note about strings is that you can add them together, or concatenate them, with a ``+`` symbol. The code::

	name = "Hayley"

	message = "Well done " + name + ". You are a winner!"

Will concatenate the items on the right hand side of the ``=`` and put the result in the variable called ``message``.

You cannot join numbers and strings together; you must first convert the number to a string using the ``str()`` function if you want to do that::

	x = temperature
	if temperature < 6:
	   display.scroll("Cold" + str(temperature))

Booleans
---------
A Boolean value is a value that is either ``True`` or ``False``, also represented by `1` and `0`. In python, there is a number of operations that 
allow you to manipulate boolean expressions.  

Comparisons
^^^^^^^^^^^^

.. figure:: assets/booleanLogic.jpg 
   :scale: 60 %

   Image from <http://www.bbc.co.uk/education/guides/zy9thyc/revision>

Comparison operations are useful to test variable values in conditional statements or loops. Here are some examples of 
comparisons written in English::

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

Logical operations
^^^^^^^^^^^^^^^^^^^

Logical operator test not the value of specific variables, but for the truth value of its operands.

+----------+--------------------------------+-------------------+
| Operator |  Evaluates to ``True`` if:     | Example           |
+==========+================================+===================+
| and      |  Both operands are true        | ``True and True`` |
+----------+--------------------------------+-------------------+
| or       |  At least one operand is true  | ``True or False`` |
+----------+--------------------------------+-------------------+
| not      |  Operand is false              | ``not False``     |
+----------+--------------------------------+-------------------+
	

Membership operations
^^^^^^^^^^^^^^^^^^^^^^

Membership operators are useful to determine presence of en element in a sequence.

+----------+----------------------------------------------------------+--------------------------+
| Operator | Evaluates to ``True`` if:                                | Example                  | 
+==========+==========================================================+==========================+
|   in     | A variable value is in the specified sequence            | ``x in [1, 2, 3, 4]``    |
+----------+----------------------------------------------------------+--------------------------+
| not in   | Does not find a variable value in the specified sequence | ``x not in [1, 2, 3, 4]``|
+----------+----------------------------------------------------+--------------------------------+

Using Boolean operations
^^^^^^^^^^^^^^^^^^^^^^^^^

You may have already used some examples that do this. In this example, the micro:bit will 
show an arrow changing in direction according to acceleration:: 

	from microbit import *
	
	while True:
	    x_acceleration = accelerometer.get_x()

		if (x_acceleration <= 100) and (x_acceleration >= 50):
			 display.show(Image.ARROW_N)

	    elif x_acceleration > 100:
	         display.show(Image.ARROW_E) 
	
	    elif  x_acceleration < 50:
	         display.show(Image.ARROW_W) 

		else:
			 display.shiw(Image.ARROW_S)	 