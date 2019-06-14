****************
Data Structures
****************

Lists
======

.. figure:: assets/lists.jpg 
 
   Image from <http://www.bbc.co.uk/education/guides/zy9thyc/revision>

Lists are a datastructures used to store any data type (or structure) in an ordered manner. Let's say we want to store a player's scores, we could use a list like the 
one pictured above. The list has one box for each value. The data stored in a list are called `elements`. 

Let's see how to use a list in Python. To create a list we can tell Python the name  of the list and what it will contain:: 

	from microbit import *

	highScores = [25, 20, 10, 15, 30]       # Create a list and store some values in it.
	print(highScores[0])			# Print 25
	print(highScores[3])			# Print 15


Finding the value of one of the elements in a list is easy as long as you remember that Python counts the elements from '0'. In our ``highScores`` list above, 
``highScores[0]`` is 25 and ``highScores[3]`` is 15.

Here you can also see that particular elements in a list cna be accessed by indexing. Furthermore, it is possible to slice lists to get only a part of a list depending
on the index. If you only want the first three, you can write ``highScores[0:3]``, or, since we are starting at 0, we can shorten it to ``highScores[:3]``. Mind that
the right endpoint is alway excluded, so the 'slice' above refers to the mathematical interval ``[0:2]``.

Not surprisingly, Python has some features to help us do things with lists. The code snippet below will go through the array elements one by one so that we can sum them 
and calculate the average high score::

	print("Average High Score: ") 		

	total = 0
	for score in highScores: 		# For each element ...
		total = total + score

	average = total / len(highScores)  # Use the len() function here to find the length of the array 
	print(average)  

Add to a List
^^^^^^^^^^^^^^
There will be times when we don't know how large to make an array in advance or what the values in the list are going to be. You might want to fill a list with
temperature readings or accelerometer values, for example.  This code illustrates how you can do that:: 

	from microbit import *

	recordedTemperature = [] 		# Create an empty list
	for i in range(100):			# Add 100 temperature values
		recordedTemperature.append(temperature())
		sleep(1000)			 

The ``for`` loop is executed 100 times and ``i`` will have values from 0 to 99. This will measure the temperature every second for 100 seconds and append the value on to the end of the list. 


Delete from a List
^^^^^^^^^^^^^^^^^^^
There are two ways to delete elements from lists that are helpful, you might want to delete an element with a particular value from a list::

	highScores.delete(24)

This will delete the first element with the value 24.
Alternatively, you might want to delete an element at a specific position, if you know it:: 
 
	highScores.pop(3)

This will delete or 'pop' the element at the given position in the list. Note that::

	highScores.pop() 

will delete the last element in the list.

.. seealso: You can look here_ to see more useful native functions on lists.

.. _here: https://docs.python.org/2/tutorial/datastructures.html#tuples-and-sequences

You might be thinking, whether string is a list. Even though string is an array of characters and we can even do similar operations on them (like slicing),
they are both different structures with different methods (try to type ``dir(str)`` and ``dir(list)`` in your console). 


Tuples
=======

Tuples are similar to lists in that the are used to store an ordered sequence of items.::

    highScoresImmutable = 25, 20, 10, 15, 30

You can retrieve values in the same way as in lists, but the most important difference is, that tuples are `immutable`. This means, that while in the ``highScores`` list above, you can change the value of infividual elements,::

    highScores[0] = 42

once you define a tuple, you cannot change the value it stores.  

Sets
=====

Unlike lists and tuples, sets hold an unordered collection of elements with no duplicates. This makes them suitable to use for testing membership or removing 
duplicate elements.

Dictionaries
=============

Dictionary is an unordered set of key:value pairs. It's a rule that all keys are unique and have no duplicates. Unlike lists or tuples, which are indexed by numbers, 
you can retrieve a value by using the key as an index.

For example, you can store the number of times you've read each of your books::

    library_register = { 'Guards! Guards!': 1,
                         'Hitchhiker's Guide To The Galaxy': 3
                         'Twilight': 0
                         'Lord of The Rings': 5 }              
