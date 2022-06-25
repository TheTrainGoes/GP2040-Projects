![Pico Arcade Breakout Board - Front render](https://user-images.githubusercontent.com/32771064/172406353-c0bfd96a-cbc3-417b-9a7e-4387ac7d4c01.png)

Pico Arcade Breakout Board
---

Summary:

The Pico Arcade Breakout Board is based on the Pico Fighting Board (https://github.com/FeralAI/PicoFightingBoard) and runs the same GP2040 firmware (https://gp2040.info/#/) on a RaspBerry Pi Pico.

The Pico Arcade Breakout Board removes all SMD components while retaining core functionality in form factor that is suited to install in a Vewlix or any other arcade machine.  

I have tested this extensively with the GP2040-RaspberryPiPico_v0.4.3.uf2 version of the firmware (included in the folder).  Please note that future releases may change default pin layout and require a different version of the board to be created.

We have a small but passionate Discord group which you can access here if interested: https://discord.gg/k87GQU2n

A massive thank you to FeralAI who made most of this possible!


---

Board design choices:

The RaspBerry Pi mounting area has been setup in a way that allows you to solder directly to the board though the extended pads or stacked with the use of a header if you happen to have gotten a pre-soldered Pico.  

Two 20pin (2x10pin) connectors are located in the bottom left of the board.  If you are planning to use the 20pin connector you do not need to add screw terminals to the board, and vice versa.  

A BootSel button for each board is available to allow for re-flashing of the firmware while the board is plugged in and also to eliminate the need to remove the Pico cover to access the Pico directly.  

An OLED display breakout is also available for each player on the board however most of the functionality of the display is currently quite limited.  

The top and side row of pads allows for direct solder of wires as well as screw terminals to be added.  

To keep the board looking clean a second board can be added on top of the Pico as a shield to cover it.  

For those that want to order through JLCPCB I have added `JLCJLCJLCJLC` on the board in a hidden area to cover the order number.

For a basic assembly you can remove the second PDCs that are used as shields and omit the nuts, bolts and spring lock washers.  This will expose the bare Pico board and recommended only for green boards.


---

There are two main ways to assemble, a full and lite version of the setup.  The full version has a nice PCB cover for the Picos that is attached via some M2 nuts, bolts and washers.  The lite version is just a bare Picos on the Pico Arcade Breakout Board (for this option I recommend doing your Pico Arcade Breakout Board PCB in green).  

The estimated cost of a full setup is $20 USD when ordering enough parts to make 5 units ($100 USD total).  All parts listed are available on AliExpress.


Parts necessary for full assembly:

1 x Pico Arcade Breakout Board<br/>
2 x Pico Arcade Breakout Board Cover<br/>
2 x RaspBerry Pi Pico board<br/>
46 x 3.5mm interlocking screw terminals (1)<br/>
2 x 2x10pin 2.54mm header<br/>
2 x 1x4pin 2.54mm header<br/>
2 x 6x6 4pin through hole tactile switch (2)<br/>
8 x M2 8mm Stainless Steel hex socket head bolt (3)<br/>
16 x M2 Stainless Steel spring lock washer (3)<br/>
16 x M2 Stainless Steel nut (3)<br/>

(1) - I typically use a combination of 2pin and 3pin terminals on mine to make the long chains<br/>
(2) - Most heights are fine for this although I usually put a short one on the board<br/>
(3) - The assembly order is 8mm bolt -> shield PCB -> 2 x spring lock washer -> nut -> main PCB -> nut<br/>


Parts necessary for lite assembly:

1 x Pico Basic Breakout Board<br/>
2 x RaspBerry Pi Pico board<br/>
46 x 3.5mm interlocking screw terminals (1)<br/>
2 x 2x10pin 2.54mm header<br/>
2 x 1x4pin 2.54mm header<br/>
2 x 6x6 4pin through hole tactile switch (2)<br/>

(1) - I typically use a combination of 2pin and 3pin terminals on mine to make the long chains<br/>
(2) - most heights are fine for this although I usually put a short one on the board<br/>


---

How to order a board:

All of the boards so far have been ordered though JLCPCB.  Due to minimum order numbers you would get five of these basic breakout boards.  Here are the steps to make your first order and what options I choose along the way.

1 - Go to JLCPCB.com<br/>
2 - Click on `Instant Quote`<br/>
3 - Click on `Add Gerber file` and choose the file named `Gerber - Pico Arcade Breakout Board v2.0.zip`<br/>
4 - Choose the following options for the board:<br/>
- Base Material = FR-4<br/>
- Layers = 2<br/>
- Dimensions = (should auto-populate) 126.55 * 70.99 mm<br/>
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

To add the PCB cover as well follow the same process but select the file `Gerber - Pico Arcade Breakout Board PCB Cover v2.0.zip`. Keep in mind for every 5 x Pico Arcade Breakout Boards you want to make you will need 10 x PCB covers.
     

---

How to upload firmware:

If uploading the firmware before assembly you can hold the BootSel button on the Pico and plug the device into your computer.  It will show up as an external device.  Copy the `GP2040-RaspberryPiPico_v0.4.3.uf2` file to it and wait for the device to disconnect after copying completes.  

If uploading the firmware after assembly plug the Pico into your computer and quickly press the BootSel button twice on the Pico Basic Breakout Board.  You should see an external device show up on your computer.  Copy the `GP2040-RaspberryPiPico_v0.4.3.uf2` file to it and wait for the device to disconnect after copying completes.  

If something goes wrong and you want to upload the firmware again (or if you have tested out the configuration tool and made a mistake) you can enter BootSel mode via either of the methods above and drag over the included `flash_nuke.uf2` file.  This file will take a moment to write to the Pico, once completed you will see the device disconnect and then re-connect as an external device.  After it has shown up again you can copy the same `GP2040-RaspberryPiPico_v0.4.3.uf2` firmware over to it again.

You will need to do this for each of the Picos on the board.


---

Donations:

Every part of this project is open source, from the GP2040 firmware to the original Pico Fighting Board design and also this Pico Basic Breakout Board design.  

Donations are not necessary but always welcome!  All received donations go into trying new things, ordering new boards and helping people get board setups that might not be in an economic position to get one themselves.

https://www.paypal.com/donate/?hosted_button_id=2JMTZVCGLDYC2


---

Revision History:

v2.0
- Swapped S1 and S2 to be more consistent with Brook pinout
- Added BootSel button to board
- Added OLED display pinout
- Added JLCPCB order number marker to board for easier and cheaper ordering

v1.0
- Original design


---

Usage / Licencing:

I am covering this under Attribution-NonCommercial 4.0 International (CC BY-NC 4.0).

You are free to:
Share — copy and redistribute the material in any medium or format
Adapt — remix, transform, and build upon the material

Under the following terms:
Attribution — You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.
NonCommercial — You may not use the material for commercial purposes.

Read more here: https://creativecommons.org/licenses/by-nc/4.0/

If you have any question please reach out to me on Twitter @TheTrain24
