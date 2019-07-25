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

A letter from the head of department
=====================================

Dear all,
Welcome to Computer Science at UCL.
The journey you are about to undertake will have a profound effect on the rest of your life — your time as a university undergraduate is unique and memorable and it is 
our task to work with you to ensure that you get the most out of it. Our aim is to make your experience with us challenging, exciting and meaningful: giving you a strong
basis for the professional world or further study after you graduate. 
Computer Science at UCL is focussed on building well-rounded expertise. Ours is an applied course based on strong theoretical foundations — this means that you will 
build things, but you will know how and why they should be created as they are. Over your time at UCL, you will work with academic supervisors and real clients and so 
you will need to learn to communicate and work in teams effectively. But, above all, you will be challenged to become an independent learner, capable of managing your 
own study; given the rate of change in technology, this is a (perhaps the) key skill for life after university.
Your journey starts here. Enclosed in this pack is a BBC micro:bit. This is a small computer with attached sensors that was designed to help students learn to program. 
Some of you may have seen this already, many will not have done. Regardless, we’d like to challenge you to do two things before you arrive, and to show us what you have 
achieved in the first week of your time at UCL. The two things are:

1.	Work through some of the material you can find at:
    <http://microbit-challenges.readthedocs.io>
    and use the examples and project ideas to write some simple Python programs for the micro:bit.

2.	Surprise us. Do something creative with the micro:bit — we don’t mind what it is, but we want it to be your own work.

There are no marks for this. And you may need to find and explore resources on the web other than those we have provided. Some of you may struggle. The point here is 
that you start your journey as independent learners: most of the things in life worth having require an investment of time and effort, and a UCL education is worth 
having. We will ask you to share what you have done with us in the first week of term, so please do remember to bring your micro:bit with you.
Please note: we do not expect you to buy additional hardware to enhance your micro:bit and we do not expect you to spend every waking hour of the next month coding. We 
are looking for creativity and a willingness to learn, not volume of code or expensive rigs.
I hope your time with us will be exciting and challenging. And, since I will be there in your first week and will then teach one of your first courses, I very much look 
forward to meeting you.


.. figure:: assets/signature_transparent.png

    Steve Hailes
    Head of Department


Guide to the guide
===================

Sections in this tutorial will walk you through coding using micro:bit, basics of programming and micro:bit's features. You don't have to meticulously go through all the 
theory covered in Basics of programming, especially if you're a beginner. Start writing simple programs using the features of micro:bit or
the examples provided and read about further programming concepts as you go. Feel free to skip over the parts you are confident in and choose the parts that are relevant.

Topics covered here are generally only touched upon and many things are not explained on purpose. One of the important skills
you will need in the course and work later on will be finding resources and reading documentation on your own, and we encourage you to explore other resources than those
found here. 

As you learn more about programming, you'll naturally keep finding better and more efficient ways to do your 
projects of the past, but right now you should focus on getting yourself started.

If your skills are advanced, you might not find this documentation very interesting. However, micro:bit is a highly configurable device and you might like to explore 
micro:bit runtime_, which gives you more flexibility about what you can do.  

.. _runtime: https://lancaster-university.github.io/microbit-docs/

.. note:: If you feel confused while reading through tutorials or if you feel like you need more guidance to start programming, don't be discouraged! There is a lot of free online courses that are great at going through basics of programming with Python, like this one_. Try to go through a first few lessons, and everything will make more sense.

.. _one: https://www.edx.org/course/introduction-to-computer-science-and-programming-using-python-2 