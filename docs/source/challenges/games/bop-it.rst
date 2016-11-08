******
Bop-it
******

.. tabularcolumns:: |L|l|

+--------------------------------+----------------------+
| **Total points possible**	 | **Uses**	        |
+================================+======================+
| 10			 	 | LED display, buttons |
+--------------------------------+----------------------+
	
Description
===========

In this challenge you will make a reaction game similar to bop-it. The first bop-it game, pictured below, was released in the 1960s and since then there have 
been many variants which test your reactions with light, sound and action.


.. figure:: bop_it.jpg
   :scale: 60 %

   The original bop-it design, source: Wikipedia

In the version of the game you create, the player must press the correct button,  ``A`` or ``B``, in under 1 second. If the player
presses the wrong button, the game ends. If they press the correct button, they get a point and can play again.


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
| Prompt the player to press either button ``A``          |            |
| or button ``B``. Hint: use ``random.randint(0,1)``.     |            |
+---------------------------------------------------------+------------+
| Test whether the user has pressed the correct button.   |      1     |
| If the user has pressed the correct button, display     |            |
| a suitable image or message.                            |            |
+---------------------------------------------------------+------------+
| If the user has pressed the wrong                       |      2     |
| button, finish the game.                                |            |
+---------------------------------------------------------+------------+
| If the player's answer was correct, add 1 to the        |      1     |
| player's score.                                         |            |
+---------------------------------------------------------+------------+
| At the end of the game, display the player's score.     |      1     |
+---------------------------------------------------------+------------+
	
	 
Extra points
============

.. tabularcolumns:: |p{14cm}|R|

+---------------------------------------------------------+--------+
| Tasks 		                                  | Points |
+=========================================================+========+
| If the player succeeds, make the time interval for the  | 	 1 |
| next round shorter.                                     |        |
+---------------------------------------------------------+--------+

 
