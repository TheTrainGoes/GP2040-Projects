Pico Basic Breakout Board
---

Summary:

The Pico Basic Breakout Board is based on the Pico Fighting Board (https://github.com/FeralAI/PicoFightingBoard) and runs the same GP2040 firmware (https://gp2040.info/#/) on a RaspBerry Pi Pico.

The Pico Basic Breakout Board removes all SMD components while retaining core functionality in a Brook form factor board.  

I have tested this extensively with the GP2040-RaspberryPiPico_v0.4.3.uf2 version of the firmware (included in the folder).  Please note that future releases may change default pin layout and require a different version of the board to be created.

We have a small but passionate Discord group which you can access here if interested: https://discord.gg/k87GQU2n

A massive thank you to FeralAI who made most of this possible!


---

Board design choices:

The Brook form factor was chosen due to its compatibility with a number of existing enclosures and holders.  The RaspBerry Pi mounting area has been setup in a way that allows you to solder directly to the board though the extended pads or stacked with the use of a header if you happen to have gotten a pre-soldered Pico.  A 20pin (2x10pin) connector is located in the bottom left of the board, matching the location and pinout of standard Brook boards.  If you are planning to use the 20pin connector you do not need to add screw terminals to the board, and vice versa.  A BootSel button is available to allow for re-flashing of the firmware while the board is plugged in and also to eliminate the need to remove the Pico cover to access the Pico directly.  An OLED display breakout is also available on the board however most of the functionality of the display is currently quite limited.  The top row of pads allows for direct solder of wires as well as screw terminals to be added.  To keep the board looking clean a second board can be added on top of the Pico as a shield to cover it.  For those that want to order through JLCPCB I have added `JLCJLCJLCJLC` on the board in a hidden area to cover the order number.

For a basic assembly you can remove the second PDC that is used as a shield and omit the nuts, bolts and spring lock washers.  This will expose the bare Pico board and recommended only for green boards.


---

There are two main ways to assemble, a full and lite version of the setup.  The full version has a nice PCB cover for the Pico that is attached via some M2 nuts, bolts and washers.  The lite version is just a bare Pico on the Pico Basic Breakout Board (for this option I recommend doing your Pico Basic Breakout Board PCB in green).  

The estimated cost of a full setup is $10 USD when ordering enough parts to make 5 units ($50 USD total).  All parts listed are available on AliExpress.


Parts necessary for full assembly:

1 x Pico Basic Breakout Board
1 x Pico Basic Breakout Board Cover
1 x RaspBerry Pi Pico board
23 x 3.5mm interlocking screw terminals *
1 x 2x10pin 2.54mm header
1 x 1x4pin 2.54mm header
1 x 6x6 4pin through hole tactile switch **
4 x M2 8mm Stainless Steel hex socket head bolt ***
8 x M2 Stainless Steel spring lock washer ***
8 x M2 Stainless Steel nut ***

* - I typically use a combination of 2pin and 3pin terminals on mine to make the 23 long chain
** - Most heights are fine for this although I usually put a short one on the board
*** - The assembly order is 8mm bolt -> shield PCB -> 2 x spring lock washer -> nut -> main PCB -> nut


Parts necessary for lite assembly:

1 x Pico Basic Breakout Board
1 x RaspBerry Pi Pico board
23 x 3.5mm interlocking screw terminals*
1 x 2x10pin 2.54mm header
1 x 1x4pin 2.54mm header
1 x 6x6 4pin through hole tactile switch**

* - I typically use a combination of 2pin and 3pin terminals on mine to make the 23 long chain
** - most heights are fine for this although I usually put a short one on the board


---

How to order a board:

All of the boards so far have been ordered though JLCPCB.  Due to minimum order numbers you would get five of these basic breakout boards.  Here are the steps to make your first order and what options I choose along the way.

1 - Go to JLCPCB.com
2 - Click on `Instant Quote`
3 - Click on `Add Gerber file` and choose the file named `Gerber - Pico Brook Basic Board v2.0.zip`
4 - Choose the following options for the board
     Base Material = FR-4
     Layers = 2
     Dimensions = (should auto-populate) 45.01 * 96.01 mm
     PCB Qty = 5
     Product Type = Industrial/Consumer electronics
     Different Design = 1
     Delivery Format = Single PCB
     PCB Thickness = 1.6
     PCB Color = (up to you)
     Silkscreen = (defaults to white for all except white boards which is black)
     Surface Finish = HASL(with lead)
     Outer Copper Weight = 1oz
     Gold Fingers = No
     Confirm Production file = No
     Flying Probe Test = Fully Test
     Castellated Holes = No
     Remove Order Number = Specify a location
     No advanced options
5 - Click on `SAVE TO CART`
6 - Go through checkout process, ensure to select economic shipping to keep costs low
     

---

How to upload firmware:

If uploading the firmware before assembly you can hold the BootSel button on the Pico and plug the device into your computer.  It will show up as an external device.  Copy the `GP2040-RaspberryPiPico_v0.4.3.uf2` file to it and wait for the device to disconnect after copying completes.  

If uploading the firmware after assembly plug the Pico into your computer and quickly press the BootSel button twice on the Pico Basic Breakout Board.  You should see an external device show up on your computer.  Copy the `GP2040-RaspberryPiPico_v0.4.3.uf2` file to it and wait for the device to disconnect after copying completes.  

If something goes wrong and you want to upload the firmware again (or if you have tested out the configuration tool and made a mistake) you can enter BootSel mode via either of the methods above and drag over the included `flash_nuke.uf2` file.  This file will take a moment to write to the Pico, once completed you will see the device disconnect and then re-connect as an external device.  After it has shown up again you can copy the same `GP2040-RaspberryPiPico_v0.4.3.uf2` firmware over to it again.


---

Donations:

Every part of this project is open source, from the GP2040 firmware to the original Pico Fighting Board design and also this Pico Basic Breakout Board design.  

Donations are not necessary but always welcome!  All received donations go into trying new things, ordering new boards and helping people get board setups that might not be in an economic position to get one themselves.

https://www.paypal.com/donate/?hosted_button_id=2JMTZVCGLDYC2


---

Revision History:

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
