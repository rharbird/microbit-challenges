**************
Catch the Eggs
**************

.. tabularcolumns:: |L|l|

+--------------------------------+----------------------+
| **Total points possible**	 | **Uses**	        |
+================================+======================+
| 10			 	 | LED display, buttons |
+--------------------------------+----------------------+
	
Description
===========

In this challenge you will test the player's ability to catch an egg in a basket. Imagine there is 
a chocolate egg dropping from the sky. The player must catch the egg before it hits the ground. The player
can move either right or left by using the ``A`` and ``B`` buttons on the micro:bit. If the egg hits 
the floor the game ends. 


Basic Game
===========
Collect points for these stages: 

.. tabularcolumns:: |p{14cm}|R|

+---------------------------------------------------------+------------+
| **Tasks** 		                                  | **Points** |
+=========================================================+============+
| Display a welcome message.                              | 	     1 |
+---------------------------------------------------------+------------+
| Create loop for the game which repeats every second.    |      1     |
+---------------------------------------------------------+------------+
|                                                         |            |
| Create a player sprite in column 0, row 3.              |      1     |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| Move the player sprite to the right if button           |            |
| ``B`` is pressed and left if button ``A`` is pressed.   |      1     |
| Hint: store the position of the                         |            |
| player in a list ``player = [0,0]``.                    |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| Create an egg sprite. The egg will start at             |      1     |
| the top of the display and move down 1 pixel every time |            |
| the game loop repeats. Hint: store the position of the  |            |
| egg in a list ``egg = [0,0]``.                          |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| Create the egg sprite in a random column on the         |      1     |
| display. Hint: use ``random.randint(0,4)``.             |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| Every time the loop repeats, check whether the player   |      2     |
| has collided with the egg. If there is a collision,     |            |
| the player has caught the egg and the game ends.        |            |
| Display an image or message to congratulate the player. |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| If the egg drops to the bottom of the display and there |            |
| has been no collision then set the position of the egg  |            |
| to a random column at the top of the display.           |      1     |
|                                                         |            |
+---------------------------------------------------------+------------+
	
	 
Extra points
============

.. tabularcolumns:: |p{14cm}|R|

+---------------------------------------------------------+------------+
| **Tasks** 		                                  | **Points** |
+=========================================================+============+
|                                                         |            |
| Let the player continue catching eggs until they drop   |      1     |
| one. When the game ends, display the player's score.    |            |
|                                                         |            |
+---------------------------------------------------------+------------+

 
