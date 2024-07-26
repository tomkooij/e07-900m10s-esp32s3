# e07-900m10s-esp32s3 adapter board for ESP32 S3 DevKit and mini boards
Adapter board for [ebyte e07-900m10s CC1101 module](https://www.ebyte.com/en/product-view-news.html?id=1567)

(currently in production at JLPCB)

3d view:
![3dview](pics/3d.png)

This should run Ramses ESP out of the box on:

ESP32 S3 DevKit-C module (9 units wide)
(TODO link and pic)

ESP32 S3 DevKit-C module (10 units wide)
(TODO link and pic)

Waveshare ESP32 s3 mini 
![ramses_esp with esp32s3](breakout_esp32s3mini.png)
(Close 2 solder bridges to connect 3v3 and GND on pins 1 and 2)

ESP32 c3 mini board.
(Close the other solder bridges, untested, may need some extra wires)

 - The header is a standard .1" (2.54mm) PCB header.
 - C1 and C2 are 1206 SMD size
 - C1 = 100nF
 - C2 = 4.7uF
 - C2 is probably not needed, it is used as a buffer for large currents while sending.
 - LED TX blue SMD 1206
 - LED RX green SMD 1206
 - THT LEDs as backup.
 - Suitable values for R1-R4 is 22O ohm
 - Antenna connector is [PCB SMA female](https://nl.aliexpress.com/item/1005005708712726.html) (use standard 1.6mm board thickness)
 - The IPEX stamp antenna on the module should also be useable (not tested)

This repo contains the KiCad 8 files as well as the gerbers to produce the PCB.
I used JLPCB for my board. Just upload the zip-file in the gerber folder to JLPCB.
