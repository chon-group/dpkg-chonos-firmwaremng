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
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This ChonOS package is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>. The licensor cannot revoke these freedoms as long as you follow the license terms:

* __Attribution__ — You must give __appropriate credit__ like below:

 LAZARIN, Nilson Mori; PANTOJA, Carlos Eduardo; VITERBO, José. Towards a Toolkit for Teaching AI Supported by Robotic-agents: Proposal and First Impressions. _In_: WORKSHOP SOBRE EDUCAÇÃO EM COMPUTAÇÃO (WEI), 31. , 2023, João Pessoa/PB. Anais [...]. Porto Alegre: Sociedade Brasileira de Computação, 2023 . p. 20-29. ISSN 2595-6175. DOI: https://doi.org/10.5753/wei.2023.229753. 