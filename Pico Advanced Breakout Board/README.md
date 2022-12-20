![Pico Advanced Breakout Board - Front render](https://github.com/TheTrainGoes/GP2040-Projects/blob/main/Pico%20Advanced%20Breakout%20Board/Pico%20Advanced%20Breakout%20Board%20-%20Front%20render.png)

![Pico Advanced Breakout Board - Assembled]([https://github.com/TheTrainGoes/GP2040-Projects/blob/main/Pico%20Advanced%20Breakout%20Board/Pico%20Advanced%20Breakout%20Board%20-%20Front%20render.png](https://github.com/TheTrainGoes/GP2040-Projects/blob/main/Pico%20Advanced%20Breakout%20Board/Pico%20Advanced%20Breakout%20Board%20-%20Assembled.JPG))

Pico Advanced Breakout Board
---

Summary:

The Pico Advanced Breakout Board is based on the Pico Fighting Board (https://github.com/FeralAI/PicoFightingBoard) and is an evolution of my Pico Basic Breakout board.

The Pico Advanced Breakout Board adds a number of new features to the Pico Basic Breakout Board.

This runs on the stock GP2040-CE firmware for the RaspBerry Pi Pico, so all future updates to the main project should be supported.

We have a small but passionate Discord group which you can access here if interested: https://discord.gg/k2pxhke7q8

A massive thank you to FeralAI and everyone on the GP2040-CE Discord server who made this possible!


---

Board design choices:

The Brook form factor was chosen due to its compatibility with a number of existing enclosures and holders.  The RaspBerry Pi mounting area has been setup in a way that allows you to solder directly to the board though the extended pads.  

A 20pin (2x10pin) connector is located in the bottom left of the board, matching the location and pinout of standard Brook boards.  If you are planning to use the 20pin connector you do not need to add screw terminals to the board, and vice versa.  

A BootSel button is available to allow for re-flashing of the firmware while the board is plugged in and also to eliminate the need to remove the Pico cover to access the Pico directly.  

An OLED display breakout is also available on the board by way of the expansion port.  This can be used for I2C modules as well.  It has proper 4.7k resistors on the 5v line routed on the board.

The top row of pads allows for direct solder of wires as well as screw terminals to be added. 

A side row of pads allows for direct solder of wires as well as screw terminals to be added for an additinoal set of inputs.

In adition to this there is aslo a 5pin 2.54mm header available for the Brook hitbox conversion cable set.

A USB-B port has been added thanks to the available test pads on the RaspBerry Pi Pico.

USB direct has also been added via a 5pin 2.54mm header.  Only one ground is needed, but some commercial fightsticks come with a five wire cable.

A spot for addressible RGB LEDs has been added and is compatible with most 5v addressible RGB LEDs.

Player LEDs are possible though another project that I am working on.  More to come on that soon.

Space for the defualt 4 pin harness from Brook are also available via a 4pin JST 2.00mm plug for Capture / LS / RS.

Turbo is accessible thought he main 23 pin screw terminal line.

There are two option pins accessible via a 2pin JST 2.00mm plugs.  These are custiomizable though the web-config mode for features like directional reversal, macros and many upcoming things.

You can also find a 5v out 2pin JST 2.00mm plug on the board for use with accessories that need 5v.

To keep the board looking clean a second board can be added on top of the Pico as a shield to cover it.  

For those that want to order through JLCPCB I have added `JLCJLCJLCJLC` on the board in a hidden area to cover the order number.

For a basic assembly you can remove the second PCB that is used as a shield and omit the nuts, bolts and spring lock washers.  This will expose the bare Pico board and recommended only for green boards.


---

Assembly:

There are two main ways to assemble, a full and lite version of the setup.  The full version has a nice PCB cover for the Pico that is attached via some M2 nuts and bolts.  The lite version is just a bare Pico on the Pico Basic Breakout Board (for this option I recommend doing your Pico Advanced Breakout Board PCB in green).  

The estimated cost of a full setup is $15 USD when ordering enough parts to make 5 units ($50 USD total).  All parts listed are available on AliExpress.


Parts necessary for full assembly:

1 x Pico Advanced Breakout Board (this should be done as 1.6mm thick)<br/>
1 x Pico Advanced Breakout Board Cover (this should be done as 1.0mm thick)<br/>
1 x RaspBerry Pi Pico board<br/>
28 x 3.5mm interlocking screw terminals (1)<br/>
2 x 4.7k SMD resistor (1206 package)
1 x 10k SMD resistro (1206 package)
1 x 100nF SMD capicator (1206 package)
1 x 5v Logic Shifter (SN74LV1T34DBVR on Digikey)
1 x 2x10pin 2.54mm header<br/>
2 x 1x5pin 2.54mm header<br/>
3 x 4pin JST 2.00mm header (2)<br/>
1 x 3pin JST 2.00mm header (2)<br/>
3 x 2pin JST 2.00mm header (2)<br/>
2 x SMD tactile switch (3)<br/>
1 x USB-B 4pin female connector<br/>
4 x M2 8mm Stainless Steel hex socket head bolt (4)<br/>
4 x M2 Brass 3mm standoff (4)<br/>
4 x M2 Stainless Steel nut (4)<br/>

(1) - I typically use 1x 16pin and 1x 7pin screw terminals for the main line and 1x 3pin and 1 x 2pin screw termianls for the second line<br/>
(2) - Either strait or right angle connectors are fine, I recommend right angle connectors to keep pinouts the same<br/>
(3) - Most heights are fine for this although I usually put a short one on the board<br/>
(4) - The assembly order is 8mm bolt -> shield PCB -> 3mm standoff -> main PCB -> nut<br/>


Parts necessary for lite assembly:

1 x Pico Advanced Breakout Board<br/>
1 x RaspBerry Pi Pico board<br/>
28 x 3.5mm interlocking screw terminals (1)<br/>
1 x 2x10pin 2.54mm header<br/>
2 x 1x5pin 2.54mm header<br/>
1 x 5pin JST 2.00mm header (2)<br/>
4 x 4pin JST 2.00mm header (2)<br/>
1 x 2pin JST 2.00mm header (2)<br/>
1 x SMD tactile switch (3)<br/>
1 x USB-B 4pin female connector<br/>

(1) - I typically use a combination of 2pin and 3pin terminals on mine to make the 23 and 5 long chains<br/>
(2) - Either strait or right angle connectors are fine, I recommend right angle connectors<br/>
(3) - Most heights are fine for this although I usually put a short one on the board<br/>


---

How to order a board:

All of the boards so far have been ordered though JLCPCB.  Due to minimum order numbers you would get five of these basic breakout boards.  Here are the steps to make your first order and what options I choose along the way.

1 - Go to JLCPCB.com<br/>
2 - Click on `Instant Quote`<br/>
3 - Click on `Add Gerber file` and choose the file named `Gerber - Pico Advanced Board v2.0.zip`<br/>
4 - Choose the following options for the board:<br/>
- Base Material = FR-4<br/>
- Layers = 2<br/>
- Dimensions = (should auto-populate) 45.01 * 96.01 mm<br/>
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

To add the PCB cover as well follow the same process but select the file `Gerber - Pico Basic Board PCB Cover v2.0.zip` but choose 1.00mm as the thickness on it.
     

---

How to upload firmware:

If uploading the firmware before assembly you can hold the BootSel button on the Pico and plug the device into your computer.  It will show up as an external device.  Copy the GP2040-CE-RaspberryPiPico_v0.5.3.uf2` file to it and wait for the device to disconnect after copying completes.  

If uploading the firmware after assembly plug the Pico into your computer and quickly press the BootSel button twice on the Pico Advanced Breakout Board.  You should see an external device show up on your computer.  Copy the `GP2040-CE-RaspberryPiPico_v0.5.3.uf2` file to it and wait for the device to disconnect after copying completes.  

If something goes wrong and you want to upload the firmware again (or if you have tested out the configuration tool and made a mistake) you can enter BootSel mode via either of the methods above and drag over the included `flash_nuke.uf2` file.  This file will take a moment to write to the Pico, once completed you will see the device disconnect and then re-connect as an external device.  After it has shown up again you can copy the same `GP2040-CE-RaspberryPiPico_v0.5.3.uf2` firmware over to it again.


---

Donations:

Every part of this project is open source, from the GP2040 firmware to the original Pico Fighting Board design and also this Pico Basic Breakout Board design.  

Donations are not necessary but always welcome!  All received donations go into trying new things, ordering new boards and helping people get board setups that might not be in an economic position to get one themselves.

https://www.paypal.com/donate/?hosted_button_id=2JMTZVCGLDYC2


---

Revision History:

v4.0 (advanced breakout board)
- Removed palyer LEDs that were using individual pins
- Added LS/DP/RS slider (these pins can be remapped to something else if desired)
- Added Option headers
- Added second set of main direction inputs via screw terminal + 2.54mm header
- Added proper 5v logic shift circuit
- Added proper resistors to I2C line
- Added tactile switch that is connected to the start button to allow for easy access to the web-config utility when no buttons are connected


v3.0 (advanced breakout board)
- Added player LEDs that can utalize the BitBangGaming Player LED module
- Added more ways to connect additional direction inputs for mix sticks
- Changed the BootSel button type to save space
- Added USB-B
- Added a header for direct access to the USB
- Added a 4pin harness for Capture / LS / RS that is compatible with Brook cables
- Added Turbo and a Turbo LED
- Added 5v out
- Added addressible RGB LEDs


v2.0
- Swapped S1 and S2 to be more consistent with Brook pinout

v1.5
- Added BootSel button to board
- Added OLED display pinout

v1.1
- Corrected 2x10pin size to proper 2.54mm spacing
- Changed screw terminals from 2.54mm to 3.5mm
- Added JLCPCB order number marker to board for easier and cheaper ordering

v1.0
- Original design

---

MIT License

Copyright (c) 2022 TheTrain

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

If you have any question please reach out to me on Twitter @TheTrain24
