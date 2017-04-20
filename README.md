# ARK - Overhead Controller of Sheffield Robotics

Here we provide the Eagle files (schematics, layouts and gerbers) for the implementation of the new Overhead Controller (OHC) for the Kilobots. 

The bootloader for the microcontroller (Atmega328, 16MHZ) is the same as the Arduino Pro Mini and can be found here: https://github.com/arduino/Arduino/tree/master/hardware/arduino/avr/bootloaders/atmega 

The software for the microcontroller can be found here: https://github.com/acornejo/kilolib
Because we use 6 IR LED boards instead of 1, in file ohc.c we need to change line 33 to "#define ir_mask 0b00111111 | PORTB".
