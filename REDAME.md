Bipolar Power Converter (BPC) Firmware

Firmware source code for the BPC is written in C, and the program runs on an Atmega2560-16AU microcontroller. Firmware is stored in nonvolatile FLASH memory in the Atmega chip.

To upgrade the firmware, a host computer running Arduino IDE is needed along with the new firmware .ino file. A suitable “In-Circuit Serial Programming” device (ICSP) for Arduino is also needed. This is usually done by programming an Arduino board to serve as a programmer, then selecting “Arduino as ISP” under “Tools => Programmer” in the IDE.

The controller board inside the BPC uses an SD card to configure the BPC. The file “config.txt” on the SD card is read once at startup. Some firmware upgrades may require that the contents of the config.txt file be changed, but the SD card does not contain any firmware code, only configuration data. The SD card does not need to be physically accessed to upgrade the firmware.