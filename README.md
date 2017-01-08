# stairlight
code to allow ledstrips to fade in and out on movement on the stairs
## Setup

1. attach ledtrips to stair steps
2. conenct ledstrips to raspberry pi using breadboard, resistors, TIP120, jumpercables (or soldering) 
3. connect the HC-SR05 PiR sensors to the raspberry pi
4. adjust gpio ports and prefered colors in variables.py
5. install scripts
6. add check.sh to crontab
7. walk down the stairs  

### Software Requirements:
. python 2.7
. pigpiod pigs (http://abyz.co.uk/rpi/pigpio/pigs.html)
. a lot of thigs i probably forgot

### Hardware Requirements:

. Stairs
. 5050 RGBWW Led Strip
. Cables
. Raspberry pi
. Breadboard
. 2x HC-SR05 PIR sensor
. 1-4 TIP120 Transistor
. 4x CA9685-16-Channel-12-bit-PWM
. some resistors
. more cables

### Wiring
To be added later

### Explanation

the trap.py script uses the HC-SR05 sensors to detect motion on the bottom and top stair steps. when motion is detected, the light will fade in from the corresponding direction. after reaching the other side of the stairs, the light will fade out in the same direction giving a smooth experience.

the check.sh script is added to crontab to check if the script is still running, and restart all if needed.

### to be added

individual color for every stair step
