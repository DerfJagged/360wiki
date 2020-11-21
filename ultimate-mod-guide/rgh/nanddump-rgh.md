# NAND Dump: NAND-X / JR Programmer

------

This guide will walk you through obtaining NAND dumps, creating a  patched dump, and writing it to the console using a NAND-X or JR  Programmer. The process is the same for both programmers. Although JR  Programmer clones may work, you might want to [check if your JR Programmer is a clone](https://i.imgur.com/8Cx62zb.jpg) in case you expected an original and received a clone.

------

## Equipment Needed

- A NAND-X or JR Programmer
- A PC running Windows Vista or later
- A mini-USB to USB cable
- A soldering iron, solder, and flux (MG 835 recommended)
- Isopropyl alcohol (91% or higher recommended) and cotton swabs
- [J-Runner with Extras](https://cdn.octalsconsoleshop.com/J-Runner with Extras.zip)

## Installing Drivers

1. Extract [J-Runner with Extras](https://cdn.octalsconsoleshop.com/J-Runner with Extras.zip). 
2. First, we need to put Windows in Test Mode in order to install the drivers.
3. Click Start, type “cmd”. Right click the result and click “Run as Administrator”.
4. Select Yes or Continue to the UAC if it appears.
5. Type “bcdedit /set TESTSIGNING ON”
6. Reboot your PC and verify that you see “Test Mode” on your desktop.
7. Plug your JR-Programmer or NAND-X.
8. Click Start, type “Device Manager”. Click on the result.
9. You will see a device listed in “Other devices” as a  “MemoryAccess” or “JR-PROGRAMMER”. Right click it and click “Update  Driver Software”
10. Choose “Browse my Computer for Driver Software”.
11. In the Search path, set it to the J-Runner folder, common/drivers. Then click Next.
12. Windows will search for and install the drivers. On any prompts that come up, choose the positive options.

## Soldering to the Motherboard

1. See the diagram for your motherboard:
   - [Phat](https://www.se7ensins.com/proxy.php?image=http%3A%2F%2Fs15.postimage.org%2Fovvxymbaj%2Fnandxphat.jpg&hash=9f3e0aa042f27397dd1dba9a28d48b86)
   - [Trinity](https://i.imgur.com/qxuVHWKl.jpg)
   - [Corona](https://team-xecuter.com/community/data/attachments/14/14346-9cde96213296dd6b79f461329459fae2.jpg) Ensure to check [these resistors](https://i.imgur.com/9QEmPTJl.jpg)
2. Tin the points with solder and apply some flux
3. Solder the wires as shown

## Reading the NAND

1. Plug your Xbox 360 power supply in, but **do not** turn the console on.
2. Plug the white end of the cable into the programmer. Plug the mini-USB cable into the programmer and your PC. 
3. In J-Runner, select "Read Nand" in the top left. It may prompt  you for your Xbox 360's model, make the correct selection and click OK.  If everything is wired properly, it will read your NAND twice and  automatically compare the dumps. If it says "Device Not Found" or Flash  Config 0x00000000, see the troubleshooting steps at the bottom of this  page. If you get messages about bad blocks, ignore them as J-Runner will remap them for you. When it has finished, it will tell you if the two  dumps are an exact match. If they aren't, take more dumps until you get  matching ones.
4. Copy one of the dumps to a safe place such as cloud storage or  send it to yourself in an email to keep it safe. They are located in the output folder.

## Writing the NAND

1. Plug your Xbox 360 power supply in, but **do not** turn the console on.
2. Plug the white end of the cable into the programmer. Plug the mini-USB cable into the programmer and your PC.
3. In J-Runner, ensure the file you want to write (typically  updflash.bin or nanddump1.bin) is loaded into the Source box. If it  isn't, click "Load Source" and select the file.
4. Select "Write Nand" in the top left. It may prompt you for your  Xbox 360's model, make the correct selection and click OK. J-Runner will write the file to the console. If it says "Device Not Found" or Flash  Config 0x00000000, see the troubleshooting steps at the bottom of this  page.

## Troubleshooting

- **"Device Not Found"**
  - Press the reset button on your NAND-X or JR-Programmer
  - Re-insert the USB cable
  - Check that the drivers are properly installed
  - NAND-X: Check that there is a yellow light illuminated
  - JR-Programmer: Check that there is a green light illuminated
- **"Flash Config 0x00000000"**
  - Check that your power brick is plugged in, with an amber colored  LED, and that it is plugged into your console completely (console turned off).
  - Check your soldering to your motherboard. Each point should be solidly connected and have a shiny round joint.
  - Check that you've cleaned up any flux you had used. Depending on the type, it may be conductive and cause issues. MG 835 is strongly  suggested to avoid this.
- **"Wrong Version"**
  - Press the reset button on your NAND-X or JR-Programmer
  - Re-insert the USB cable
  - 

# NAND Dump: LPT Method

------

This guide will walk you through obtaining NAND dumps, creating a patched dump, and writing it to the console using a LPT cable.

------

## Equipment Needed

- A PC with a 25 pin LPT/printer port. Generally, this port is purple colored.
- A PC running Windows Vista or later
- A soldering iron, solder, and flux
- Isopropyl alcohol (90% or higher recommended) and cotton swabs
- 28AWG or 30AWG wire
- Five 100ohm 1/2W resistors
- A 1N914/4148 switching diode
- A 25-pin male D-sub connector. This can be taken from an old  parallel printer cable, but it will likely need to be taken apart to be  re-wired.
- (Recommended) A 25-pin D-sub connector hood. This will protect your  cable from possible shorts and make the cable more permanent. 
- (Recommended) 2.54mm/0.1" male pin headers and wires with a female pin header so you can attach/detach LPT cable

## Preparing the LPT Cable

If not using a printer cable, cut 7 wires to about 6 inches in  length. It's recommended to use wires with a female pin header on the  end so that the cable can be easily attached/detached from the  motherboard. Using the diagram below, solder a 100ohm 1/2W resistor on  pins 1, 2, 14, 16, 17 on the backside of the D-Sub connector. The  direction of the resistor does not matter. Solder the wires onto the end of the resistors and the two other colored pins in the diagram. Keep in the mind that the diagram is showing the **PC connector side**, meaning that the diagram is accurate if you are looking at the **backside** of the D-Sub connector. Each point should be solidly connected so that a tug on the wire won't disconnect the wire. 

- If you have a full printer cable, you will need to cut off one end  and check whether the pins on the male connector correspond to the wires inside. Some printer cables only have a few wires connected, so you may need to open it and move wires around via soldering onto the connector.

![LPT](https://a.thumbs.redditmedia.com/1h_KsIV9mwT3wDi-xtsMegIwxYyeY-mC2j6vc4LbRp8.png)

Once you've finished soldering, clean up any flux with isopropyl alcohol and cotton swabs.

## Preparing the Motherboard

- If you attached female pin headers on the LPT cable, solder a  male pin header to the 1N914/4148 diode. Ensure that the side of the  diode with the black line is faced away from the male pin header. Solder the side of the diode with the black line to the orange point on the  relevant section of [this diagram](https://i.imgur.com/AgcWDPS.jpg). Solder a male pin header to the rest of the points in the diagram. Each point should be solidly connected so that a tug on the wire won't  disconnect the wire. You should now be able to plug your cable onto the  motherboard and plug it into your **powered off** PC. 
- If you did not attach female pin headers on the LPT cable, use the relevant section of [this diagram](https://i.imgur.com/AgcWDPS.jpg) and solder the 1N914/4148 diode onto the wire on pin 11 (orange),  ensuring that the side with the black line on it is faced away from the  cable connector. Solder the side of the diode with the black line to the motherboard's orange point, and solder the rest of the cable's wires to the corresponding colors on the motherboard. Each point should be  solidly connected so that a tug on the wire won't disconnect the wire.  You should now be able to plug your cable onto the motherboard and plug  it into your **powered off** PC. 

Once you've finished soldering, clean up any flux with isopropyl alcohol and cotton swabs.

## Reading the NAND

1. Download and extract [NandPro 3.0a](http://www.mediafire.com/file/2jujuawjhbb0za0/Nandpro30.rar/file). 
   - If you are using a 64-bit system, download [InpOutBinaries](http://www.mediafire.com/file/15y0sgsb5nm1pk6/InpOutBinaries_1501.zip/file) and extract it into the NandPro folder.
   - If you are using a 32-bit system, run `port95.exe` in the NandPro folder and install it.
2. **With your PC powered off**, plug the LPT cable  into its parallel port. It should be connected to both your Xbox 360 and the PC. Plug your Xbox 360 power supply in, but **do not** turn the console on.
3. Press the Windows key + R and type "cmd" and press enter. In the  Command Prompt, enter these commands with ## being either 16 or 64:
   - `cd Desktop\Nandpro30`
   - `nandpro lpt: -r## original_nand1.bin`
4. Press Enter and it will start dumping the NAND. It will increment a hexadecimal counter, starting at address 0000 and ending at 03FF. If  it says "Could not detect flash controller!" or anything about missing  CB/CD files, see the troubleshooting steps at the bottom of this page.  If you get messages about bad blocks, ignore them. This will create a  file called `original_nand1.bin` in NandPro folder. This  process will take approximately 35 minutes for regular consoles. When it is finished, type the command again, changing the name of the dump as  follows, with ## being either 16 or 64:
   - `nandpro lpt: -r## original_nand2.bin`
5. Download and extract [J-Runner](https://cdn.octalsconsoleshop.com/J-Runner with Extras.zip).
6. Launch J-Runner. Select `...` next to the Source File field and choose `original_nand1.bin`. Select "..." next to the Additional File field and choose `original_nand2.bin`. Press the "Nand Compare" button and it will list any bad blocks and  tell you if the two dumps are an exact match. If they aren't, take more  dumps until you get matching ones.
7. Copy one of the dumps to a safe place such as cloud storage or  send it to yourself in an email to keep it safe. Rename the other dump  to `nanddump1.bin` and move it to the `output` folder in the J-Runner directory.

## Writing the Nand

1. Copy the generated `image_00000000.ecc` or `updflash.bin` file into your Nandpro30 folder. Press the Windows key + R and type  "cmd" and press enter. In the Command Prompt, enter these commands:

- `cd Desktop\Nandpro30`
- `nandpro lpt: -w16 image_00000000.ecc` OR
- `nandpro lpt: -w## updflash.bin` (with ## being either 16 or 64)

1. Press Enter, and it will start writing the modified dump to your  motherboard. It will increment a hexadecimal counter, starting at  address 0000 and ending at 004F. If it says "Could not detect flash  controller!" or anything about missing CB/CDs, see the troubleshooting  steps at the bottom of this page.
2. Once it has successfully written to the motherboard, unplug the  power cable from your Xbox 360 and unplug the LPT cable from the  computer.

## Troubleshooting

- **"Could not detect flash controller!" while dumping**
  - Check that your power brick is plugged in, with an amber colored  LED, and that it is plugged into your console completely (console turned off).
  - Check your motherboard soldering to make sure that you have wires,  resistors, and the diode in the correct places. Each point should be  solidly connected so that a tug on the wire won't disconnect the wire. 
  - Check that the wiring on your LPT connector matches the diagram. The diagram shows *the PC's port*, which is the same as the *back* of the connector.
  - Check that you've cleaned up any flux you had used. Depending on the type, it may be conductive and cause issues.
- **What should I do if I ripped off a soldering pad?**
  - Look online for an alternate point to solder onto. Practice more on junk electronics before attempting to continue.



# NAND Dump: Matrix USB NAND Flasher Method

------

This guide will walk you through obtaining NAND dumps, creating a  patched dump, and writing it to the console using a Matrix USB NAND  Flasher (also known as a MTX SPI NAND Flasher).

------

## Equipment Needed

- Matrix USB NAND Flasher
- A PC running Windows Vista or later
- A mini-USB to USB cable
- A soldering iron, solder, and flux
- Isopropyl alcohol (90% or higher recommended) and cotton swabs
- 28AWG or 30AWG wire
- [J-Runner with Extras](https://cdn.octalsconsoleshop.com/J-Runner with Extras.zip)

## Soldering to the Motherboard

1. See the diagram for your motherboard:
   - [Phat](https://i.imgur.com/yMISSdX.png)
   - [Trinity](https://i.imgur.com/CS2Wa1W.png)
   - [Corona](https://i.imgur.com/3l8bgca.png).
2. Tin the points with solder and apply some flux
3. Solder the wires as shown

## Reading the NAND

1. Plug your Xbox 360 power supply in, but **do not** turn the console on.
2. Plug the mini-USB cable into the programmer and your PC. 
3. In J-Runner, select "Read Nand" in the top left. It may prompt  you for your Xbox 360's model, make the correct selection and click OK.  If everything is wired properly, it will read your NAND twice and  automatically compare the dumps. If it says "Device Not Found" or Flash  Config 0x00000000, see the troubleshooting steps at the bottom of this  page. If you get messages about bad blocks, ignore them as J-Runner will remap them for you. When it has finished, it will tell you if the two  dumps are an exact match. If they aren't, take more dumps until you get  matching ones.
4. Copy one of the dumps to a safe place such as cloud storage or  send it to yourself in an email to keep it safe. They are located in the output folder.

## Writing the NAND

1. Plug your Xbox 360 power supply in, but **do not** turn the console on.
2. Plug the mini-USB cable into the programmer and your PC.
3. In J-Runner, ensure the file you want to write (typically  updflash.bin or nanddump1.bin) is loaded into the Source box. If it  isn't, click "Load Source" and select the file.
4. Select "Write Nand" in the top left. It may prompt you for your  Xbox 360's model, make the correct selection and click OK. J-Runner will write the file to the console. If it says "Device Not Found" or Flash  Config 0x00000000, see the troubleshooting steps at the bottom of this  page.

## Troubleshooting

- **"Device Not Found"**
  - Re-insert the USB cable
  - Check that the drivers are properly installed
- **"Flash Config 0x00000000"**
  - Check that your power brick is plugged in, with an amber colored  LED, and that it is plugged into your console completely (console turned off).
  - Check your soldering to your motherboard. Each point should be solidly connected and have a shiny round joint.
  - Check that you've cleaned up any flux you had used. Depending on the type, it may be conductive and cause issues. MG 835 is strongly  suggested to avoid this.
- **"Wrong Version"**
  - Re-insert the USB cable



