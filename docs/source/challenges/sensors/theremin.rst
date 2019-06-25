********
Theremin
********

Description
===========
In this project, we will use the accelerometer to control the frequency of a tone.  

The theremin is a weird and wonderful electronic instrument that requires no physical contact. Have a listen to a program about them at: `<http://www.bbc.co.uk/programmes/b0076nqv>`_.
The theremin was invented in 1920 by Léon Theremin, an early Russian electronic engineer. It is played by moving one’s hands near two antennas – the first controls the volume of the output and the second the pitch.
For those that are musical it is worth knowing that the Theremin inspired Robert Moog to invent the synthesiser, so, although it’s a little-used instrument, it has had a powerful effect on the history of music.

.. figure::  assets/leon_theremin.jpg

   Image: Leon Theremin, source: Wikipedia


Aside: a quick look at lists
----------------------------

As part of this task, you will have to collect and store some values from the accelerometer in a list and to calculate the average. Here is some information about how to do that. 
A list is a data structure used in just about all programming languages. In our case, it’s a numbered collection
of accelerometer values. In essence it’s a set of boxes into which we can put values – each box has a number, starting at 0
and going up.
Say we needed to keep the last 30 values of the accelerometer, then we create a list and add accelerometer value to it
every time that we go around the loop like this:: 
        
        while True:

            x_acceleration = accelerometer.get_x()

            # Add to the list of readings
            readings.append(x_acceleration)
        
            # If readings contains more than 30 values then pop the first value from the beginning
            if len(readings) > 30:
                readings.pop(0)
            sleep(1)
        
As you can see, if the array has more than 30 entries in it we will just delete the first entry, element number 0::

        readings.pop(0)