*****************
Data Structures
****************

Lists
-----

.. figure:: assets/lists.jpg 
 
   Image from <http://www.bbc.co.uk/education/guides/zy9thyc/revision>

Lists are useful for storing several values together. Let's say we want to store a player's scores, we could use a list like the one pictured above. The list has one box for each value. The cells or boxes are known as `elelments`. 

Let's see how to use a list in Python. To create a list we can tell Python the name  of the list and what it will contain:: 

	from microbit import *

	highScores = [25, 20, 10, 15, 30]       # Create a list and store some values in it.
	print(highScores[0])			# Print 25
	print(highScores[3])			# Print 15


Finding the value of one of the elements in a list is easy as long as you remember that Python counts the elements from '0'. In our ``highScores`` list above, ``highScores[0]`` is 25 and ``highScores[3]`` is 15.

Not surprisingly, Python has some features to help us do things with lists. The code snippet below will go through the array elements one by one so that we can sum them and calculate the average high score::

	print("Average High Score: ") 		

	total = 0
	for score in highScores: 		# For each element ...
		total = total + score

	average = total / len(highScores)  # Use the len() function here to find the length of the array 
	print(average)  

Add to a List
^^^^^^^^^^^^^
There will be times when we don't know how large to make an array in advance or what the values in the list are going to be. You might want to fill a list with
temperature readings or accelerometer values, for example.  This code illustrates how you can do that:: 

	from microbit import *

	recordedTemperature = [] 		# Create an empty list
	for i in range(100):			# Add 100 temperature values
		recordedTemperature.append(temperature())
		sleep(1000)			 

The ``for`` loop is executed 100 times and ``i`` will have values from 0 to 99. This will measure the temperature every second for 100 seconds and append the value on to the end of the list. 


Delete from a List
^^^^^^^^^^^^^^^^^^
There are two ways to delete elements from lists that are helpful, you might want to delete an element with a particular value from a list::

	highScores.delete(24)

This will delete the first element with the value 24.
Alternatively, you might want to delete an element at a specific position, if you know it:: 
 
	highScores.pop(3)

This will delete or 'pop' the element at the given position in the list. Note that::

	highScores.pop() 

will delete the last element in the list.

Tuples

Dictionaries