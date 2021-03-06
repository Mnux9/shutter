# Shutter
Camera shutter controlled by raspberry pi.

## Description
My old camera doesn't have any intervalometer function so i made this dogy script to controll the shutter with a raspberry pi's GPIO pins 

## Script
replace [GPIO] with the number of your GPIO
```
echo "---------AUTO SHUTTER---------"
echo "PRESS: CTRL + C TO STOP"
raspi-gpio set [GPIO] dh 
raspi-gpio set [GPIO] dl 
```
## Run
1) ssh into the raspberry pi
2) create shutter.sh and paste the code into it
3) allow execution of the scrip ```chmod +x shutter.sh```
4) set your GPIO as output (this needs to be done after every restart) ```raspi-gpio set [GPIO] op```
5) test ```./shutter.sh```
6) run it on repeat (replace [DELAY]...) ```watch -n [DELAY] script.sh```
7) press ctrl + c to stop it

## Wiring
The wiring is very simple:

1) Just take the camera apart (don't get zaped by the flash capacitor like I did) and tap into shutter button pins. This will be differend on other cameras.

![shutter tap](https://github.com/Mnux9/shutter/blob/main/images/shutter-tap.jpg)

2) Connect the the thing to raspberry pi. Pin 32 and pin 34 as the ground in my case. This can be chanaged [GPIO].

![connecting to raspberry](https://github.com/Mnux9/shutter/blob/main/images/raspi-connect.jpg)
