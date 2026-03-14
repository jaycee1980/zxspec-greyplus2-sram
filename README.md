# zxspec-greyplus2-sram
A replacement RAM module for a ZX Spectrum +2 (Grey) machine to replace 8x4164 chips

# What's it for ?
The grey +2 uses 4164 (64Kx1) DRAM as its system memory... there are two banks of it, one as "Contended" RAM, one as "Uncontended" RAM. This is similar in principle to the 4116 (16x1) DRAM and 4532 (32Kx1) DRAM in the original 48K spectrum. These chips can and do fail, and procuring replacements is getting more and more difficult.

For 48K spectrums, there are Lower and Upper RAM Replacement boards utilising modern 5V SRAM as a replacement. I couldn't find an equivalent solution for a grey +2 though.

So here we are! :)
![image of assembled board](/pictures/assembled.jpg)

# Building it
The gerber.zip file in this repository contains Gerber files needed by a PCB manufacturer to make the board. I personally use [JLCPCB](https://jlcpcb.com) but any PCB manufacturer should be able to produce it.

The [BOM file](/bom.txt) contains the parts needed to make the board. Please note that I have only personally used the Cypress CY62128ELL-45ZAXI memory at the moment, but the other SRAM listed there should also work. You *might* need to install C4 in some cases. My personal grey +2 worked just fine without it.

Also be aware that on the back of the PCB there is a jumper pad. This should be bridged such that the A pad is connected to the middle pad. You can use a solder blob, a short length of wire, or a 0 ohm resistor for this.

