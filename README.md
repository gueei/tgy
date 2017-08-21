https://github.com/sim-/tgy

https://github.com/bluerobotics/tgy

This tree branches from BlueRobotics' implementation of BlueESC (discontinued). 
It allows I2C communication from the host to the ESC. 

At the moment, only Afro ESC with all-N FEs is providing pinouts for I2C. 

The original ESC program require assigning the I2C Address in the firmware - 
i.e. Changing address means flashing the firmware. 
In this version, the address is saved in EEPROM and can be changed via I2C:

Register
0xCE	(read-write) 1-byte I2C Address 

Program limits the address to 0x03 - 0x3F, and the changed address will be available 
in the next power-on. 
