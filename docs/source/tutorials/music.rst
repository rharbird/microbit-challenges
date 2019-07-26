********
Sound
********
Micro:bit can be used to play simple tunes, provided that you connect a speaker to your board. 

If you are using headphones you can use crocodile clips to connect your micro:bit to headphones: 

..  figure:: assets/headphones_connect.png
    :align: center	
    :scale: 70 %

.. warning:: You cannot control the volume of the sound level from the micro:bit. Please be very careful if you were using headphones. A speaker is a safer choice while 
	working with sound.

You can also connect your micro:bit to a speaker using crocodile clips: 

.. figure:: assets/connect_speaker.jpg
   :align: center

   Source: <https://www.kitronik.co.uk/blog/microbit-alarm-kitronik-university/>

Basic Functions
================

Play a tune
-----------
To play a tune you can use the ``play`` function: ::

	from microbit import *
	import music

	music.play(music.NYAN)

.. note:: You must import the ``music`` module to play and control sound.

The music module includes a number of built-in tunes. Here's some of them: 

 *  ``music.DADADADUM``
 *  ``music.ENTERTAINER``
 *  ``music.PRELUDE``
 *  ``music.ODE``
 *  ``music.NYAN``
 * ``music.RINGTONE``
 
 
Make your own tune
-------------------
To play a tune, specify the note (C,D,E,F,G,A,B; including sharps (eg.: C#)) to play. Optionally, it's possible to specify the octave (1-8) and the duration it will be played
for: ::
	
	from microbit import *
	import music

	# Play a 'C'
	music.play('C')

	# Play a 'C' for 4 beats long
	music.play('C:4')

	# Play a 'C' in octave number 3 for 4 beats long
	music.play('C3:4')

Playing a series of notes one after the other is easy, you just put the notes you want to play in a list::

	from microbit import *
	import music

	# Tune: Frere Jacques
	tune = ["C4:4", "D4:4", "E4:4", "C4:4", "C4:4", "D4:4", "E4:4", "C4:4",
        	"E4:4", "F4:4", "G4:8", "E4:4", "F4:4", "G4:8"]
	music.play(tune)
	
Micro:bit will remember the octave of the note defined previously. Hence, the tune above can be rewritten as follows: ::

	tune = ["C4:4", "D4:4", "E4:4", "C:4", "C:4", "D:4", "E:4", "C:4",
        	"E:4", "F4:4", "G4:8", "E:4", "F:4", "G:8"]


Advanced Functions
===================
You can also specify the note you want to play using its frequency using the ``pitch`` method. For example, to create a police siren effect ::

	while True:
		for freq in range(880, 1760, 16):
		        music.pitch(freq, 6)
		for freq in range(1760, 880, -16):
			music.pitch(freq, 6)
	 
Can you guess what this does? Each time around the loop a new frequency is calculated by adding (or subtracting) 16. 

Practice questions
===================
* Make up your own tune.
* Make a musical instrument. Change the pitch of the sound played based on the readings from the accelerometer.  
