Hori Fighting Edge
---

Summary:

This project aims to replace the main board in the Hori Fighting Edge (PS3 version) allowing you to connect either a Brook board via the 20pin or a RasBerry Pi Pico that is running the GP2040 firmware.





---

Main PCB pinout:
<br/>
<br/>
Button Loom<br/>
CN5 - XH 2.54mm 9 pin<br/>
<br/>
1 - Grey   - L2       - (4K)<br/>
2 - White  - L1       - (4P)<br/>
3 - Orange - R2       - (3K)<br/>
4 - Purple - R1       - (3P)<br/>
5 - Green  - Circle   - (2K)<br/>
6 - Yellow - Triangle - (2P)<br/>
7 - Red    - Cross    - (1K)<br/>
8 - Blue   - Square   - (1P)<br/>
9 - Black  - Ground<br/>
<br/>
<br/>
Right Side LEDs<br/>
CN6 - PH 2.00mm 3 pin<br/>
<br/>
1 - Blue/Purple  - Red LED<br/>
2 - White        - Ground (needs 100 ohm resistor)<br/>
3 - Black        - Blue LED<br/>
<br/>
<br/>
Touch Panel Buttons<br/>
CN3 - PH 2.00mm 6 pin<br/>
<br/>
1 - Red    - 5v VCC (needs 100 ohm resistor)<br/>
2 - White  - 'CNF' on the touch panel<br/>
3 - Black  - 'X' on the touch panel<br/>
4 - Yellow - 'Select' on the touch panel<br/>
5 - Green  - 'Start' on the touch panel<br/>
6 - Orange - Ground<br/>
<br/>
<br/>
Touch Panel LEDs (Part 1 of 2)<br/>
CN15 - XH 2.54mm 7 pin<br/>
<br/>
1 - Grey - R3 Red LED (needs 100 ohm resistor)<br/>
2 - Orange - Select Red LED (needs 100 ohm resistor)<br/>
3 - Green - NC Red LED (needs 100 ohm resistor)<br/>
4 - Yellow - Lockout 'X' Red LED (needs 100 ohm resistor)<br/>
5 - Black - Lockout 'X' Blue LED (needs 100 ohm resistor)<br/>
6 - White - Touch Panel LED (needs 100 ohm resistor)<br/>
7 - Red - Ground<br/>
<br/>
<br/>
Touch Panel LEDs (Part 2 of 2)<br/>
CN14 - PH2.00mm 9 pin<br/>
<br/>
1 - Red - Circle Red LED (needs 100 ohm resistor)<br/>
2 - White - Cross Red LED (needs 100 ohm resistor)<br/>
3 - Black - Square Red LED (needs 100 ohm resistor)<br/>
4 - Yellow - Triangle Red LED (needs 100 ohm resistor)<br/>
5 - Green - L1 Red LED (needs 100 ohm resistor)<br/>
6 - Orange - R1 Red LED (needs 100 ohm resistor)<br/>
7 - Grey - L2 Red LED (needs 100 ohm resistor)<br/>
8 - Blue - R2 Red LED (needs 100 ohm resistor)<br/>
9 - Purple - L3 Red LED (needs 100 ohm resistor)<br/>
<br/>
<br/>
USB Connection<br/>
CN2 - XH 2.54mm 5 pin<br/>
<br/>
1 - Red - 5v VCC<br/>
2 - White - Data-<br/>
3 - Green - Data+<br/>
4 - Black 1 - USB OTG ID (this can be bridged with pin 5)<br/>
5 - Black 2 - Ground (this can be bridged with pin 4)<br/>
<br/>
<br/>
Joystick Loom<br/>
CN1 - PH 2.00mm 5 pin<br/>
<br/>
1 - Black  - Ground<br/>
2 - Green  - Right<br/>
3 - Yellow - Left<br/>
4 - Orange - Up<br/>
5 - Red    - Down<br/>
<br/>
<br/>
Guide Button (Playstation Button)<br/>
CN4 - Ph 2.00mm 2 pin<br/>
<br/>
1 - Red   - Guide<br/>
2 - White - Ground<br/>
<br/>
<br/>
Left Side LEDs<br/>
CN7 - PH 2.00mm 3 pin<br/>
<br/>
1 - Blue/Purple  - Red LED<br/>
2 - White        - Ground (needs 100 ohm resistor)<br/>
3 - Black        - Blue LED<br/>
<br/>
<br/>
CN12 - Not used on the PS3 version<br/>
<br/>
CN13 - Not used on the PS3 version<br/>




