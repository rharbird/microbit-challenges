***********
LED Display
***********

This is a quick guide to some of the things you can do with the LED display. The idea is that you can use this information to experiment and create something for yourselves. Try stuff out – see what happens and see what you can make.
There are 25 LEDs  set out like the picture below. The LEDs are numbered from (0,0) in the  top left hand corner, to (4,4) in the bottom right hand corner. You can use the LEDs like a very tiny screen to display  single characters, a string of characters or  a small picture like the smiley face here.  The LEDs can be set to different brightnesses.  Let's find out how to use them.


.. image:: happy.png
   :scale: 40 %


Basic Functions
===============

Display a string or an image
----------------------------

You can display characters on the LED display very easily like this::

    from microbit import *

    display.show("Hello")

The characters you display must be within a pair of quotes, either " " or ' '. 
 
MicroPython comes with lots of built-in pictures to show on the display.
For example, to make the device appear happy you type::

    from microbit import *

    display.show(Image.HAPPY)


Here's some of the the other images you can use:

    * ``Image.HEART``, ``Image.HEART_SMALL`` 
    * ``Image.HAPPY``, ``Image.SMILE``, ``Image.SAD``, ``Image.CONFUSED``, ``Image.ANGRY``, ``Image.ASLEEP``, ``Image.SURPRISED``, ``Image.SILLY``, ``Image.FABULOUS``, ``Image.MEH``, ``Image.YES``, ``Image.NO``
    * ``Image.ARROW_N``, ``Image.ARROW_NE``, ``Image.ARROW_E``, ``Image.ARROW_SE``, ``Image.ARROW_S``, ``Image.ARROW_SW``, ``Image.ARROW_W``, ``Image.ARROW_NW``
    * ``Image.MUSIC_CROTCHET``, ``Image.MUSIC_QUAVER``, ``Image.MUSIC_QUAVERS``
    * ``Image.XMAS``, ``Image.PACMAN``, ``Image.TARGET``, ``Image.ROLLERSKATE``, ``Image.STICKFIGURE``, ``Image.GHOST``, ``Image.SWORD``, ``Image.UMBRELLA``
    * ``Image.RABBIT``, ``Image.COW``, ``Image.DUCK``, ``Image.HOUSE``, ``Image.TORTOISE``, ``Image.BUTTERFLY``, ``Image.GIRAFFE``, ``Image.SNAKE``


Scroll a string 
---------------
To continuously scroll a string across the display you can use::

    from microbit import *

    display.scroll("Hello!")


Clear the display
-----------------
If you want to clear the LED display, you can do so like this::

    from microbit import *

    display.clear()


Advanced Functions
==================

Set a pixel
-----------
You can set a pixel in the LED display using the ``set_pixel`` method::

    from microbit import *

    display.set_pixel(0,4,9)

This sets the LED at column ``0`` and row ``4`` to a brightness of ``9``. The brightness value can be any whole number
between 0 and 9 with 0 switching the LED off and 9 being the brightest setting. You could use a ``for loop`` 
to set all the LEDs one at a time::

    from microbit import *

    display.clear()
    for x in range(0, 5):
    	for y in range(0, 5):
    	    display.set_pixel(x,y,9)  

The ``for loop`` lets you execute a loop a specific number of times using a counter. The outer loop::

	for x in range(0,5)

will execute the loop five times substituting ``x`` consecutive values in the range ``0`` to ``4`` for ``x`` each time. The loop will stop before it reaches the final value in the range.

The inner loop::

	for y in range(0,5):

will execute the loop five times substituting ``y`` consecutive values in the range ``0`` to ``4`` for ``y`` each time. The loop will stop before it reaches the final value in the range.

DIY images
----------
Of course, you want to make your own image to display on the micro:bit, right?

That's easy.  Each LED pixel on the physical display can be set to one of ten values. If a
pixel is set to ``0`` (zero) then it's off. It literally has zero brightness.
However, if it is set to ``9`` then it is at its brightest level. The values
``1`` to ``8`` represent the brightness levels between off (``0``) and full on
(``9``).

Armed with this information, it's possible to create a new image like this::

    from microbit import *

    boat = Image("05050:"
                 "05050:"
                 "05050:"
                 "99999:"
                 "09990")

    display.show(boat)

In fact, you don't need to write this over several lines. If you think you can
keep track of each line, you can rewrite it like this::

    boat = Image("05050:05050:05050:99999:09990")

(When run, the device should display an old-fashioned "Blue Peter" sailing ship
with the masts dimmer than the boat's hull.)

Have you figured out how to draw a picture? Have you noticed that each line of
the physical display is represented by a line of numbers ending in ``:`` and
enclosed between ``"`` double quotes? Each number specifies a brightness.
There are five lines of five numbers so it's possible to specify the individual
brightness for each of the five pixels on each of the five lines on the
physical display. 


Animation
---------
Static images are fun, but it's even more fun to make them move. This is also
amazingly simple to do with MicroPython ~ just use a list of images!

Luckily we have a
couple of lists of images already built in. They're called ``Image.ALL_CLOCKS``
and ``Image.ALL_ARROWS``::

    from microbit import *

    display.show(Image.ALL_CLOCKS, loop=True, delay=100)

We tell MicroPython to use ``Image.ALL_CLOCKS`` and
it understands that it needs to show each image in the list, one after the
other. We also tell MicroPython to keep looping over the list of images (so
the animation lasts forever) by saying ``loop=True``. Furthermore, we tell it
that we want the delay between each image to be only 100 milliseconds (a tenth
of a second) with the argument ``delay=100``.

Now, here's how to create your own animation.  First you need to create a list.
Here is a list of boats::

    all_boats = [boat1, boat2, boat3, boat4, boat5, boat6]

You can store anything in a list with Python, even images. 
In my example I'm going to
make my boat sink into the bottom of the display. To do that, 
I'm going to create 6 images and put them into a list called ``all_boats``::

    from microbit import *

    boat1 = Image("05050:"
                  "05050:"
                  "05050:"
                  "99999:"
                  "09990")

    boat2 = Image("00000:"
                  "05050:"
                  "05050:"
                  "05050:"
                  "99999")

    boat3 = Image("00000:"
                  "00000:"
                  "05050:"
                  "05050:"
                  "05050")

    boat4 = Image("00000:"
                  "00000:"
                  "00000:"
                  "05050:"
                  "05050")

    boat5 = Image("00000:"
                  "00000:"
                  "00000:"
                  "00000:"
                  "05050")

    boat6 = Image("00000:"
                  "00000:"
                  "00000:"
                  "00000:"
                  "00000")

    all_boats = [boat1, boat2, boat3, boat4, boat5, boat6]
    display.show(all_boats, delay=200)

Finally, we can tell MicroPython to animate a list of images using ``display.show``. 

Projects with LED Display
==========================
* Try out some of the built-in images to see what they look like. 
* Animate the ``Image.ALL_ARROWS`` list. How do you avoid looping forever (hint: the opposite of ``True`` is ``False``). Can you change the speed of the animation?
* Make your own image. Next try to make it fade out and then fade in again?
* Make a sprite, use a single LED on the display. Can you make it jump when you press a button?
