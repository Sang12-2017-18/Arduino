The port I use: /dev/ttyACM0

I set up my breadboard with the help of this link:
       https://www.makerspaces.com/simple-arduino-projects-beginners/
       
I connected the port to my laptop. While uploading the blink sketch, I get this error:
      
      avrdude: ser_open(): can't open device "/dev/ttyACM0": Permission denied
       An error occured while uploading the sketch

If I type the command: sudo chmod 666 /dev/ttyACM0 on terminal
and then try uploading,it gives the message "Done Uploading".

Now the LED Blinks at a slower rate.(Right output obtained).
My first Arduino experiment works!

Problem 1:
I have to now find a way to permanently allot R/W privileges to the arduino usb cable.

Solution:
I added myself to dialout group, and it works! 
