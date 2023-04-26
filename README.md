# chonosFirmwareManager - ChonOS Firmware Layer Manager
A manager of the Firmware Layer for Embedded Multi-agent Systems.

## DESCRIPTION

List of options and arguments:

+ --help          \- shows this tutorial.

+ --list          \- shows all connected microcontrollers.

+ -s [sketck]     \- creates and compile a Firmware Project

  * -f [file]   \- defines the .INO firmware code 
  
  * -b [board]  \- defines the firmware board. Should be informed the FQDN (e.g., arduino:avr:uno)

+ -d [sketck]     \- deploys the Firmware Project

  * -b [board]  \- defines the firmware board. Should be informed the FQDN (e.g., arduino:avr:uno)
  
  * -p [port]   \- defines the USB port.

+ --listLibraries \- shows all instaled libraries.

+ -i [library]    \- imports a .ZIP library file.

## EXAMPLE
Imports a library for the Arduino Libraries Folder
```console
root@machine:~# chonosFirmwareManager -i /tmp/mylibrary.zip
```

Compiles the Firmware Project <myproject> using the source file </tmp/firmware.ino> for the Arduino Mega board   
```console
root@machine:~# chonosFirmwareManager -s myproject -f /tmp/firmware.ino -b arduino:avr:mega
```

Deploys the previously compiled Firmware Project <myproject> for the Arduino Mega board connected at /dev/ttyACM0 port 
```console
root@machine:~# chonosFirmwareManager -d myproject -b arduino:avr:mega -p /dev/ttyACM0
```
## COPYRIGHT
Copyright © 2023 Chon Group http://chon.group. License GPLv3+: GNU GPL version 3 or later https://gnu.org/licenses/gpl.html. This is free software: you are free to change and redistribute it. There is NO WARRANTY, to the extent permitted by law.

