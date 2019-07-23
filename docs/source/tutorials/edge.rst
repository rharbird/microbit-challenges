***************
Edge Connector
***************

To fully starts using micro:bit and its functions to interface with the world, you will need to learn about its edge connector. This can be used to connect to external
circuits and components. 
However, in order to use the edge connector, you will need extra equipment like crocodile clips/banana plugs or other external PCB connectors (1.27mm pitch).

.. _`touch sensing` : https://microbit-micropython.readthedocs.io/en/latest/tutorials/io.html

.. figure:: assets/edge_connector.svg
    :align: center

    Source: https://tech.microbit.org/hardware/edgeconnector/

There are 5 rings to connect with 4mm crocodile clips/banana plugs - 2 of them (3V, GND) are connected to the micro:bit power supply and the other three can be used for 
general purpose input/output using both analog and PWM (pulse width modulation) and `touch sensing`_. The smaller 1.27 mm strips allow you to either connect to different 
parts of micro:bit or which you can use for your own purposes.

You can find the description of each of the pins and what they can be used for at <https://microbit.pinout.xyz/>. Refer to the `developer
reference`_ for further information. 

_`developer reference`: https://tech.microbit.org/hardware/edgeconnector/