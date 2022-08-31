![Pico Mini Fighter Board - Front render](https://github.com/TheTrainGoes/GP2040-Projects/blob/main/Pico%20Mini%20Fighter/Pico%20Mini%20Fighter%20-%20Front%20render.png)

Pico Mini Fighter Board
---

Summary:

The Pico Mini Fighter Board is based on the Pico Fighting Board (https://github.com/FeralAI/PicoFightingBoard) and runs a customized GP2040-CE firmware ([https://gp2040.info/#/](https://github.com/OpenStickFoundation/GP2040-CE)) on a RaspBerry Pi Pico.

The Pico Mini Fighter Board removes all SMD components while retaining core functionality in form factor that is suited to install in a small spaces.  

I have tested this extensively with the GP2040CE_-_0.5.1_-_Waveshare_RP2040_Zero.uf2 version of the firmware (included in the folder).  Please note that future releases may change default pin layout and require a different version of the board to be created.

Please note that this board requires use of the Waveshare RP2040 Zero board.

We have a small but passionate Discord group which you can access here if interested: https://discord.gg/k87GQU2n


---

Board design choices:

Due to the Waveshare RP2040 Zero having components on both the top and bottom of the PCB, it is necessary to use headers between the Pico and the board.  

A 20pin (2x10pin) 2.54mm connector is located in the bottom left of the board.  

A 4pin (1x4pin) JST 2.00mm header for the standard Brook aux cable (TP / L3 / R3) is located on the leftmost of the board.

A 4pin (1x4pin) JST 2.00mm header for addressable RGB LEDs (Dout / GND / 5v / 5v) is located to the right of the above connector.

For those that want to order through JLCPCB I have added `JLCJLCJLCJLC` on the board in a hidden area to cover the order number.


---

Parts necessary for full assembly:

1 x Pico Mini Fighter Board<br/>
1 x Waveshare RP2040 Zero board<br/>
1 x 2x10pin 2.54mm header<br/>
2 x 1x4pin JST 2.00mm headers<br/>


---

How to order a board:

All of the boards so far have been ordered though JLCPCB.  Due to minimum order numbers you would get five of these basic breakout boards.  Here are the steps to make your first order and what options I choose along the way.

1 - Go to JLCPCB.com<br/>
2 - Click on `Instant Quote`<br/>
3 - Click on `Add Gerber file` and choose the file named `Gerber - Pico Micro Fighter v4.0.zip`<br/>
4 - Choose the following options for the board:<br/>
- Base Material = FR-4<br/>
- Layers = 2<br/>
- Dimensions = (should auto-populate)<br/>
- PCB Qty = 5<br/>
- Product Type = Industrial/Consumer electronics<br/>
- Different Design = 1<br/>
- Delivery Format = Single PCB<br/>
- PCB Thickness = 1.6<br/>
- PCB Color = (up to you)<br/>
- Silkscreen = (defaults to white for all except white boards which is black)<br/>
- Surface Finish = HASL(with lead)<br/>
- Outer Copper Weight = 1oz<br/>
- Gold Fingers = No<br/>
- Confirm Production file = No<br/>
- Flying Probe Test = Fully Test<br/>
-  Castellated Holes = No<br/>
- Remove Order Number = Specify a location<br/>
- No advanced options<br/>

5 - Click on `SAVE TO CART`<br/>
6 - Go through checkout process, ensure to select economic shipping to keep costs low


---

How to upload firmware:

If uploading the firmware before assembly you can hold the Boot button on the Pico and plug the device into your computer.  It will show up as an external device.  Copy the `GP2040CE_-_0.5.1_-_Waveshare_RP2040_Zero.uf2` file to it and wait for the device to disconnect after copying completes.  

If something goes wrong and you want to upload the firmware again (or if you have tested out the configuration tool and made a mistake) you can enter BootSel mode via either of the methods above and drag over the included `flash_nuke.uf2` file.  This file will take a moment to write to the Pico, once completed you will see the device disconnect and then re-connect as an external device.  After it has shown up again you can copy the same `GP2040CE_-_0.5.1_-_Waveshare_RP2040_Zero.uf2` firmware over to it again.


---

Donations:

Every part of this project is open source, from the GP2040 firmware to the original Pico Fighting Board design and also this Pico Basic Breakout Board design.  

Donations are not necessary but always welcome!  All received donations go into trying new things, ordering new boards and helping people get board setups that might not be in an economic position to get one themselves.

https://www.paypal.com/donate/?hosted_button_id=2JMTZVCGLDYC2


---

Revision History:

v4.0
- Added more length to the board to ensure enough space for the 2 x 4pin JST 2.00mm connectors
- Added info about the 2 x 4pin JST 2.00mmm connectors on the back of the board

v3.0
- Small changes to default pinout

v2.0
- Changed design of the aux connectors from 2.54mm to 2.00mm

v1.0
- Original design
