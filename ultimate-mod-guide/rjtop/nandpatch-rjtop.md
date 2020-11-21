# NAND Dump: NAND-X / JR Programmer

------

This guide will walk you through obtaining NAND dumps, creating a  patched dump, and writing it to the console using a NAND-X or JR  Programmer. The process is the same for both programmers. Although JR  Programmer clones may work, you might want to [check if your JR Programmer is a clone](https://i.imgur.com/8Cx62zb.jpg) in case you expected an original and received a clone.

------

## Equipment Needed

- A NAND-X or JR Programmer
- A mini-USB to USB cable
- A soldering iron, solder, and flux
- Isopropyl alcohol (90% or higher recommended) and cotton swabs
- 28AWG or 30AWG wire

## Installing Drivers

1. Download and extract [JRunner](http://www.mediafire.com/file/lk6p034dx445fmd/TWM_Jrunner_Package.zip/file). 
2. Press Win+R and type `devmgmt.msc` and press Enter to  open Device Manager. You can also get to it by searching for it in the  Start menu. Plug the USB cable into both your programmer and your PC.  Windows should find it and it will appear as `J-R PROGRAMMER` or `NAND-X` under the "Other Devices" category in Device Manager.
3. If you are on Windows 10, you will need to [disable signed driver enforcement](https://www.reddit.com/r/360hacks/wiki/troubleshooting/unsigned_drivers).
4. Right click the programmer's name and select Update Driver  Software... > Browse my computer for driver software > Browse...  > navigate to your JRunner folder > common > drivers > OK  > Next. You may receive a popup saying that Windows can't verify the  publisher of the driver, select the option to install it anyway. It  should successfully install and file your device under its own category  in Device Manager. Your programmer's LED light should also turn green.

## Soldering to the Motherboard

1. Your kit will come with a cable with a white plug on one end, and either open wires or single plastic connectors on the other end. Solder each wire according to [this diagram](https://i.imgur.com/H0UBur2.jpg) and the colored spots on the picture below. Note that the wire colors  may be different than the picture below. If this is the case, go off of  the wire position and not the color of the wires. ![JR1](../../media/KhM9wPOs9_lFYzHwJpLqmY0CSCA86jXOVf54K-VklTM.png)
2. Once you've finished soldering, clean up any flux with isopropyl alcohol and cotton swabs.

## Dumping the NAND

1. Plug your Xbox 360 power supply in, but **do not** turn the console on.
2. Plug the white end of the cable into the bottom port of the  programmer. Plug the mini-USB cable into the programmer and your PC. 
3. Download the files for the dashboard you wish to upgrade to (such as the [17526 Dashboard Files](http://www.mediafire.com/file/vx321lyc0ng2r51/17526_dash_Jrunner.zip/file)). It's recommended to use the latest dashboard, as older dashboards do  not support newer games. Extract the numbered folder into the `xeBuild` folder inside of the JRunner directory.
4. Launch JRunner. Select "Read Nand" in the top left. It may prompt you for your Xbox 360's model, make the correct selection and click OK. If everything is wired properly, it will read your NAND twice and  automatically compare the dumps. If it says "Device Not Found" or  anything about missing CB/CD files, see the troubleshooting steps at the bottom of this page. If you get messages about bad blocks, ignore them. When it has finished, it will tell you if the two dumps are an exact  match. If they are, you can close JRunner and proceed. If they aren't,  take more dumps until you get matching ones.
5. Copy one of the dumps to a safe place such as cloud storage or  send it to yourself in an email to keep it safe. Rename the other dump  to `nanddump1.bin` and move it to the `output` folder in the JRunner directory.

## Modifying the Dump and Flashing

1. In J-Runner, select "..." next to the Source File field and choose your `nanddump1.bin`. In the top right of the window, the dashboard version 17526 should be  in the dropdown menu next to "Dash Version". If not, select it from the  dropdown menu. 
   - If no dashboards are listed, you will need to download a dashboard , extract it to the XeBuild folder inside your JRunner directory, and  restart JRunner.
2. Select the `Jtag` radio button in the top right of the window and put a check in the `R-jtag` box. If your motherboard is **NOT** a Xenon, put a check in the "Aud_Clamp?" box as well.
3. In the top left of the window, select the button labeled "Write  Xell-Reloaded". If it says "Device Not Found" or anything about missing  CB/CD files, see the troubleshooting steps at the bottom of this page.  If you get messages about bad blocks, ignore them. It may prompt you for your motherboard model again, make the correct choice and press OK. The progress bar will begin moving and stop when it reaches 03FF (or 1900  for a 256MB/512MB Jasper). This process will take ~3 minutes (~10  minutes for a 256MB / 512MB Jasper).
4. Once it has successfully written to the motherboard, unplug the  power cable from your Xbox 360 and unplug the USB cable from the  computer and programmer.
5. Go back to the R-JTOP Hack page and continue at the start of the [Programming the Glitch Chip section](https://old.reddit.com/r/360hacks/wiki/r-jtop#wiki_programming_the_glitch_chip).

## Troubleshooting

- **"Device Not Found" while dumping**
  - Check that your power brick is plugged in, with an amber colored  LED, and that it is plugged into your console completely (console turned off).
  - Check your soldering on both the motherboard and your programmer.  Each point should be solidly connected so that a tug on the wire won't  disconnect the wire.
  - Check that you've cleaned up any flux you had used. Depending on the type, it may be conductive and cause issues.
- **Errors about missing CB/CD files**
  - Try downloading [this bootloader pack](https://www.mediafire.com/file/3jbjey3mqx73qrb/Xbox_360_Bootloader_Files.zip/file) and extract the files into the `common` folder in your JRunner directory.
- **What should I do if I ripped off a soldering pad?**
  - Look online for an alternate point to solder onto. Practice more on junk electronics before attempting to continue.

# NAND Dump: Matrix USB NAND Flasher Method

------

This guide will walk you through obtaining NAND dumps, creating a  patched dump, and writing it to the console using a Matrix USB NAND  Flasher (also known as a MTX SPI NAND Flasher).

------

## Equipment Needed

- Matrix USB NAND Flasher
- A mini-USB to USB cable
- A soldering iron, solder, and flux
- Isopropyl alcohol (90% or higher recommended) and cotton swabs
- 28AWG or 30AWG wire

## Soldering to the Motherboard

1. Solder a wire to each of the J1D2.# and J2B1.# pads. The label  corresponds to what header they will attach to (J1D2 or J2B1) and which  pin on that header.
2. Solder the other ends of the wires to the corresponding points on the motherboard in the diagram below. ![USB-NAND-Flasher1](../../media/_rQvXEUZzbMsRzNwrclpTjFbKW6al_ftd2OTaH4zS_o.png)
3. Once you've finished soldering, clean up any flux with isopropyl alcohol and cotton swabs.

## Dumping the NAND

1. Download and extract [NandPro 3.0a](http://www.mediafire.com/file/2jujuawjhbb0za0/Nandpro30.rar/file). 
   - If you are using a 64-bit system, download [InpOutBinaries](http://www.mediafire.com/file/15y0sgsb5nm1pk6/InpOutBinaries_1501.zip/file) and extract it into the NandPro folder.
   - If you are using a 32-bit system, run `port95.exe` in the NandPro folder and install it.
2. Plug the USB cable into both the Matrix and your PC. Plug your Xbox 360 power supply in, but **do not** turn the console on.
3. Press the Windows key + R and type "cmd" and press enter. In the  Command Prompt, enter these commands. Replace the "16" with "64" if you  have a 256MB or 512MB Jasper.
   - `cd Desktop\Nandpro30`
   - `nandpro usb: -r16 original_nand1.bin`
4. Press Enter and it will start dumping the NAND. It will increment a hexadecimal counter, starting at address 0000 and ending at 03FF (or  1900 for a 256MB/512MB Jasper). If it says "Could not detect flash  controller!" or anything about missing CB/CD files, see the  troubleshooting steps at the bottom of this page. If you get messages  about bad blocks, ignore them. This will create a file called `original_nand1.bin` in NandPro folder. This process will take approximately 5 minutes for  regular consoles, ~30 minutes for 256MB/512MB Jaspers When it is  finished, type the command again, changing the name of the dump as  follows, with ## being either 16 or 64:
   - `nandpro usb: -r## original_nand2.bin`
5. Download and extract [JRunner](http://www.mediafire.com/file/lk6p034dx445fmd/TWM_Jrunner_Package.zip/file). Download the files for the dashboard you wish to upgrade to (such as the [17526 Dashboard Files](http://www.mediafire.com/file/vx321lyc0ng2r51/17526_dash_Jrunner.zip/file)). It's recommended to use the latest dashboard, as older dashboards do  not support newer games. Extract the numbered folder into the `xeBuild` folder inside of the JRunner directory.
6. Launch JRunner. Select `...` next to the Source File field and choose `original_nand1.bin`. Select "..." next to the Additional File field and choose `original_nand2.bin`. Press the "Nand Compare" button and it will list any bad blocks and  tell you if the two dumps are an exact match. If they are, you can close JRunner and proceed. If they aren't, take more dumps until you get  matching ones.
7. Copy one of the dumps to a safe place such as cloud storage or  send it to yourself in an email to keep it safe. Rename the other dump  to `nanddump1.bin` and move it to the `output` folder in the JRunner directory.

## Modifying the Dump

1. In J-Runner, select "..." next to the Source File field and choose your `nanddump1.bin`. In the top right of the window, the dashboard version 17526 should be  in the dropdown menu next to "Dash Version". If not, select it from the  dropdown menu. 
   - If no dashboards are listed, you will need to download a dashboard , extract it to the XeBuild folder inside your JRunner directory, and  restart JRunner.
2. Select the `Jtag` radio button in the top right of the window and put a check in the `R-jtag` box. If your motherboard is **NOT** a Xenon, put a check in the "Aud_Clamp?" box as well.
3. In the top left of the window, select the button labeled "Create  Xell-Reloaded". Ensure that your motherboard model is selected, and  press OK. It will generate a `.bin` file (for example, `xenon.bin` or `jasper_hack_aud_clamp.bin`) in the `output` folder of your JRunner directory. 

## Flashing the Dump

1. Copy the generated `xxxxx.bin` (for example, `xenon.bin`) file into your Nandpro30 folder. Press the Windows key + R and type  "cmd" and press enter. In the Command Prompt, enter these commands,  replacing xxxxx with your file's name and replacing the "16" with a "64" if you are using a 256MB or 512MB Jasper:
   - `cd Desktop\Nandpro30`
   - `nandpro usb: -w16 xxxxx.bin`
2. Press Enter, and it will start writing the modified dump to your  motherboard. It will increment a hexadecimal counter, starting at  address 0000 and ending at 004F. If it says "Could not detect flash  controller!" or anything about missing CB/CD files, see the  troubleshooting steps at the bottom of this page. This process will take approximately 5 minutes for regular consoles, ~30 minutes for  256MB/512MB Jaspers.
3. Once it has successfully written to the motherboard, unplug the  power cable from your Xbox 360 and unplug the USB cable from the  computer and the Matrix.
4. Go back to the R-JTOP Hack page and continue at the start of the [Programming the Glitch Chip section](https://old.reddit.com/r/360hacks/wiki/r-jtop#wiki_programming_the_glitch_chip).

## Troubleshooting

- **"Could not detect flash controller!" while dumping**
  - Check that your power brick is plugged in, with an amber colored  LED, and that it is plugged into your console completely (console turned off).
  - Check your soldering on both the motherboard and Matrix. Each point  should be solidly connected so that a tug on the wire won't disconnect  the wire.
  - Check that you've cleaned up any flux you had used. Depending on the type, it may be conductive and cause issues.
- **Errors about missing CB/CD files**
  - Try downloading [this bootloader pack](https://www.mediafire.com/file/3jbjey3mqx73qrb/Xbox_360_Bootloader_Files.zip/file) and extract the files into the `common` folder in your JRunner directory.
- **What should I do if I ripped off a soldering pad?**
  - Look online for an alternate point to solder onto. Practice more on junk electronics before attempting to continue.