# Exchanging the capacitor

## Parts
* [0.68 μF tantalum capacitor](https://www.conrad.de/de/p/tancap-ca42-684m035ab-tantal-kondensator-tht-2-5-mm-0-68-f-35-v-20-b-x-h-4-mm-x-14-mm-1-st-1578634.html)
* [Voltage Reference MC7805CT](https://www.conrad.de/de/p/on-semiconductor-mc7805ct-spannungsregler-linear-typ78-to-220ab-positiv-fest-5-v-1-a-175030.html?searchType=SearchRedirect)
* Generic Lead Solder

## Reference Manuel 
* [LX200 Schematic](http://www.lx200classic.com/files/LX200%20Hand%20Controller.pdf)
* [Manual Voltage Reference MC7805CT](https://asset.conrad.com/media10/add/160267/c1/-/en/000175030DS01/datenblatt-175030-on-semiconductor-mc7805ct-spannungsregler-linear-typ78-to-220ab-positiv-fest-5-v-1-a.pdf)

## Tools
* [Soldering Station](https://www.conrad.de/de/p/basetech-zd-931-loetstation-digital-48-w-150-bis-450-c-1460697.html)
* [Solder Pump](https://www.conrad.de/de/p/toolcraft-lee-192-entloetsaugpumpe-antistatisch-2196503.html)
* [Third Hand](https://www.conrad.de/de/p/inline-dritte-hand-mit-lupe-800404647.html)
* [Soldering Tools](https://www.conrad.de/de/p/toolcraft-lns-151-platinenbesteck-6teilig-2182257.html)

## How to

The power supply of the remote is implemented with the standard 5V voltage reference MC7805CT. On my remote, the capacitor on the input side catched fire. By the datasheet, this reference needs a 0.33 μF capacitor on the input side, but MEADE used a 0.68 μF capacitor. As as capacitor, they choose tantalum capacitor. Because I did wanted to avoid risks, I replaced the broken capacitor with a 0.68 μF tantalum capacitor, but I think it would also be save to use a different type of capacitor and a lower capacitance, as long as it's value is over 0.33 μF. Please note that tantalum capacitors can only be used in one direction, so that their cathode needs to be connected to ground. 
![image](https://github.com/Spo-ck/MEADE-LX200-Telescope-GOTO-Hand-Controller-Repair-Capacitor-Kondensator-Issue-solved/blob/master/Capacitor%20Repair/LX200%20Power%20Supply%20Schemtic.png?raw=true)
[LX200 Schematic](http://www.lx200classic.com/files/LX200%20Hand%20Controller.pdf)
![image](https://github.com/Spo-ck/MEADE-LX200-Telescope-GOTO-Hand-Controller-Repair-Capacitor-Kondensator-Issue-solved/blob/master/Capacitor%20Repair/MC7805CT%20Schematic.png?raw=true)
[Manual Voltage Reference MC7805CT](https://asset.conrad.com/media10/add/160267/c1/-/en/000175030DS01/datenblatt-175030-on-semiconductor-mc7805ct-spannungsregler-linear-typ78-to-220ab-positiv-fest-5-v-1-a.pdf)

At this reference voltage, Ground is implemented on the middle pin (2), the input anode is implemented on the left pin (1), and the output anode is implemented on the right pin (3). 
Unsoldering the broken capacitor worked fine at 300°C with my remote. I sued a solder pump, and if you have problem with getting the solder out of the PCD, it can be useful to add some lead solder. To get the capacitor out of the pcb is also used standard soldering equipment.

Because of the PCB's dimensions, and because the PCB has two layers, I recommend to check on both layers (front and back) if the pads have been soldered to the capacitor, or to separately solder the pins of the capacitor on the pads of the front and the back side.
