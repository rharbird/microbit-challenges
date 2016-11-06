******
Radio
******
Your micro:bit has a radio chip that can be used to transmit and receive
messages.

.. image:: radio.jpg
   :scale: 80 %


Basic Functions
================

Getting ready - setting a group number
--------------------------------------
Before you can use the radio you must turn it on.  Once the radio is on it will hear the messages from any other micro:bit that is within range. If you 
only want share messages within a group of devices then each micro:bit in the group must be configured to share the same group identifier. The address must be a number between ``0`` and ``255``. You can do that like this::

	from microbit import *
	import radio		

	radio.on()			# Switch the radio on.
	radio.config(group=40)	# Set the group number to 40

Sending and receiving a message
-------------------------------
Now you are ready to send or receive a message. You can send a string which is 
up to 250 characters in length in the message. Here is an
example::

	my_message = "Be nice to yu turkeys dis christmas, Cos' turkeys just wanna hav fun, Turkeys are cool, turkeys are wicked, An every turkey has a Mum."

	radio.send(my_message)


Receiving a message is similar in nature, just use::

    message_received = radio.receive()

Putting it together
-------------------
Your micro:bit is smart, it can send and receive messages in quick succession. Just tell the micro:bit to keep checking for messages or sending them like this::

	from microbit import * 
	import radio

	radio.on()

	# Event loop.
	while True:
		radio.send('secret message') 
		incoming = radio.receive()
		if incoming is not None:
		    display.show(incoming)
		    print(incoming)
		sleep(500)

If you print the incoming message, you will see that sometimes it contains the value ``None``. That is because sometimes the micro:bit checks for a message but nothing has arrived. We can ignore these non-events by checking whether ``incoming`` equals ``None`` and ignoring it if that is the case.


Ideas for Projects with the Radio
=================================
* Send a message every time button ``A`` is pressed.
* You will need a pair of micro:bits. Program one micro:bit to receive messages and print the message received using the ``print()`` method. eave this micro:bit plugged into your computer with a USB cable. Program the other micro:bit to send accelerometer readings or the temperature readings in messages every second. Unplug this micro:bit and use a battery pack to power it. Congratulations! you have created a data logger!   
* How far can you place one micro:bit away from another before it can no longer receive messages? Can you find out how to change the signal strength with ``radio.config()``?
