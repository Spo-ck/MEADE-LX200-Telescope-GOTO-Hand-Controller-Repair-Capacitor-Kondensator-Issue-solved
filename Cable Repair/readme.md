# Reestablishing a connection between the PCB and the keyboard with silver solder varnish

![image](https://github.com/Spo-ck/MEADE-LX200-Telescope-GOTO-Hand-Controller-Repair-Capacitor-Kondensator-Issue-solved/blob/master/Cable%20Repair/Burned%20Wires.png?raw=true abc)
## Parts
* [Silver Conductive Vanish](https://www.amazon.de/YoungerY-leitfähiger-Kleber-anhaftender-Elektronik-Leiterplatte-PWB-Reparatur/dp/B07VV9SPXB/ref=sr_1_3_sspa?__mk_de_DE=ÅMÅŽÕÑ&dchild=1&keywords=silberleitlack&qid=1601325026&sr=8-3-spons&psc=1&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUFEMkFST1YwQzFOWDEmZW5jcnlwdGVkSWQ9QTAwNzgzMzMxWVRXSURTV0FLMVImZW5jcnlwdGVkQWRJZD1BMDA4MTI3NzNFMVNVWVpDRTNUN0smd2lkZ2V0TmFtZT1zcF9hdGYmYWN0aW9uPWNsaWNrUmVkaXJlY3QmZG9Ob3RMb2dDbGljaz10cnVl)
* [Thin Cables](https://www.conrad.de/de/p/lapp-49900276-klingeldraht-1-x-0-80-mm-weiss-braun-meterware-607805.html)

## Tools
* [Third Hand](https://www.conrad.de/de/p/inline-dritte-hand-mit-lupe-800404647.html)
* [Soldering Tools](https://www.conrad.de/de/p/toolcraft-lns-151-platinenbesteck-6teilig-2182257.html)

## How To
After the power supply was repaired, the next problem that needed to be solved was the connection issue with the burned cables. The basic idea was to bridge the cables from one side to be other to make the keyboard work again. In my case, my hand controller used a very thin cable, and the button on the front side of my controller had been integrated in the flat ribbon cable. 
In general, there are 20 cabled integrated in the flat ribbon cable, whereas 19 serve as cables for the positive side of the 19 buttons, and the twentist cable serves as ground connection. You can differentiate the ground cable from the others because its diameter is doubled compared to the other cables. Unfortunately, in my case also the ground was burned, so that all buttons became out of order, whereas if only signal cables would have been burned, the buttons which cables would not have been burned would still work.

In the first attempt I fried to melt the insulation with a soldering iron, and solder cabled to the flat ribbon cable for bridging it. Unfortunately the problem with the flat ribbon cable is, that below 200°C, the insulation does not melt, and above 200°C, the insulation together with the flat cable gets gasified.

This issue was solved with scratching the insulation from one side of the cables. Then silver conductive varnish was applied above the scratches. After letting the varnish dry for one night, it was possible so measure a connection. Sadly, connections glued with varnish are physically not very stable. Because of this, additional cables glued to the flat ribbon cable came off very quickly in every attempt.

As a result it can the sad that it possible to reestablish a connection with conductive varnish, but these connections are not stable enough to be used. Because of this, the next solution was developed.
