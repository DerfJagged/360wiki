# NAND-X Programmer

------

The Xecuter NAND-X is a device used to read/write to Xbox 360 NANDs  and program glitch chips. It works in conjunction with the Windows  program JRunner and can be used for JTAG and RGH installs. It also can  be used with the Xecuter X360USB PRO device to flash DVD drives.

Drivers and updates for the device can be found within the program JRunner. 

------

## Updating Glitch Chip Timing File

1. Unplug console power and plug the mini USB cable from your NAND-X  into your PC. Plug in the glitch chip using the glitch chip programming  cables.
2. Launch JRunner, select Advanced > Custom NAND/CR Functions, then choose your XSVF file, and start.

## Updating the NAND-X Firmware

1. Plug the NAND-X into to your computer via a USB port. Ensure JRunner says "bootloader attached".
2. Select Tools > Update NAND-X FW.
3. Navigate to your J-Runner folder > Common, and select the NAND-X  firmware. It will take some time to flash. Once it is done, unplug the  NAND-X and plug it back in. If the LED lights up green, you are done. If not, try unplugging it a few times.

## Troubleshooting

### General Tips

- Verify all solder points are well done and not bridged. If unsure or think it is badly done, reflow the solder.
- Make sure you are running JRunner as Administrator (Right click JRunner > Run as Administrator).
- JRunner may have issues with Windows 10, either find an older operating system to flash from or try [this](https://mega.nz/#!AAEwSLRS!au6qMJbY-CsMTl92XjRQbhshkniheMwG4RIDZbZ2mAw) version (you must [disable driver signing](https://www.reddit.com/r/360hacks/wiki/troubleshooting/unsigned_drivers)). If you are planning on using an older operating system, you can use  Windows 7 or XP in a VM with USB access (make sure to install .NET  Framework or JRunner won't work).
- Reinstall the drivers by opening Device Manager and right clicking  the entry for NAND-X and choosing Update Drivers > Browse > My  Computer > JRunner > common > drivers, and choosing the correct driver for your case.
- Some devices have defects, so ensure sure the USB port is soldered on well.

If issues persist, try one of the below fixes.

### NAND-X not Detected by JRunner

Try pressing the Black reset button on the NAND-X and see if it detects it. If not, follow the steps below. 

1. Plug into PC and open JRunner, verify that it says Bootloader Attached.
2. In JRunner: go to Tools > Update nand-x.fw, and browse to the  JRunner folder (in My Computer). Select the commons > PICFLASH*  version relevant to your case (ignore the ISO version).
3. Let it finish reflashing the programmer, then hold the reset button for 5 seconds. Your NAND-X should work after this.

### Unable to start JRunner/.NET Framework errors

Make sure you have the correct version of the .NET Framework installed, which is listed in the README file.