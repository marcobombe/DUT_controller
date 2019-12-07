DUT controller
===============

commands:
- dut_on
- dut_off
- dut_reset

aliases (.bashrc):
- alias dut_off='/usr/bin/python2  ~/workspace/DUT_controller/dut_off.py'
- alias dut_on='/usr/bin/python2  ~/workspace/DUT_controller/dut_on.py'
- alias dut_reset='/usr/bin/python2  ~/workspace/DUT_controller/dut_reset.py'

connections:

Relais:
GND = PIN 6
VCC = PIN 2
CTRL= PIN 40

Display (I2C Mode):
GND = PIN 14 
VCC = PIN 1
DO (SCL) = PIN 5 
D1 (SDA) = PIN 3
RES (GND) = 100nF to GND and 10kOhm to VCC, and to PIN 38 for clear power on reset
DC (GND) = PIN 9
CS (GND) = PIN 39

To set I2C mode:
Resolder resistor R3 to R1, short R8.
Connect CS to GND.
Connect DC to GND.
Connect RES with 100nf to GND and 10kOhm to VCC.

References:
https://www.rhydolabz.com/displays-c-88/096-oled-display-module-spii2c-128x64-7-pin-blue-p-2079.html

and

https://www.raspberrypi-spy.co.uk/2018/04/i2c-oled-display-module-with-raspberry-pi/
