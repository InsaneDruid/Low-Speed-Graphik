# Low Speed Graphik - a HSG clone
The Low Speed Graphik is a 100% compatible clone of the EF9365/9366-based HSG graphics board for PET/CBM 4000 or 8000 series computers from 1982.
It implements all the features, including the high speed vector generation, basic expansion, light pen usage as well as the support for the internal and/or external monitor.

![Low Speed Graphik render](https://github.com/InsaneDruid/Low-Speed-Graphik/blob/main/images/low_speed_graphik_render.png)

Most of the components are readily available. Chips not available from Mouser or Digikey can still be purchased from a variety of sources in China. An optional GAL replacement for the TBP18s030 PROM is provided.

[Schematic](https://github.com/InsaneDruid/Low-Speed-Graphik/blob/main/lsg_schematics.pdf "Schematic")  

[Bill of Materials](https://htmlpreview.github.io/?https://github.com/InsaneDruid/Low-Speed-Graphik/blob/main/lsg_bom.html "Bill of Materials")

## The Firmware
There are several ways to get both the programmed 2332A	ROM and TBP18s030 PROM	
chips for the Low Speed Graphik. One is to use U29 and U11 from a original HSG. 
This works well and is especially interesting for those seeking to replace a broken original HSG pcb.

The other possibility is to program a 2532 EPROM replacing U29 and a 18S030 PROM (or compatible, like 82S123, 27S19, 6331, 74S288, 7603a)
replacing U11. The firmware needed for flashing can be found on the web. The 18S030 can also be replaced by a GAL.

## The GAL Version
A 16v8 GAL can be used to replace the rare TBP18s030 PROM at location U11. This can be done either via an [adapter socket](https://github.com/InsaneDruid/Low-Speed-Graphik/blob/main/gerbers/GAL2PROM_R1.zip "GAL to PROM adapter gerber files") provided by Diddl from forum.classic-computing.de or by using the GAL version of the LSG board which already provides a GAL compatible pinout.

In both cases the [firmware file](https://github.com/InsaneDruid/Low-Speed-Graphik/blob/main/firmware/HSG-Clock-22v10_v4.zip "Firmware for the GAL replacing the TBP18s030 PROM"), also provided by Diddl, is used to program the GAL.

## The ROM Option Jumper
The LSG can be used with either 2332 mask ROMs, pin-compatible 2532 EPROMs or more modern 2732 EPROMs.
A jumper field is provided on the underside of the board. Connect the pads according to the following scheme:  
1-2 for 2332 ROM or 2532 EPROM  
2-3 for 2732 EPROM

## The License
This work is licensed under a Creative Commons Attribution-ShareAlike 4.0 International License.  
See https://creativecommons.org/licenses/by-sa/4.0/.

## The Credits
This work would not have been possible without the help from a bunch of amazing people from [VzEkC e. V. forums](https://forum.classic-computing.de/forum/ "forum.classic-computing.de"). Many thanks go out to:

* *masi* - for providing a working board to test and extract the firmware from
* *Seemann2000* - for the scans of a blank board that were the backbone for this project
* *Toast_r* - for providing reference images, burning the 2532 and building the GAL adapter
* *Jogi* & *vossi* - for providing reference images
* *joshy* - for helping to indentify part values
* *Richi* - for providing a boatload of parts for the prototype
* *Diddl* - for his GAL replacement of the 18S030 PROM
* *funkenzupfer* - for dissecting the master timings that triggered the idea of the GAL replacement
* *CBM_Ba* - for funding, building, and testing the first prototype
