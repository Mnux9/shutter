# Shutter
Camera shutter controlled by raspberry pi.

## Description
My old camera doesn't have any intervalometer function so i made this dogy script to controll the shutter with a raspberry pi's GPIO pins 

## Script
```
echo "---------AUTO SHUTTER---------"
echo "PRESS: CTRL + C TO STOP"
raspi-gpio set [GPIO] dh #replace the [GPIO] with the number of your GPIO
raspi-gpio set [GPIO] dl #replace the [GPIO] with the number of your GPIO
```

## Wiring
The wiring is very simple:

Just take the camera apart (dont get zaped by the flash capacitor like I did) and tap into shutter button pins. This will be differend on other cameras.

![shutter tap](https://github.com/Mnux9/shutter/blob/main/images/shutter-tap.jpg)

Connect the the thing to raspberry pi. Pin 32 and pin 34 as the ground in my case.

![connecting to raspberry](https://github.com/Mnux9/shutter/blob/main/images/raspi-connect.jpg)
