***********************
Rocki, Paper, Scissors
***********************

.. tabularcolumns:: |L|l|

+--------------------------------+-----------------------------------------------------------------------+
| **Total points possible**	 | **Uses**	                                                         |
+================================+=======================================================================+
| 10			 	 | Two Micro:bits, Battery pack with 2 AAA batteries, Radio, LED Display |
+--------------------------------+-----------------------------------------------------------------------+
	
Description
===========
In this project, we will make a rock, paper, scissors game using use the radio on the micro:bit to send messages from one microbit to another. 

Basic Task
===========
Collect points for these stages: 

.. tabularcolumns:: |p{14cm}|R|

+---------------------------------------------------------+------------+
| **Tasks** 		                                  | **Points** |
+=========================================================+============+
| Read the radio tutorial sheet.                          |            |
| Write code to transmit and receive messages.            |    2       |
| Print the message sent on the REPL.                     |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| Choose which micro:bit will host the R,P,S game and     |    1       |
| which micro:bit will be used by the player. On the      |            |
| host micro:bit, display a welcome message.              |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| On the host micro:bit, use ``while True:`` for the      |    2       |
| game loop. Use the ``random.randint(1,3)`` function to  |            |
| generate a number between 1 and 3. This will represent  |            |
| rock, paper or scissors.                                |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
|                                                         |            |
|                                                         |            |
|                                                         |            |
| Add some code so that the message is sent when button   |    1       |
| ``A`` is pressed.                                       |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| Connect the battery pack to the second micro:bit.       |     2      |
| Upload the same code the second micro:bit.              |            |
|                                                         |            |
+---------------------------------------------------------+------------+
| Test the pair of micro:bits. You should be able to      |            |
| send and receive messages.                              |     2      |
|                                                         |            |
+---------------------------------------------------------+------------+
| When a message is received, light up an LED for a       |     1      |
| second.                                                 |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| Keep the score on each device. Count the number of      |            |
| messages received.                                      |     1      |
|                                                         |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| If button ``B`` is pressed, display the score.          |     1      |
|                                                         |            |
+---------------------------------------------------------+------------+
