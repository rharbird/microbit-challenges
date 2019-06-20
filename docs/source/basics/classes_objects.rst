********************
Classes and Objects
********************

Python is an object-oriented language - it's based on the concept of "objects" that contain some fields (variables) and methods (functions). It's procedures can modify
it's attributes (fields) - it has a "self" awareness.
To create an instance of an object, you first need to construct a "prototype", that will define what the object will look like and what's it capable of. The prototype
is called a class::

    class Snake:
        x_position = 0
        y_position = 0
        direction = "w"

        def move_snake(self, x_position, y_position):
            self.x_position = x_position
            self.y_position = y_position 

        def show_snake(self):
            display.set_pixel(self.x_position, self.y_position, 9)
            sleep(600)
            display.set_pixel(self.x_position, self.y_position, 0)

This example shows a class for a snake object we could use for a simple game. It has position and direction attributes and methods that move the snake and show it on 
the LED display.::

    # Create an instance of a Snake object
    python = Snake()

    # Print position on x axis
    print(python.x_position)

    # Move python to the right
    python.move_snake(python.x_position + 1, python.y_position)

We can access object's attributes and call methods on it.    
