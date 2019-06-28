*******************
Substitution Cipher
*******************
	
Description
===========

The substitution cipher is deceptively easy. Messages are encrypted using a key which is created in advance. 
You make the key by changing the alphabet:

.. figure:: assets/substitution.png

Your goal is to turn your micro:bit into a machine that can encode messages using a substitution cipher. We
call the message to be encrypted *plain text* and the encrypted message *cipher text*. You will need to store the alphabet with the substition cipher in your program. 
You can use a python dictionary to do this. A python dictionary for the substitution cipher above looks like this::

	key =  {'A':'V', 
			'B':'J', 
			'C':'Z', 
			'D':'B',
			  ...   }

Try this out, experiment using the REPL. 