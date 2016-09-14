****************
Music
****************
This is a quick guide to some of the things you can do with Micro:bit music. The idea is that you can use this information to experiment and 
create something for yourselves.  You can use the Micro:bit to play simple tunes, provided that you connect a speaker to your board. 

By default the music module expects the speaker to be connected via pin 0. 

.. image:: pin0-gnd.jpg

Connect your Micro:bit to some headphones like this: 

.. image:: connect_headhphones.jpg


Basic Functions
================

Play a tune
-----------
Let's play some music::

    from microbit import *
    import music

    music.play(music.NYAN)

** Note: ** You must import the ``music`` module to play and control sound.

MicroPython has quite a lot of built-in melodies. Here's some of them, try them out:: 

* ``music.DADADADUM``
* ``music.ENTERTAINER``
* ``music.PRELUDE``
* ``music.ODE``
* ``music.NYAN``
* ``music.RINGTONE``


Make your own tune
-------------------
Playing a series of notes one after the other is easy, you just put the notes you want to play in a list::









	fromch note has a name (like ``C#`` or ``F``), an octave (telling MicroPython how
high or low the note should be played) and a duration (how
long it lasts through time). Octaves are indicated by a number ~ 0 is the
lowest octave, 4 contains middle C and 8 is about as high as you'll ever need
unless you're making music for dogs. Durations are also expressed as numbers.
The higher the value of the duration the longer it will last. Such
values are related to each other - for instance, a duration of ``4`` will last
twice as long as a duration ``2`` (and so on). If you use the note name ``R``
then MicroPython will play a rest (i.e. silence) for the specified duration.

Each note is expressed as a string of characters like this::

    NOTE[octave][:duration]

For example, ``"A1:4"`` refers to the note named ``A`` in octave number ``1``
to be played for a duration of ``4``.

Make a list of notes to create a melody (it's equivalent to creating an
animation with a list of images). For example, here's how to make MicroPython
play opening of "Frere Jaques"::

    import music

    tune = ["C4:4", "D4:4", "E4:4", "C4:4", "C4:4", "D4:4", "E4:4", "C4:4",
            "E4:4", "F4:4", "G4:8", "E4:4", "F4:4", "G4:8"]
    music.play(tune)

.. note::

    MicroPython helps you to simplify such melodies. It'll remember the octave
    and duration values until you next change them. As a result, the example
    above can be re-written as::

        import music

        tune = ["C4:4", "D", "E", "C", "C", "D", "E", "C", "E", "F", "G:8",
                "E:4", "F", "G:8"]
        music.play(tune)

    Notice how the octave and duration values only change when they have to.
    It's a lot less typing and simpler to read.
 microbit import *
	import music

	# Play some notes one at a time
	music.play('a') 
	music.play('b') i
	music.play('c')

	

Advanced Functions
================
Describe the more advanced functions if there are any.

Ideas for Projects with Music 
===================================
* List projects that students can make with the microbit. 
