WARNING **Dangerous voltages**: RS232 uses voltages as high as +/- 30V. 

**You are building this circuit on your own responsibility.**

# Retroduino

Arduino with RS232 port, that works with Arduino Studio.

After connecting to PC you will be able to upload a new sketch from Arduino Studio and use Serial Monitor,
just as with the regular USB connection. Restart functionality is provided via RS232 DTR signal line.
Check provided schematic for more details.

When connecting to PC use _RS232 Straight Cable_ (one end should be Male and the other should be Female).
DO NOT USE CROSS CABLE (both ends Male).

I have used _LogiLink USB2.0 to Serial Adapter_ to connect this project to my PC. No drivers were required for Linux. System detected a new serial port at `/dev/ttyUSB0`. Which can also be checked via `sudo dmesg`,
after plugging in USB end of the adapter to PC.

EDIT: DTR line during normal operation has positive voltage >4V (measured on DB-9 socket pin). When Serial port is open it temporarily drops to a negative voltage. We use that to trigger reset operation on ATmega chip.

![On Breadboard](./docs/breadboard.png)

# References

* [RS232 Cables (Straight vs Cross)](https://www.cable-tester.com/rs232-cable-wiring-for-crossed-straight/)
* [MAX232 Connections](https://www.electronics-lab.com/project/rs232-max232-interface-module/)
* [Arduino Uno Rev3 Schematic](https://www.arduino.cc/en/uploads/Main/Arduino_Uno_Rev3-schematic.pdf)
* [MAX232 Datasheet](https://www.ti.com/lit/gpn/MAX232)

