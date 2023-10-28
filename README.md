# ChonOS Firmware Layer Manager

This manager allows the upgrade of the firmware layer in embedded systems constructed using Arduino boards.

## DESCRIPTION

List of options and arguments:

+ ___--help___          \- shows this tutorial.

+ ___--list___          \- shows all connected microcontrollers.

+ ___-s [sketck]___     \- creates and compile a Firmware Project

  * -f [file]   \- defines the .INO firmware code 
  
  * -b [board]  \- defines the firmware board. Should be informed the FQDN (e.g., arduino:avr:uno)

+ ___-d [sketck]___     \- deploys the Firmware Project

  * -b [board]  \- defines the firmware board. Should be informed the FQDN (e.g., arduino:avr:uno)
  
  * -p [port]   \- defines the USB port.

+ ___--listLibraries___ \- shows all instaled libraries.

+ ___-i [library]___    \- imports a .ZIP library file.

+ ___-r [libraryName]___ \- removes a library.

+ ___--deploy -f [file] -b [board] -p [port]___ \- compiles and deploys the firmware file in the defined port for the defined board

## EXAMPLE
Imports a library for the Arduino Libraries Folder
```console
sudo chonosFirmwareManager -i /tmp/mylibrary.zip
```

Deploys the firmware file for the Arduino Mega board connected at /dev/ttyACM0 port 
```console
sudo chonosFirmwareManager –-deploy -f firmware.ino -p /dev/ttyACM0 -b arduino:avr:uno
```
## COPYRIGHT
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This ChonOS package is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>. The licensor cannot revoke these freedoms as long as you follow the license terms:

* __Attribution__ — You must give __appropriate credit__ like below:

 LAZARIN, Nilson Mori; PANTOJA, Carlos Eduardo; VITERBO, José. Towards a Toolkit for Teaching AI Supported by Robotic-agents: Proposal and First Impressions. _In_: WORKSHOP SOBRE EDUCAÇÃO EM COMPUTAÇÃO (WEI), 31. , 2023, João Pessoa/PB. Anais [...]. Porto Alegre: Sociedade Brasileira de Computação, 2023 . p. 20-29. ISSN 2595-6175. DOI: https://doi.org/10.5753/wei.2023.229753. 

 ```
@inproceedings{chonOS,
author = {Nilson Lazarin and Carlos Pantoja and José Viterbo},
title = {Towards a Toolkit for Teaching AI Supported by Robotic-agents: Proposal and First Impressions},
booktitle = {Anais do XXXI Workshop sobre Educação em Computação},
location = {João Pessoa/PB},
year = {2023},
keywords = {},
issn = {2595-6175},
pages = {20--29},
publisher = {SBC},
address = {Porto Alegre, RS, Brasil},
doi = {10.5753/wei.2023.229753},
url = {https://sol.sbc.org.br/index.php/wei/article/view/24887}
}
 ```