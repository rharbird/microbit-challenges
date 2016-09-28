**************
Send a Message
**************

.. tabularcolumns:: |L|l|

+--------------------------------+-----------------------------------------------------------------------+
| **Total points possible**	 | **Uses**	                                                         |
+================================+=======================================================================+
| 10			 	 | Two Micro:bits, Battery pack with 2 AAA batteries, Radio, LED Display |
+--------------------------------+-----------------------------------------------------------------------+
	
Description
===========
In this project, we will use the radio on the micro:bit to send messages from one microbit to another. You will
display the number of messages sent between a pair of micro:bits on the LED display.


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
| Add some code so that the message is sent when button   |    1       |
| a is pressed.                                           |            |
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
|                                                         |            |
| Now you should find a way to count the messages. You    |            |
| could add 1 to a counter every time you send a message, |     1      |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| You need to do something special to send and receive    |     2      |
| numbers - you need to translate the number to a string  |            |
| using the ``str()`` function before sending it in the   |            |
| message. At the receiving end you need to translate     |            |
| the string back into a number using the ``int()``       |            |
| function.                                               |            |
|                                                         |            |
+---------------------------------------------------------+------------+
