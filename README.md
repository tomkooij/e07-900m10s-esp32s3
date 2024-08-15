# e07-900m10s-esp32s3 adapter board for ESP32 S3 DevKit and mini boards
Adapter board for [ebyte e07-900m10s CC1101 module](https://www.ebyte.com/en/product-view-news.html?id=1567)

3d view:
![3dview](pics/3d.png)

![pcb](pics/pcb.png)

This should run [Ramses_ESP](https://github.com/IndaloTech/ramses_esp/) out of the box on:

ESP32 S3 DevKit-C module (9 units wide)
(TODO link and pic)

[ESP32 S3 DevKit-C module](https://nl.aliexpress.com/item/1005006387668474.html) (10 units wide)

Waveshare ESP32 s3 mini 
(Close 2 solder bridges to connect 3v3 and GND on pins 1 and 2)

ESP32 c3 mini board.
(Close the other solder bridges, 3v3 and GND are off by two pins, botch wires needed)

 - The header is a standard .1" (2.54mm) PCB header.
 - C1 and C2 are 1206 SMD size
 - C1 = 100nF
 - C2 = 10uF
 - C2 is probably not needed, it is used as a buffer for large currents while sending.
 - LED TX blue SMD 1206
 - LED RX green SMD 1206
 - THT LEDs as backup.
 - Suitable values for R1-R4 is 22O ohm
 - Antenna connector is [PCB SMA female](https://nl.aliexpress.com/item/1005005708712726.html) (use standard 1.6mm board thickness)
 - The IPEX stamp antenna on the module should also be useable (not tested)

This repo contains the KiCad 8 files as well as the gerbers to produce the PCB.
I used JLCPCB for my board. Just upload the zip-file in the gerber folder to JLPCB.

## Known issues (improvements)
 - Messed up the ESP32C3 supermini pinout. Jumper/botch wires necessary.
 - Mounting holes not 100% square
 - Mounting hole H1 is in ESP32S3 Antenna keep out zone
 - Pin markings on back of PCB (for soldering) would be nice

## Prototype:

![ramses_esp proto](pics/ramses_esp_proto.png)

This is a clone of the (excellent!) [Ramses_ESP](https://github.com/IndaloTech/ramses_esp/) Ramses-II RF bridge. (evofw3 HGI-80 clone).
Using the esp32-s3 it clones the behaviour of the HGI-80: RF tot USB serial and adds MQTT over WiFi.

## Where can I order?
Buy the original ramses ESP from [IndaloTech](https://indalo-tech.onlineweb.shop/). This product is not affialiated at all with IndaloTech. It's just a clone. However, I've previously bought a SSM-D2 (ramses_esp predecessor) and its build quality is excellent.

You can order the PCB from your favorite PCB fabshop using the gerbers in the gerber folder. I used JLCPCB.

I might sell some stuff on [Tweakers V&A](https://tweakers.net/aanbod/user/90636/) (NL only)
