********************
Classes and Objects
********************

.. figure:: assets/snake.png 
	 :align: center

Python is an object-oriented language - it's based on the concept of "objects" that contain some fields (variables) and methods (functions). It's procedures can modify
it's attributes (fields). Everything in Python is an object - whether it's an integer or a string. 

``Object`` is a handy concept to make a representation of something abstract - for example a useful way of storing data in an ordered manner. Reminds you of something?
Yes, a list. 
How would you describe a list object? What attributes does it have? When/How is it useful? 

.. tip:: Do you remember the ``dir(ClassName)`` command? It lists all the attributes and methods of a required class, such as ``dir(str)``. 

If you find you need an object that Python does not have, you can create your own. To create an instance of an object, you first need to construct a 
"prototype", that will define what the object will look like and what it's capable of. The prototype
is called a class::

    class Player():
        total_count = 0

        def __init__(self, name):
            self.name = name
            self.score = 0
            self.__class__.total_count += 1

        def update_score(self, score):
            self.score = score

        def change_name(self, name):
            self.name = name           
                                                          

This example shows a prototype for a Player object. A player has a class attribute ``total_count``, that keep count of all the instances of objects of class Player. 
A class attribute is the same for any instance of class Player, and so you can find out the total count of players through any of them.
Other attributes are instance attributes name and score, which can be updated using class methods ``update_score()`` and ``change_name``.  

It is possible to define an ``__init__()`` method for your class, which can take in other arguments and can specify an initial state of an object. In this way, when 
the object ``player_1`` below is instantiated, the player's initial score will be zero, the name will be as specified in the argument and ``total_count`` 
will increment by one.::

    player_1 = Player("teapot418")
    player_2 = Player("r00t")

    player_1.update_score(40)
    player_2.change_name("bott0m")

Now you might wonder, why does calling methods on ``player_1`` or ``player_2`` work with one argument only, while the method definitions have two arguments? 
Surely Python raises an error in this case. As you may have guessed, the instance object - ``player_1`` - is passed as the first argument, and is actually equivalent to 
saying ``Player.update_score(player_1, 40)``. 

.. note:: The keyword ``self``  has no special meaning in Python, it is just a convention. You should use it if only for the reason of making your code more 
readable to others or yourself when you come back to it after some time (you can read more on discussion of ``self`` in this blogpost_ by Guido van Rossum - the
father of Python).

.. _blogpost: http://neopythonic.blogspot.com/2008/10/why-explicit-self-has-to-stay.html


Accessing attributes is the same for all objects again: ``obj.name``. For example, to print the name of a Player object you write: ::

    print(player_1.name)

To create an attribute for a class, you don't have to declare it in the class definition - they are like local variables in that they spring into existence when they're 
assigned to. In this way, we can create a ``counter`` attribute for our ``player_1`` object. What does the following program output then? ::

    player_1.counter = 0

    while (player_1.counter < 10):
        player_1.counter += 1

    print(player_1.counter)    

There are many more nuances and useful characteristics of classes that we don't talk about in this tutorial. If you do want to learn more, look at Python documentation_.

.. _documentation: https://docs.python.org/3/tutorial/classes.html#a-word-about-names-and-objects


To give you another example of using classes, here is a Snake class that one could use for a snake game. 

class Snake:

        def __init__(self):
            self.x_position = 0
            self.y_position = 0
            self.direction = "w"

        def move_snake(self, x_position, y_position, direction):
            self.x_position = x_position
            self.y_position = y_position 
            self.direction = direction

        def show_snake(self):
            display.set_pixel(self.x_position, self.y_position, 9)
            sleep(600)
            display.set_pixel(self.x_position, self.y_position, 0)

    # Create an instance of a Snake object
    python = Snake()

    # Access its position on x axis and print
    print(python.x_position)

    # Move python to the right
    python.move_snake(python.x_position + 1, python.y_position)   
   

We can access object's attributes and call methods on it. What prints out to the console in this case?::

    python = Snake()
    mamba = Snake()

    mamba.x_position = 1
    python.x_position = 2

    Snake().x_position = 3

    print(mamba.x_position)
    print(python.x_position)

Another thing that might help you understand to concept of objects and classes, is to bear in mind that everything in Python is an object. Take a list, for instance