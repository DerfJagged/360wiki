# JR Programmer

------

The Xecuter JR Programmer is a device used to read/write to Xbox 360  NANDs and program glitch chips. It works in conjunction with the Windows program JRunner and can be used for JTAG and RGH installs. It also can  be used with the Xecuter X360USB PRO device to flash DVD drives.

Drivers and updates for the device can be found within the program JRunner. 

------

## Switches Usage

There are two possible switches on the JR Programmer:

- The `JP-BL` switch is JR Programmer bootloader mode switch. When the switch is set to `JP-BL`, you can flash new programmer firmware. When the switch is set to the  opposite (blank) side, you can read/write to console NANDs. 
- The  `JP-3` switch is the glitch chip power switch. When the switch is set to `JP-3`, the glitch chip will be powered on and ready to be flashed. When the  switch is set to the opposite (blank) side, the glitch chip will be  powered off. This switch is not present on the original JR Programmer.

## Updating Glitch Chip Timing File

1. Unplug console power and unplug the mini USB cable from your JR Programmer.
2. Set the switch to JTAG-XSVF if not set to that already.
3. Plug in the JR Programmer to your computer via the mini USB cable  and plug in the glitch chip using the glitch chip programming cables.
4. Launch JRunner, select Advanced > Custom NAND/CR Functions, then choose your XSVF file, and start.

## Updating the JR Programmer Firmware

1. Unplug the JR Programmer completely and set the switch on the bottom (if the USB slot is on your left) to JP-BL.
2. Plug in the JR Programmer to your computer via the USB slot. Ensure J-Runner says "bootloader attached".
3. Select Tools > Update JRP FW.
4. Navigate to your J-Runner folder > Common, and select the v2 JRP  firmware. It will take some time to flash. Once it is done, unplug the  JR Programmer and flip the switch at the bottom away from JP-BL and plug it back in. If the LED lights up green, you are done. If not, try  unplugging it a few times.

## Troubleshooting

### General Tips

- Verify all solder points are well done and not bridged. If unsure or think it is badly done, reflow the solder.
- Make sure you are running JRunner as Administrator (Right click JRunner > Run as Administrator).
- JRunner may have issues with Windows 10, either find an older operating system to flash from or try [this](https://mega.nz/#!AAEwSLRS!au6qMJbY-CsMTl92XjRQbhshkniheMwG4RIDZbZ2mAw) version (you must [disable driver signing](https://www.reddit.com/r/360hacks/wiki/troubleshooting/unsigned_drivers)). If you are planning on using an older operating system, you can use  Windows 7 or XP in a VM with USB access (make sure to install .NET  Framework or JRunner won't work).
- Reinstall the drivers by opening Device Manager and right clicking  the entry for JR Programmer and choosing Update Drivers > Browse > My Computer > JRunner > common > drivers, and choosing the  correct driver for your case.
- Some devices have defects: play with the switches and make sure the USB port is soldered on well.

If issues persist, try one of the below fixes.

### Red Light on JR Programmer/JR Programmer not Detected by JRunner

1. Put the bottom left switch on the programmer towards JP-BL.
2. Plug into PC and open JRunner, verify that it says Bootloader Attached.
3. In JRunner: go to Tools > Update jr-p.fw, and browse to the  JRunner folder (in My Computer). Select the commons > PICFLASH*  version relevant to your case (v2 if you have a v2, the other for a v1;  ignore the ISO version).
4. Let it finish reflashing the programmer, then proceed to flip the  switch back away from JP-BL and hold the reset button for 5 seconds.  Your JR Programmer should work after this.

### Unable to start JRunner/.NET Framework errors

Make sure you have the correct version of the .NET Framework installed, which is listed in the README file.