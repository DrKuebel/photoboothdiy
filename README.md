# Selfiebox DIY

Here you will find code for my SELFIEBOX made with a Raspberry pi under Raspbian.

It is based on this instrutable: https://www.instructables.com/id/Wedding-Event-Photobooth/

Requires for the code works:

1. Enable Camera module

To enable the camera module there is a little configuration to do: https://www.raspberrypi.org/documentation/usage/camera/

2. Prepare Raspbian with all librairies you need
(most of them are already installed with the raspbian image.)

* Install Python (because program is made with Python), you will find how to do here: https://www.raspberrypi.org/documentation/linux/software/python.md

* Install Pygame (library for python graphical interface), more information here: https://www.packtpub.com/mapt/book/hardware_and_creative/9781785285066/3/ch03lvl1sec19/installing-pygame

* Install Picamera (library for the camera module of Raspberry pi): https://www.raspberrypi.org/documentation/linux/software/python.md

* Install Python module RPI.GPIO (library for control Raspberry GPIO for the arcade button): https://learn.adafruit.com/playing-sounds-and-using-buttons-with-raspberry-pi/install-python-module-rpi-dot-gpio

* Install CUPS to add a printer on Raspbian, you will find how to do here: https://www.howtogeek.com/169679/how-to-add-a-printer-to-your-raspberry-pi-or-other-linux-computer/

* Install Python CUPS 
  sudo apt-get install python-cups

* Update Gutenprint to Version 5.3.1 to add some more printers.
But this is still a bit tricky..
Details here: https://sourceforge.net/projects/gimp-print/files/gutenprint-5.2/5.2.14/
https://www.raspberrypi.org/forums/viewtopic.php?t=219763

* Install PIL (library for images on Python): https://www.pkimber.net/howto/python/modules/pillow.html

To run it you just have to launch a terminal, navagate to the program folder and type "sudo python camera.py"

If you want to test it without a button wire on GPIO Pin 25 of the raspberry, you can push down arrow of your keyboard.

Finally, I wanted to run the program at startup of the raspberry pi so I followed this tuto https://www.simplified.guide/linux/automatically-run-program-on-startup

The script which launch at startup is on the Github: photobooth-script.sh 
