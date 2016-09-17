****************
Music
****************
This is a quick guide to some of the things you can do with Micro:bit music. The idea is that you can use this information to experiment and 
create something for yourselves.  You can use the Micro:bit to play simple tunes, provided that you connect a speaker to your board. 

.. By default the music module expects the speaker to be connected via pin 0. 
.. .. image:: pin0-gnd.png

If you are using headphones you can Connect your Micro:bit to some headphones like this: 

.. image:: connect_headphones.jpg


Basic Functions
================

Play a tune
-----------
Let's play some music::
	from microbit import *
	import music

    	music.play(music.NYAN)

 **Note:** You must import the ``music`` module to play and control sound.

MicroPython has quite a lot of built-in melodies. Here's some of them, try them out: 

 *  ``music.DADADADUM``
 *  ``music.ENTERTAINER``
 *  ``music.PRELUDE``
 *  ``music.ODE``
 *  ``music.NYAN``
 * ``music.RINGTONE``
 
 
Make your own tune
-------------------
Here is a snippet of code showing how to play a sound. The number after the 
note is the octave and the number after the colon says how long the note will
last::
	from microbit import *
	import music

	# Play a 'C'
	music.play(C)

	# Play a 'C' for 4 beats long
	music.play(C:4)

	# Play a 'C' in octave number 3 for 4 beats long
	music.play(C3:4)

Playing a series of notes one after the other is easy, you just put the notes you want to play in a list::

	from microbit import *
	import music

	# Tune: Frere Jacques
	tune = ["C4:4", "D4:4", "E4:4", "C4:4", "C4:4", "D4:4", "E4:4", "C4:4",
        	"E4:4", "F4:4", "G4:8", "E4:4", "F4:4", "G4:8"]
	music.play(tune)
	

Advanced Functions
===================
You can also specify the note you want to play as a ``frequency``. Take a look at this example where we make a police siren. The clever thing here is that the
frequency or note is controlled by a for loop::


	while True:
		for freq in range(880, 1760, 16):
		        music.pitch(freq, 6)
		for freq in range(1760, 880, -16):
			music.pitch(freq, 6)
	 

Ideas for Projects with Music 
==============================
* Make up your own tune.
* Make a theremin. Change the pitch of the sound based on the readings from the accelerometer.  
