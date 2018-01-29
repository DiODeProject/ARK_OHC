# ARK - Overhead Controller of Sheffield Robotics

Here we provide the Eagle files (schematics, layouts and gerbers) for the implementation of the new Overhead Controller (OHC) for the Kilobots. 

The bootloader for the microcontroller (Atmega328, 16MHZ) is the same as the Arduino Pro Mini and can be found here: https://github.com/arduino/Arduino/tree/master/hardware/arduino/avr/bootloaders/atmega 

The software for the microcontroller can be found here: https://github.com/acornejo/kilolib. 
Because we use 6 IR LED boards instead of 1, in file `ohc.c` we need to change line 33 to `#define ir_mask 0b00111111 | PORTB`. And then compile on the terminal as `make arduino-ohc-16mhz`.

## Citation
If you make use of or extend this design please cite:

* Nikolaidis, E., Sabo, C., Marshall, J. A. R., Reina, A. (2017) Characterisation and upgrade of the communication between overhead controllers and Kilobots. doi: [10.15131/shef.data.4990910.v2](https://figshare.com/articles/Characterisation_and_upgrade_of_the_communication_between_overhead_controllers_and_Kilobots/4990910)

## See Also
* [KilobotArena](https://github.com/DiODeProject/KilobotArena)
* [Kilobot Wiki](http://diode.group.shef.ac.uk/kilobots/index.php/Kilobots)
