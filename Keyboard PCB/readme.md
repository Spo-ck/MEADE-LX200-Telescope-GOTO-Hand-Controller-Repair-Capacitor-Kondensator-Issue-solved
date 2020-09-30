## Keyboard

![image](https://github.com/Spo-ck/MEADE-LX200-Telescope-GOTO-Hand-Controller-Repair-Capacitor-Kondensator-Issue-solved/blob/master/Keyboard%20PCB/pictures/new%20keyboard.jpg?raw=true)
***new keyboard pcb***

### Parts
* [LED 3mm Rot](https://www.conrad.de/de/p/tru-components-1577379-led-bedrahtet-rot-rund-3-mm-125-mcd-60-20-ma-1577379.html)
* [19 x Micro Switches](https://www.shop-014.de/michawi-p5362h110s463-micro-Taster-MT-04-E.html)
* [PCB](https://www.reichelt.de/punkt-streifenrasterplati-hartpapier-160x100mm-h25ps160-p23953.html?&trstct=pol_5&nbc=1)
* Generic 42 Ω Resistor
* [Dupond Connectors](https://www.reichelt.de/entwicklerboards-dupont-crimp-set-610-teilig-debo-set-dupont-p279901.html?&trstct=pos_0&nbc=1)
* Generic solid core wires (PCB)
* Generic cables (Connector cable to mainboard)
* Generic Lead Solder

### Reference Manuel 
* [LX200 Schematic](http://www.lx200classic.com/files/LX200%20Hand%20Controller.pdf)

### Tools
* [Soldering Station](https://www.conrad.de/de/p/basetech-zd-931-loetstation-digital-48-w-150-bis-450-c-1460697.html)
* [Solder Pump](https://www.conrad.de/de/p/toolcraft-lee-192-entloetsaugpumpe-antistatisch-2196503.html)
* [Third Hand](https://www.conrad.de/de/p/inline-dritte-hand-mit-lupe-800404647.html)
* [Soldering Tools](https://www.conrad.de/de/p/toolcraft-lns-151-platinenbesteck-6teilig-2182257.html)

### Pinmapping

Mapping of the different keyboard switches to the pins of the 20 pin header:

1. GOTO
2. Mode
3. E
4. ENTER
5. N
6. W
7. S
8. 9
9. 8
10. 7
11. 5
12. 6
13. 4
14. 1
15. 2
16. 3
17. 0
18. Prev
19. Next
20. GND

![image](https://github.com/Spo-ck/MEADE-LX200-Telescope-GOTO-Hand-Controller-Repair-Capacitor-Kondensator-Issue-solved/blob/master/Keyboard%20PCB/Schematics/LX200%2020pin%20header.png?raw=true)
[LX200 Schematic](http://www.lx200classic.com/files/LX200%20Hand%20Controller.pdf)

### How to

Rebuilding the keyboard is pretty simple. I took the mapping from the LX200 reference schematic and rebuilt it using standard parts according to schematic I uploaded here.
The 19 switches have to be soldered on a standard pcb with a distance of 13mm first. After that, the ground pins of all switches are connected together. 

![image](https://github.com/Spo-ck/MEADE-LX200-Telescope-GOTO-Hand-Controller-Repair-Capacitor-Kondensator-Issue-solved/blob/master/Keyboard%20PCB/Schematics/Keyboard%20schmatic.png?raw=true)
***new schematic***

It is important that the original switches have a resistance between 30 and 60 Ω. To emulate this, I connected a 42 Ω Resistor in series to the ground pins of the switches.

After the ground pins have been soldered, also the positive sides of the switches have been soldered according to the schematic. 

In order to connect the PCB directly to the main board, I crimped dupont / jumper connectors on the cables and plugged them on the 20 pin header of the main board. Because it should be easy to remove the keyboard again, 5 4-Pin connectors have been used instead of a single 20-Pin connector.

In oder to remove the old 20pin connector of the old keyboard, soldering tools are very helpful. It is also very handy to remove some of the claps of the 20 pin header. 

In a last step, I added LEDs between the buttons. According to the original schematic, 2 LEDs (LED9 & LED10) are connected in series directly to the 5V reference as a backlight for the buttons. As it can be hard to only use 2 LEDs for 19 buttons, I increased the number of LEDs. It is recommendable to connect the LEDs in two subsystems that contain an equal number of LEDs. The LEDs of each subsystem are connected in parallel. In the next step, LED 9 and LED 10 are unsoldered, and Subsystem 1 is then connected to the Pads of LED 9, and Subsystem 2 is connected to the Pads of LED 10. Please mind that LEDs have to be connected in the correct way.

![image](https://github.com/Spo-ck/MEADE-LX200-Telescope-GOTO-Hand-Controller-Repair-Capacitor-Kondensator-Issue-solved/blob/master/Keyboard%20PCB/Schematics/LX200%20LED%20Schemtic.png?raw=true)
[LX200 Schematic](http://www.lx200classic.com/files/LX200%20Hand%20Controller.pdf)

![image](https://github.com/Spo-ck/MEADE-LX200-Telescope-GOTO-Hand-Controller-Repair-Capacitor-Kondensator-Issue-solved/blob/master/Keyboard%20PCB/Schematics/LED%20Shematic.png?raw=true)
***led schmatic***

Besides the LEDs for the buttons backlight, there are also 5 LEDs for the mainboard to indicate its current mode. The holes that I designed in the front case will perfectly fit to these LEDs, so that you can see them through the holes after installing the mainboard into the case. For a better vision, also caps for the LEDs can be designed in a way that they insulate one LEDs light from the LEDs next to it. Another ides is to unsolder the LEDs and replace them. The holes are made in a way that the LEDs mentioned above will perfectly fit. In only thing you need to do is to sonder wires and maybe dupond connectors between the new LEDs and the Main board.
