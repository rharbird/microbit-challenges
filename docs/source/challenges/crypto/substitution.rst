*******************
Substitution Cipher
*******************

.. tabularcolumns:: |L|l|

+--------------------------------+----------------------+
| **Total points possible**	 | **Uses**	        |
+================================+======================+
| 10			 	 | LED display          |
+--------------------------------+----------------------+
	
Description
===========

The substitution cipher is deceptively easy. Messages are encrypted using a key which is created in advance. 
You make the key by jumbling up the alphabet like this:

.. figure:: substitution.png

Your goal is to turn your micro:bit into a machine that can encode messages using a substitution cipher. We
call the message to be encrypted *plain text* and the encrypted message *cipher text*. You will need to store the alphabet with the substition cipher in your program. You can use a python *dictionary* to do this. A python dictionary for the substitution cipher above looks like this::
	cipher_key = { 'A':'V', 'B':'J', 'C':'Z', 'D':'B', 'E':'G', 'F':'N', 'G':'F', 'H':'E', 'I':'P', 'J':'L', 'K':'I','L':'T','M':'M','N':'X','O':'D','P':'W','Q':'K','R':'Q','S':'U','T':'C','U':'R','V':'Y','W':'A','X':'H','Y':'S','Z':'O'}

In English, this means: the character 'A' should be substituted with the character 'V'; the character 'B' should be substituted with the character 'J' and so on. You can print a dictionary using ``print(cipher_key)``.
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
| corresponding cipher text. Print the dictionary using   |            |
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
| Use the dictionary you created to translate each        |     4      |
| character in the message to a corresponding             |            |
| encrypted character. Hint: ``cipher_key['A']`` will     |            |
| give you the cipher character corresponding to the      |            |
| letter 'A' in your dictionary.                          |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| Display the encrypted text on the micro:bit display and |      1     |
| print encrypted text in the REPL using the ``print()``  |            |
| function.   						  |            |
|                                                         |            |
+---------------------------------------------------------+------------+
