********
Theremin
********

.. tabularcolumns:: |L|l|

+--------------------------------+------------------------+
| **Total points possible**	 | **Uses**	          |
+================================+========================+
| 10			 	 | Accelerometer, speaker |
+--------------------------------+------------------------+
	
Description
===========
In this project, we will use the accelerometer to control the frequency of a tone.  

The theremin is a weird and wonderful electronic instrument that requires no physical contact. Have a listen to a program about them at: `<http://www.bbc.co.uk/programmes/b0076nqv>`_.
The theremin was invented in 1920 by Léon Theremin, an early Russian electronic engineer. It is played by moving one’s hands near two antennas – the first controls the volume of the output and the second the pitch.
For those that are musical it is worth knowing that the Theremin inspired Robert Moog to invent the synthesiser, so, although it’s a little-used instrument, it has had a powerful effect on the history of music.

.. figure::  leon_theremin.jpg

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

                                                                     
Basic Task
===========
Collect points for these stages: 

.. tabularcolumns:: |p{14cm}|R|

+---------------------------------------------------------+------------+
| **Tasks** 		                                  | **Points** |
+=========================================================+============+
| We are going to use the accelerometer values in the x   | 	 1     |
| axis. Write some code to print accelerometer values     |            |
| for the x axis.                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| Write down (on paper) the x axis values for the 	  |      1     |
| accelerometer when you tilt the board left, when you    |            |
| tilt the board                                          |            |
| to the right and when the board is held flat, face-up.  |            |
| We need to know the minimum and maximum values for the  |            |
| range.                                                  |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| Collect 30 accelerometer readings in a list.            |     2      |
| Have a look at the notes above for some information     |            |
| about this. Print the list to the REPL.                 |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| Now let's try making some sound. Connect the speaker to |      1     |
| the micro:bit using  some crocodile clips. 		  |            |
| Import the music library ``import music`` and play      |            |
| some sounds using ``music.pitch(frequency, time)``      |            |
| where frequency is between 50 and 4000 Hz and time is   |            |
| a value in milliseconds.                                |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| You need to translate the value of the accelerometer    |      1     |
| reading into a sound frequency value. Can you think of  |            |
| a way to do this?                                       |            |
| Experiment with your program, print values to the REPL. |            |
|                                                         |            |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| Play a frequency that corresponds to the accelerometer  |     1      |
| value.                                                  |            |
|                                                         |            |
+---------------------------------------------------------+------------+
| You will find that the sound wavers because the         |            |
| accelerometer values vary quickly. One way to address   |            |
| this is to calculate the average value and play a .     |            |
| frequency that corresponds to that.                     |            |
|                                                         |     2      |
| Calculate the average accerometer value and print it.   |            |
| Hint: There are two python functions that can help us   |            | 
| with that: ``sum(readings) / len(readings)``            |            | 
| ``sum`` adds up all the elements of a list and ``len``  |	       | 
| returns the length of a list so we have the total value |	       |
| of all the accelrometer readings divided by the number  |            |
| of readings.                                            |            |  
+---------------------------------------------------------+------------+
