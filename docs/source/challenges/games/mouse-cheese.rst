*******************
Where's the Cheese?
*******************

.. tabularcolumns:: |L|l|

+--------------------------------+----------------------+
| **Total points possible**	 | **Uses**	        |
+================================+======================+
| 10			 	 | LED display, buttons |
+--------------------------------+----------------------+
	
Description
===========

In this challenge the player is a mouse and the mouse must eat the cheese before the time is up. The player can 
move around the display by tilting the micro:bit to the left or right, up or down.
When the player lands on the cheese, call function: ``love.badaboom()`` and see what happens. The player must eat  the cheese within  a time 
limit or the game ends.  

Basic Game
===========
Collect points for these stages: 

.. tabularcolumns:: |p{14cm}|R|

+---------------------------------------------------------+------------+
| **Tasks** 		                                  | **Points** |
+=========================================================+============+
| Display a welcome messge.                               | 	     1 |
+---------------------------------------------------------+------------+
| Create loop for the game which repeats every second.    |      1     |
+---------------------------------------------------------+------------+
|                                                         |            |
| Create a player sprite. Display the player sprite in    |      1     |
| top left hand corner of the display.                    |            |
| Hint: store the position of the                         |            |
| player in a list ``player = [0,0]``.                    |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| Move the player sprite to the right if the micro:bit    |            |
| is tilted right and left if the micro:bit is tilted     |      2     |
| left. Hint: Use the values from                         |            |  
| ``accelerometer.get_x()``                               |            |
| to determine the tilt of the board.  			  |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| Move the player sprite upwards if the micro:bit is      |            |
| tipped up. Move the player sprite downwards if the      |      2     |
| micro:bit tipped downward. Hint: use                    |            |
| `accelerometer.get_y()`` to determine the tilt of the   |            |
| board.                                                  |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| Create a cheese sprite. Assign a random position to the |      1     |
| cheese sprite. Hint: store the position of the          |            |
| cheese in a list ``cheese = [0,0]``.                    |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| When the player moves, check whether the	          |      1     | 
| mouse is in the same position as the cheese. If it is   |            |
| then the player has won. call function                  |            |
| ``love.badaboom()`` and see what happens.               |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| Create a timer, if the mouse does not find the cheese   |      1     |
| before the timer expires, the game ends. Hint: at the   |            |
| start of the game get the start time by using function  |            |
| ``microbit.running_time()``.                            |            |
|                                                         |            |
+---------------------------------------------------------+------------+
	
	 
Extra points
============

.. tabularcolumns:: |p{14cm}|R|

+---------------------------------------------------------+------------+
| **Tasks** 		                                  | **Points** |
+=========================================================+============+
|                                                         |            |
| Repeat the game when the mouse reaches the cheese.      |      1     |
| Reduce the amount of time the player has to find the    |            |
| cheese.                                                 |            |
|                                                         |            |
+---------------------------------------------------------+------------+

 
