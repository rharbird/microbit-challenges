**********
Morse Code
**********

.. tabularcolumns:: |L|l|

+--------------------------------+----------------------+
| **Total points possible**	 | **Uses**	        |
+================================+======================+
| 10			 	 | LED display, speaker |
+--------------------------------+----------------------+
	
Description
===========

Morse code was invented in 1836 by a group of people including the American artist Samuel F. B. Morse. Using Morse code  a message is  represented as a series of electrical pulses which can be sent along wires to an electromagnet at the receiving end of the system.  The symbols used for each letter are shown in the figure below. 

.. figure:: morse.png
   :scale: 60 %

Source: raspberrypi.org

Of course, you aren't limited to electrical pulses, you can transmit a Morse code message using light or even sound.  A Morse code message sent over electrical wires is known as a telegram, a message is 
translated to Morse code by an operator at the sending end using a a telegraph key like the one pictured here.

.. figure:: J38TelegraphKey.jpg 
   :scale: 60 %

Telegraph key, source: Wikipedia 

The message is converted back to normal text by another operator at the receiving end. 

Your goal is to turn your micro:bit into a machine that can encode messages using Morse code. We will call the message to be converted *plain text*.  You will need to store the alphabet with the morse code in your program. You can use a python *dictionary* to do this. Here is part of a python dictionary for morse code::

    morse_code = { 'A':'.-', 'B':'-...', 'C':'---.', 'D':'-..', 'E':'.', 'F':'..-.', 'G':'..-.', 'H':'--.', ...  }

In English, this means: the character 'A' should be substituted with the string '.-'; the character 'B' should be substituted with the string '-...' and so on. You can print a dictionary using::

    print(morse_code)

Try this out, experiment using the REPL. 

                                                                     
Basic Task
===========
Collect points for these stages: 

.. tabularcolumns:: |p{14cm}|R|

+---------------------------------------------------------+------------+
| **Tasks** 		                                  | **Points** |
+=========================================================+============+
| Display a welcome message.                              | 	 1     |
+---------------------------------------------------------+------------+
|                                                         |            |
| Create a dictionary containing the alphabet and the     |      2     |
| corresponding morse code. Print the dictionary using    |            |
| the REPL.                                               |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| In this version of your program you should store the    |      1     |
| message to encode in a string like this: 		  |            |
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
| Use the dictionary you created to translate each        |     3      |
| character in the message to a corresponding             |            |
| encrypted character. Hint: ``morse_code['A']`` will     |            |
| give you the morse code symbol corresponding to the     |            |
| letter 'A' in your dictionary.                          |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| Display the morse code on the micro:bit display and     |      1     |
| print the code in the REPL using the ``print()``        |            |
| function.   						  |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| Connect a speaker to the micro:bit and play a series of |            |
| of beeps to represent the morse code message.           |     1      |
|                                                         |            |
|                                                         |            |
+---------------------------------------------------------+------------+
