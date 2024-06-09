Fork of fan-control-rock5c by Nick Peng
==============
I just needed to change a hardware id for it to work on ROCK5C.
Let me know if you have any issues.

Fan-control 
==============

A tool to control fan speed by temperature automatically for ROCK5C.

Features
--------------
1. Control fan speed by temperature. (above 45 degrees)
2. set fan speed manually

Build & install
==============
```shell
make package
dpkg -i fan-control*.deb
```

Usage
==============
```shell
systemctl enable fan-control
systemctl start fan-control
```
  
Configuration
==============

configuration file locations is `/etc/fan-control.json`, Configuration parameter description:

|Configuration|Description|
|--|--|
|pwmchip|pwmchip id, 1 for auto scan|
|gpio|gpio id, 0 is default gpio |
|pwm-period|PWM period|
|temp-map|temperature configuration table|
|temp|temperature, in degrees Celsius|
|duty|duty ratio|
|duration|duration, in second|


License
===============
MIT License


