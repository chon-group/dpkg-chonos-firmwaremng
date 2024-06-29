# ChonOS Firmware Layer Manager

|![chonos-firmwaremng]()|
|:--:|
|ChonOS Firmware Layer Manager allows the management of the interfacing and firmware layers. The designer can deploy or update the firmware of Arduino boards remotely without disassembling the cyber-physical system.|

## How to Install?
1) In a terminal run the commands below:

```console
echo "deb [trusted=yes] http://packages.chon.group/ chonos main" | sudo tee /etc/apt/sources.list.d/chonos.list
sudo apt update
sudo apt install chonos-firmwaremng
```

### DESCRIPTION

List of options and arguments:
|Argument|Description|
|-|-|
|--list|shows all connected microcontrollers.|
|||
|--listLibraries|shows all instaled libraries.|
|-i \[library\]| imports a .ZIP library file.|
|-r \[libraryName\]|removes a library.|
|||
|-s \[sketck\]|creates and compile a Firmware Project.|
||-f \[file\] defines the .INO firmware code |
||-b \[board\] defines the firmware board. Should be informed the FQDN (e.g., arduino:avr:uno)|
|-d \[sketck\]|deploys the Firmware Project.|
||-b \[board\] defines the firmware board. Should be informed the FQDN (e.g., arduino:avr:uno)|
||-p \[port\] defines the USB port.|
|--deploy |compiles and deploys the firmware file in the defined port for the defined board|
||-f \[file\] -b \[board\] -p \[port\]|


### EXAMPLES

1. Imports a library for the Arduino Libraries Folder

```sh
sudo chonosFirmwareManager -i /tmp/mylibrary.zip
```

2. Deploys the firmware file for the Arduino UNO board connected at /dev/ttyACM0 port 

```sh
sudo chonosFirmwareManager –-deploy -f firmware.ino -p /dev/ttyACM0 -b arduino:avr:uno
```

## COPYRIGHT
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />The Chonos Firmware Manager is part of the [_Cognitive Hardware on Networks Operating
System (chonOS)_](http://os.chon.group/) and is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>. The licensor cannot revoke these freedoms as long as you follow the license terms:

* __Attribution__ — You must give __appropriate credit__ like below:

LAZARIN, Nilson Mori; PANTOJA, Carlos Eduardo; VITERBO, José. Towards a Toolkit for Teaching AI Supported by Robotic-agents: Proposal and First Impressions. In: WORKSHOP SOBRE EDUCAÇÃO EM COMPUTAÇÃO (WEI), 31. , 2023, João Pessoa/PB. Anais [...]. Porto Alegre: Sociedade Brasileira de Computação, 2023 . p. 20-29. ISSN 2595-6175. DOI: https://doi.org/10.5753/wei.2023.229753.


<details>
<summary> Bibtex citation format</summary>

```
@inproceedings{chonOS,
 author = {Nilson Lazarin and Carlos Pantoja and José Viterbo},
 title = { Towards a Toolkit for Teaching AI Supported by Robotic-agents: Proposal and First Impressions},
 booktitle = {Anais do XXXI Workshop sobre Educação em Computação},
 location = {João Pessoa/PB},
 year = {2023},
 issn = {2595-6175},
 pages = {20--29},
 publisher = {SBC},
 address = {Porto Alegre, RS, Brasil},
 doi = {10.5753/wei.2023.229753},
 url = {https://sol.sbc.org.br/index.php/wei/article/view/24887}
}

```
</details>
