**********************
Caesar Cipher - Part I
**********************

.. tabularcolumns:: |L|l|

+--------------------------------+----------------------+
| **Total points possible**	 | **Uses**	        |
+================================+======================+
| 10			 	 | LED display, buttons |
+--------------------------------+----------------------+
	
Description
===========

Humans have been interested in hiding messages for as long as they have been able to communicate by writing things
down. One of the earliest ciphers is known as the Caesar cipher, named after Julius Caesar, and was used by the 
Roman emporer to communicate with troops on the battlefield. Using the Caesar cipher you encrypt all the letters in a message by shifting the alphabet a number of places. The figure below shows how to encrypt a message with a shift of 3 letters:

.. figure:: shift.png

Your goal is to turn your micro:bit into a machine that can **encode** messages using the Caesar cipher. We
call the message to be encrypted *plain text* and the encrypted message *cipher text*. 

There is a trick you can use to encrypt, or shift the message. The trick relies on the fact that your
micro:bit sees the letters of the alphabet as numbers. You can translate a letter to a number, and back again using the python functions ``ord()`` and ``chr()``.                 
                                                                     
Let's say you want to shift each character by 4 places.  Try using this code to turn the character into a 
number and  add 4::

	ascii_char = ord(plaintext_char) + 4      	               
                                                                     
In English this means: translate ``plaintext_char`` into a number using the ``ord()`` function and add 4, the number of characters we want to shift. 

But hold on, there is one more thing that we need to do. If you look at the picture above, you will see that we need to wrap around going from Z back to A. To do this we need to subtract 26 (the number of letters in the alphabet) if we have gone past the letter 'Z'::

        ascii_char = ord(plaintext_char) + 4                       
	if ascii_char > ord('Z') 
		ascii_char = ascii_char - 26
	encrypted_char = chr(ascii_char) 

Try this out, experiment using the REPL. 

                                                                     
Basic Challenge
===============
Collect points for these stages: 

.. tabularcolumns:: |p{14cm}|R|

+---------------------------------------------------------+------------+
| **Tasks** 		                                  | **Points** |
+=========================================================+============+
| Display a welcome messge.                               | 	 1     |
+---------------------------------------------------------+------------+
|                                                         |            |
| You need to find out from the player how many places    |      2     |
| to shift the message. One way to do this is             |            |
| to shift the message by the number of button presses    |            |
| the user makes. Keep a count of how many times          |            |
| button ``A`` is pressed. The player can press button    |            |
| ``B`` to indicate they have finished.                   |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| In your program you should store the    		  |      1     |
| message you want to translate in a string like this:	  |            |
| ``message = 'KEEP THIS A SECRET```.                     |            |
|                                                         |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| Now display the message a character at a time using a   |      1     |
| ``for`` loop. Hint: to get each character in the message|            |
| use ``for c in message:``. 				  |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| Use the ``ord()`` function to translate each character  |     1      |
| into an numeric value and add the number of characters  |            |
| you want to shift.                                      |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| Make sure you have wrapped the result around.           |     1      |
| Hint: Check whether the shifted value is greater than   |            |
| the numeric value for ``Z``.                            |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
|                                                         |            |
| Use ``chr()`` to translate each number            	  |      2     |
| back into a character 				  |            |
| Hint: Don't encrypt the spaces.                         |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| Display the encrypted text on the micro:bit and print   |      1     |
| encrypted text in the REPL using the ``print()`` 	  |            |
| function.   						  |            |
|                                                         |            |
+---------------------------------------------------------+------------+
