****************************
Micro:bit - Getting Started 
****************************

The BBC micro:bit is a programmable micro-computer - microcontroller - that can be used to create all kinds of projects from robots to musical instruments – 
the possibilities are endless. Let's take a look at the features that you can use in your designs:

 * 25 red LED lights that can flash messages.
 * Two programmable buttons (A and B) that can be used to tell the micro:bit when to start and stop things.
 * A thermistor to measure the temperature.
 * A light sensor to measure the change in light.
 * An accelerometer to detect motion.
 * A magnetometer to tell you which direction you’re heading in.
 * A radio and a Bluetooth Low Energy connection to interact with other devices.

.. figure:: assets/microbit-hardware-access.jpg
   :scale: 35%
   :align: center
   
   Source: https://microbit.org/guide/features/

You can program micro:bit using several languages: MicroPython, C++ or JavaScript. This tutorial will focus on programming micro:bit using
MicroPython, but if you already are familiar with Python, or you're looking for extra challenge, look at the section for :ref:`Programming Micro:bit Using Other laguages`. 
C/C++ might be useful in particular, as it's the main language used to program embedded devices.

.. _languages: https://microbit.org/code/

MicroPython is a version of Python_ , that's designed to run on microcontrollers like micro:bit. Since their functionality is virtually the same (look here_ for difference 
in behaviour), we refer to the language used as Python in these tutorials. Programming in Python consists of
writing a series of steps to be executed (it's an *imperative* language), as you will see later when writing your first program.  

.. _Python: https://www.python.org/
.. _here: https://docs.micropython.org/en/latest/genrst/index.html
.. figure:: assets/programming.jpg
   :align: center 
   :scale: 30 %

   Source: HOMEWORK

Guide to the guide
===================

Sections in this tutorial will walk you through coding using micro:bit, basics of programming and micro:bit's features. You don't have to meticulously go through all the 
theory covered in Basics of programming, especially if you're a beginner. Start writing simple programs using the micro:bit and read about further programming concepts 
as you go. Feel free to skip the parts you are confident in and choose the parts that are relevant.

Topics covered here are generally only touched upon and many things are not explained on purpose. Some of the important skills
you will need during the course of your studies and work later on will be independent exploration of materials and capability to read official documentation, hence we 
encourage you to explore other resources than those found here.  

As you learn more about programming, you'll naturally keep finding better and more efficient ways to do your 
projects of the past, but right now you should focus on getting yourself started.

If your skills are intermediate/advanced, you might not find this documentation very interesting. However, micro:bit is a highly configurable device and you might like 
to explore micro:bit runtime_, which gives you more flexibility with what it can be used for.  

.. _runtime: https://lancaster-university.github.io/microbit-docs/

.. note:: If you feel confused while reading through tutorials or if you feel like you need more guidance to start programming, don't be discouraged! There is a number of 
    free online courses that are great at going through basics of programming with Python, like this one_. Try to go through a first few lessons, and everything should 
    make more sense.

.. _one: https://www.edx.org/course/introduction-to-computer-science-and-programming-using-python-2 