******
Radio
******
High level description of the sensor and picture if necessary, for example:

.. image:: compass.jpg


Basic Functions
================

Getting ready - setting an address
----------------------------------
Before you can use the radio you must turn it on.  Once the radio is on it will hear the messages from any other micro:bit that is within range. If you 
only want share messages within a group of devices then each microbit in the group must be configured to share the same ``address``. The address must be a number between ``0`` and ``255``. You can do that like this::

	from microbit import *
	import radio		

	radio.on()			# Switch the radio on.
	radio.config(address=40)	# Set the group address to 40

Sending and receiving a message
------------------
Now you are ready to send or receive a message. You can send a string which is 
up to 250 characters in length (that's 251 bytes) in the message. Here is an
example::

	my_message = "Be nice to yu turkeys dis christmas, Cos' turkeys just wanna hav fun, Turkeys are cool, turkeys are wicked, An every turkey has a Mum."

	radio.send(my_message)


Receiving a message is similar in nature, just use::
	message_received = radio.receive()

Putting it together
-------------------
Your microbit is very clever, it can send and receive messages in quick succession. Just tell the microbit to keep checking for messages or sending them like this::

	from microbit import * 
	import radio

	radio.on()

	# Event loop.
	while True:
		radio.send('secret message') 
		incoming = radio.receive()
		display.show(incoming)
		sleep(500)


Ideas for Projects with the Radio
=================================
* Send a message every time button `A` is pressed.
* You will need a pair of microbits. Program one microbit to receive messages and print the message received using the `print()` method. eave this microbit plugged into your computer with a USB cable. Program the other microbit to send accelerometer readings or the temperature readings in messages every second. Unplug this microbit and use a battery pack to power it. Congratulations! you have created a data logger!   
* How far can you place one microbit away from another before it can no longer receive messages? Can you find out how to change the signal strength with ``radio.config()``?
