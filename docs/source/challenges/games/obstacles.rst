*********
Obstacles
*********

.. tabularcolumns:: |L|l|

+--------------------------------+----------------------+
| **Total points possible**	 | **Uses**	        |
+================================+======================+
| 10			 	 | LED display, buttons |
+--------------------------------+----------------------+
	
Description
===========

In this challenge  the player is driving down a road or race track. There are obstacles in the road and  the player 
must  dodge them using the ``A`` and ``B`` buttons on the micro:bit. If the player hits an obstacle the game ends. 

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
| Create a player sprite in any column in the bottom row. |            |
| Display the pixel at maximum brightness.                |            |
+---------------------------------------------------------+------------+
| Move the player sprite 1 pixel upwards each time the    |      1     |
| loop repeats. If the player sprite is in row 0, move    |            |
| the player sprite back to row 4.                        |            |
| Hint: store the position of the                         |            |
| player in a list: ``player = [0,0]``.                   |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| Move the player sprite to the right if button           |            |
| ``B`` is pressed and left if button ``A`` is pressed.   |      1     |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| Create an obstacle sprite in any column in the top row. |      2     |
| Display the pixel at a low brightness.                  |            |
| The obstacle should move down 1 pixel every time        |            |
| the game loop repeats. Hint: store the position of the  |            |
| obstacle in a list ``obstacle = [0,0]``.                |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| Now when you create the obstacle sprite, place it in a  |            |
| random column on the display.                           |      1     |
| Hint: use ``random.randint(0,4)``.                      |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| Every time the loop repeats, check whether the player   |      2     |
| has collided with the obstacle. If there is a collision,|            |
| the game ends.                                          |            |
|                                                         |            |
+---------------------------------------------------------+------------+
	
	 
Extra points
============

.. tabularcolumns:: |p{14cm}|R|

+---------------------------------------------------------+------------+
| **Tasks** 		                                  | **Points** |
+=========================================================+============+
|                                                         |            |
| At the start of the game, give the player 3 lives.      |      1     |
| Subtract a life every time there is a collision. End    |            |
| game when the player has no lives left.                 |            |
|                                                         |            |
+---------------------------------------------------------+------------+

 
