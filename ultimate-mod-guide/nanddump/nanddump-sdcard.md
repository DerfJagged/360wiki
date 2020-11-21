# NAND Dump: SD Card Method

------

This guide will walk you through obtaining NAND dumps, creating a  patched dump, and writing it to the console using a SD card read/write  kit. **This is the only option and is only applicable to Corona Phison/eMMC (V2/V4/V6) motherboards.**

------

## Equipment Needed

- A [supported SD card reader](https://www.ebay.com/sch/i.html?_from=R40&_trksid=p2380057.m570.l1313&_nkw=smoke+usb+card+reader&_sacat=0)
- A PC running Windows Vista or later
- A soldering iron, solder, and flux (MG 835 recommended)
- Isopropyl alcohol (91% or higher recommended) and cotton swabs
- One of the following:
  - SD Tool 2.2 [Link To Buy](https://store.phenommod.com/index.php?route=product/product&path=60_61&product_id=65) **Recommended**
  - Xecuter Corona 4GB NAND RW Kit V4.
  - Maximus SD Tool for 4gb Corona Nand Kit.
  - Your own [DIY R/W cable](http://i.imgur.com/VeWvR.jpg).
- [J-Runner with Extras](https://cdn.octalsconsoleshop.com/J-Runner with Extras.zip)

## Software Setup

- Extract [J-Runner](https://cdn.octalsconsoleshop.com/J-Runner with Extras.zip). 

## Soldering to the Motherboard

- If you bought a SD Tool 2.2, use this [install diagram](https://weekendmodder.com/store/image/catalog/modshop4gb tool.jpg)
- If you bought an Xecuter Corona SD Card R/W kit, it will come with a QSB to install according to this [installation diagram](http://i.imgur.com/I87Y1kO.png).
- If you bought a Maximus SD Tool, install according to [pages 1-4 of the manual](http://www.arcalide.com/download/360/corona/SDTool_Manual_Eng.pdf).
- If you did not buy a R/W kit, you can create your own SD card reader using a microSD to SD card adapter and wiring it up [according to this diagram](http://i.imgur.com/VeWvR.jpg). 

## Reading the NAND

1. With your Xbox 360 powered off and the card reader plugged into a PC, insert the SD card into the reader. Plug your Xbox 360 power supply in, but **do not turn it on**.
2. Launch J-Runner, and in the top right, click the "NAND Type" button and select "Corona 4GB" and OK.
3. In J-Runner, select "Read Nand" in the top left. A pane will open in the lower right, listing some removable drives. If everything is  wired properly, one will show up as Removable Media. If you don't see  it, see the troubleshooting steps at the bottom of this page. Select the drive and click "Read". It will read your NAND twice and automatically  compare the dumps. When it has finished, it will tell you if the two  dumps are an exact match. If they aren't, take more dumps until you get  matching ones.
4. Copy one of the dumps to a safe place such as cloud storage or  send it to yourself in an email to keep it safe. They are located in the output folder.

## Writing the NAND

1. With your Xbox 360 powered off and the card reader plugged into a PC, insert the SD card into the reader. Plug your Xbox 360 power supply in, but **do not turn it on**.
2. Launch J-Runner, and in the top right, click the "NAND Type" button and select "Corona 4GB" and OK.
3. In J-Runner, ensure the file you want to write (typically  updflash.bin or nanddump1.bin) is loaded into the Source box. If it  isn't, click "Load Source" and select the file.
4. Select "Write Nand" in the top left. A pane will open in the  lower right, listing some removable drives. If everything is wired  properly, one will show up as Removable Media. If you don't see it, see  the troubleshooting steps at the bottom of this page. Select the drive  and click "Write". J-Runner will write the file to the console.

## Troubleshooting

- **Console does not show up in the list of devices**
  - Check soldering
  - Make sure you insert the SD card tool before powering the Xbox
  - Make sure the crystal is grounded properly
- **What should I do if I ripped off a soldering pad?**
  - Look online for an alternate point to solder on to. You may need to  repair traces before the console works properly again. Practice more on  junk electronics before attempting to continue.