---

Board design choices:

The Brook form factor was chosen due to its compatibility with a number of existing enclosures and holders.  The RaspBerry Pi mounting area has been setup in a way that allows you to solder directly to the board though the extended pads or stacked with the use of a header if you happen to have gotten a pre-soldered Pico.  

A 20pin (2x10pin) connector is located in the bottom left of the board, matching the location and pinout of standard Brook boards.  If you are planning to use the 20pin connector you do not need to add screw terminals to the board, and vice versa.  

A BootSel button is available to allow for re-flashing of the firmware while the board is plugged in and also to eliminate the need to remove the Pico cover to access the Pico directly.  

An OLED display breakout is also available on the board however most of the functionality of the display is currently quite limited.  

The top row of pads allows for direct solder of wires as well as screw terminals to be added.  

To keep the board looking clean a second board can be added on top of the Pico as a shield to cover it.  

For those that want to order through JLCPCB I have added `JLCJLCJLCJLC` on the board in a hidden area to cover the order number.

For a basic assembly you can remove the second PDC that is used as a shield and omit the nuts, bolts and spring lock washers.  This will expose the bare Pico board and recommended only for green boards.


---

Assembly:

There are two main ways to assemble, a full and lite version of the setup.  The full version has a nice PCB cover for the Pico that is attached via some M2 nuts, bolts and washers.  The lite version is just a bare Pico on the Pico Basic Breakout Board (for this option I recommend doing your Pico Basic Breakout Board PCB in green).  

The estimated cost of a full setup is $10 USD when ordering enough parts to make 5 units ($50 USD total).  All parts listed are available on AliExpress.


Parts necessary for full assembly:

1 x Pico Basic Breakout Board<br/>
1 x Pico Basic Breakout Board Cover<br/>
1 x RaspBerry Pi Pico board<br/>
23 x 3.5mm interlocking screw terminals (1)<br/>
1 x 2x10pin 2.54mm header<br/>
1 x 1x4pin 2.54mm header<br/>
1 x 6x6 4pin through hole tactile switch (2)<br/>
4 x M2 8mm Stainless Steel hex socket head bolt (3)<br/>
8 x M2 Stainless Steel spring lock washer (3)<br/>
8 x M2 Stainless Steel nut (3)<br/>

(1) - I typically use a combination of 2pin and 3pin terminals on mine to make the 23 long chain<br/>
(2) - Most heights are fine for this although I usually put a short one on the board<br/>
(3) - The assembly order is 8mm bolt -> shield PCB -> 2 x spring lock washer -> nut -> main PCB -> nut<br/>


Parts necessary for lite assembly:

1 x Pico Basic Breakout Board<br/>
1 x RaspBerry Pi Pico board<br/>
23 x 3.5mm interlocking screw terminals (1)<br/>
1 x 2x10pin 2.54mm header<br/>
1 x 1x4pin 2.54mm header<br/>
1 x 6x6 4pin through hole tactile switch (2)<br/>

(1) - I typically use a combination of 2pin and 3pin terminals on mine to make the 23 long chain<br/>
(2) - most heights are fine for this although I usually put a short one on the board<br/>


---

How to order a board:

All of the boards so far have been ordered though JLCPCB.  Due to minimum order numbers you would get five of these basic breakout boards.  Here are the steps to make your first order and what options I choose along the way.

1 - Go to JLCPCB.com<br/>
2 - Click on `Instant Quote`<br/>
3 - Click on `Add Gerber file` and choose the file named `Gerber - Pico Basic Board v2.0.zip`<br/>
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

To add the PCB cover as well follow the same process but select the file `Gerber - Pico Basic Board PCB Cover v2.0.zip`.
     

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


---

Usage / Licencing:

I am covering this under Attribution-NonCommercial 4.0 International (CC BY-NC 4.0).<br/>
<br/>
You are free to:<br/>
Share — copy and redistribute the material in any medium or format<br/>
Adapt — remix, transform, and build upon the material<br/>
<br/>
Under the following terms:<br/>
Attribution — You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.<br/>
NonCommercial — You may not use the material for commercial purposes.<br/>
<br/>
Read more here: https://creativecommons.org/licenses/by-nc/4.0/<br/>
<br/>
If you have any question please reach out to me on Twitter @TheTrain24
