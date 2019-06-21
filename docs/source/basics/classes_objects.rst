********************
Classes and Objects
********************

.. figure:: assets/snake.png 
	 :align: center

Python is an object-oriented language - it's based on the concept of "objects" that contain some fields (variables) and methods (functions). It's procedures can modify
it's attributes (fields) - it has a "self" awareness.
To create an instance of an object, you first need to construct a "prototype", that will define what the object will look like and what's it capable of. The prototype
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

    player_1 = Player("teapot418")
    player_2 = Player("r00t")

    player_1.update_score(40)
    player_2.change_name("bott0m")        
                                                          

This example shows a prototype for a Player object. A player has a class attribute ``total_count``, that keep count of all the instances of objects of class Player. 
A class attribute is the same for any instance of class Player, and so you can find out the total count of players through any of them.
Other attributes are instance attributes name and score, which can be updated using class methods ``update_score()`` and ``change_name``.  
  
 It has position and direction attributes and methods that move the snake and show it on 
the LED display. Variables within a class are either class or instance variables. A class variable is the same for all instances of the class, 
 It is possible to define an ``__init__()`` method for your class, which can take in other arguments to specify an initial state of an object. In defining an
``__init__()`` method, a snake object has an initial position of 0, 0 and western direction. ::

class Snake:
        total_count = 0

        def __init__(self):
            self.x_position = 0
            self.y_position = 0
            self.direction = "w"
            self.__class__.total_count += 1

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