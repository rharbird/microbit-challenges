*******************
Consonant or Vowel?
*******************
 
.. tabularcolumns:: |L|l|

+--------------------------------+----------------------+
| **Total points possible**      | **Uses**             |
+================================+======================+
| 10                             | LED display, buttons |
+--------------------------------+----------------------+

	
Description
===========

In this challenge you will make a reaction game called Consonant or Vowel.  The micro:bit must show the player  a letter which 
is either a consonant or a vowel. The player must press button ``A`` if it is a consonant and button ``B`` if it is a vowel. They
must choose an answer in 1 second.  If the player presses the wrong button, the micro:bit displays a suitable image or message and the game ends. 
If they press the correct button, the micro:bit displays a message or image and the player gets a point and can play again.


Basic Game
===========
Collect points for these stages: 

.. tabularcolumns:: |p{14cm}|R|

+---------------------------------------------------------+------------+
| **Tasks**                                               | **Points** |
+=========================================================+============+
| Display a welcome messge.                               |      1     |
+---------------------------------------------------------+------------+
| Create loop for the game which repeats every second.    |      1     |
|                                                         |            |
+---------------------------------------------------------+------------+
|                                                         |            |
| Create a list of consonants in your program and a list  |      1     |
| of vowels. Hint: ``vowels = ['A', 'E', 'I', 'O', 'U']`` |            |
|                                                         |            |
+---------------------------------------------------------+------------+
| Randomly select either consonants or vowels.            |            |
| Hint: use ``random.randint(0,1)``.                      |      1     |
| Randomly select a letter from the list.                 |            |
|                                                         |            |
| Display the letter.                                     |            |
|                                                         |            |
+---------------------------------------------------------+------------+
| Test whether the user has pressed the correct button.   |      1     |
| If the user has pressed the correct button, display     |            |
| a suitable image or message.                            |            |
+---------------------------------------------------------+------------+
| If the user has pressed the wrong                       |      2     |
| button, finish the game.                                |            |
+---------------------------------------------------------+------------+
| If the player's answer was correct, add 1 to the        |      1     |
| player's score.                                         |            |
+---------------------------------------------------------+------------+
| At the end of the game, display the player's score.     |      1     |
+---------------------------------------------------------+------------+


Extra points
============

.. tabularcolumns:: |p{14cm}|R|

+---------------------------------------------------------+--------+
| Tasks                                                   | Points |
+=========================================================+========+
| If the player succeeds, make the time interval for the  |      1 |
| next round shorter.                                     |        |
+---------------------------------------------------------+--------+

