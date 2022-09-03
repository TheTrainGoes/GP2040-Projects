![Development Kit - Pico Prototyping Board - Design image](https://github.com/TheTrainGoes/GP2040-Projects/blob/main/Pico%20Development%20Kit/Development%20Kit%20-%20Pico%20Prototyping%20Board%20-%20Design%20image.png)

![Development Kit - Fightstick Prototyping Board - Design image](https://github.com/TheTrainGoes/GP2040-Projects/blob/main/Pico%20Development%20Kit/Development%20Kit%20-%20Fightstick%20Prototyping%20Board%20-%20Design%20image.png)



Pico Development Kit
---

Summary:

The Pico Development Kit is designed to be a modular system that allows you to build and connect on a standardized system to develop and test things on the RaspBerry Pi Pico.

---

Board design choices:

This project is heavily designed around fabrication through JLCPCB.  

Each board is sized at 100mm x 100mm which is the JLCPCB maximum for their special rate cost + low price shipping.  This should mean that each piece, when ordered seperatly will cost you around $7.50 CAD (@ $6 USD) for 5x pieces.

Each board can be connected together physically through the expander plates if desired, or the boards can be used on their own.  

Each board interfaces with each other though 2.54mm male DePont pins / headers.

For those that want to order through JLCPCB I have added `JLCJLCJLCJLC` on the board in a hidden area to cover the order number.

---

Parts necessary for full assembly on each board:

Pico Prototyping Board
27 x SMD 3x6x2.5mm Tactile Switch (2pin)<br/>
1 x RaspBerry Pi Pico board<br/>
4 x 2x10pin 2.54mm header<br/>
1 x 1x4pin 2.54mm header<br/>
1 x 1x5pin 2.54mm header<br/>
1 x 1x3pin 2.00mm PH connector<br/>
1 x USB-B connector socket 90o<br/>
4 x 2.54mm 0.1" Pitch PCB Screw Terminal 16pin<br/>

Fightstick Prototyping Board
1 x 2x10pin 2.54mm header<br/>
4 x 1x4pin 2.54mm header<br/>
2 x 1x2pin 2.54mm header<br/>
1 x 2.42" OLED display (convereted from 7pin to 4pin)<br/>
19 x 6mmx6mm Tactile Switch<br/>

LED Prototyping Board
54 x WS2812b addressible RGB LEDs<br/>
54 x 100nF 1206 SMD capacitors<br/>
2 x 2x10pin 2.54mm header<br/>
2 x 2x5pin 2.54mm header<br/>
1 x 1x6pin 2.54mm header<br/>

Expander Plate A
4 x M3 10mm spacer<br/>
8 x M3 6mm button top hex bolts<br/>

Expander Plate B
4 x M3 6mm button top hex bolts<br/>
4 x M3 nuts (or acorn nuts)<br/>

---

How to order a board:

All of the boards so far have been ordered though JLCPCB.  Due to minimum order numbers you would get five of these boards.  Here are the steps to make your first order and what options I choose along the way.

For the following boards use these steps:
- Pico Prototyping Board
- Fightstick Prototyping Board
- LED Prototyping Board

1 - Go to JLCPCB.com<br/>
2 - Click on `Instant Quote`<br/>
3 - Click on `Add Gerber file` and choose the file named `Gerber - Pico Arcade Breakout Board v2.0.zip`<br/>
4 - Choose the following options for the board:<br/>
- Base Material = FR-4<br/>
- Layers = 2<br/>
- Dimensions = (should auto-populate) 100mm * 100mm mm<br/>
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

For the following boards use these steps:
- Expander Plate A
- Expander Plate B

1 - Go to JLCPCB.com<br/>
2 - Click on `Instant Quote`<br/>
3 - Click on `Add Gerber file` and choose the file named `Gerber - Pico Arcade Breakout Board v2.0.zip`<br/>
4 - Choose the following options for the board:<br/>
- Base Material = Aluminum<br/>
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

Donations:

Every part of this project is open source, from the GP2040 firmware to the original Pico Fighting Board design and also this Pico Basic Breakout Board design.  

Donations are not necessary but always welcome!  All received donations go into trying new things, ordering new boards and helping people get board setups that might not be in an economic position to get one themselves.

https://www.paypal.com/donate/?hosted_button_id=2JMTZVCGLDYC2
