***************************
Theremin with Accelerometer
***************************

======   ======   ======================================
Level    Points   Uses
======   ======   ======================================
Medium	 2	  Accelerometer
======   ======   ======================================

The theremin is a weird and wonderful electronic instrument that requires no physical contact. Have a listen to a program about them at: `<http://www.bbc.co.uk/programmes/b0076nqv>`_.
The theremin was invented in 1920 by Léon Theremin, an early Russian electronic engineer. It is played by moving one’s hands near two antennas – the first controls the volume of the output and the second the pitch. 
For those that are musical it is worth knowing that the Theremin inspired Robert Moog to invent the synthesiser, so, although it’s a little-used instrument, it has had a powerful effect on the history of music.
`
.. image::  leon_theremin.jpg


You will need
=============

 * Micro:bit
 * USB cable
 * 2 Crocodile clip cables
 * a pair of headphones or a speaker

Make a theremin
===============

In this project, we will use the accelerometer to control the frequency of a tone.  The project itself falls into two parts: making a tone at a given frequency and controlling that frequency using the accelerometer.

Find the range of accelerometer values 
--------------------------------------
The first thing you need to do is to document the range of accelerometer values. We are going to use the x axis. 
Write the maximum and minimum values in the boxes below:

======  =============   ======================================
Axis	Minimum Value	Maximum Value 
======  =============   ======================================
X							
======  =============   ======================================

Here are the maximum and minimum values for the audible frequency of sound:

=========  =============   ======================================
	   Minimum Value   Maximum Value 
=========  =============   ======================================
Frequency  500		   4000
=========  =============   ======================================


See if you can work out how a way of calculating the output frequency for a given value of accelerometer input.
Try it – print the original and scaled values in the REPL using ``print``.

We now need to connect the micro:bit to the speaker.
Use the rescaled value you’ve just generated to set the tone on the speaker. How does it sound?
Awful, in all probability. 

Connect the speaker
-------------------
We now need to connect the accelerometer to the speaker.
Use the rescaled value you’ve just generated to set the tone on the speaker. How does it sound?
Awful, in all probability. 

The problem with the tone that never seems to stand still comes from the fact that the accelerometer value doesn’t stand still – it is noisy so we need to filter the value – to smooth it out over time.
To do that, we might make use of some maths. We could read the sensor and make an average out of the last n readings, where n is a number you choose. This is called a simple moving average and, mathematically, it’s represented by the formula:

.. math::  out_i = (in_i + in_(i-1) +in_(i-2) + in_(i-3)+...+ in_(i-n+1))/n

Try to implement this. To do so, you’ll need to know what a list is.


Aside: a quick look at lists
----------------------------

A list, or array, is a data structure used in just about all programming languages. In our case, it’s a numbered collection 
of accelerometer values. In essence it’s a set of boxes into which we can put values – each box has a number, starting at 0 
and going up.
Say we needed to keep the last 30 values of the accelerometer, then we create an array and add accelerometer value to it
every time that we go around the loop like this:: 
	
	while True:

	    x_acceleration = accelerometer.get_x()

	    #  translate the acceleration to a point in the frequency range.
	    #  I have written a function to do this called "translate"
	    frequency = translate(x_acceleration, 1000, -1000, 4000, 500)
	    
	    # Add to the list of readings
	    readings.append(frequency)
	
	    # If readings contains more than 30 values then pop the first value from the beginning
	    if len(readings) > 30:
	        readings.pop(0)
	    sleep(1)
	
As you can see, if the array has more than 30 entries in it we will just delete the first entry, element number 0::

	readings.pop(0)

Give this a go....

Back again
----------

All that remains now is to calculate the average of all the values we've recorded in the list. Luckily, there are
two python functions that can help us with that::

	sum(readings) / len(readings) 

``sum`` adds up all the elements of a list and ``len`` returns the length of a list so we have the total value of 
all the accelrometer readings divided by the number of readings.

Try this out and play the resulting value you get.
