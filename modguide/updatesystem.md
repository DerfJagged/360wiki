# Stock



# NAND Modded

## Updating your Kernel/Dashboard

------

**WARNING: Do not never update your console using original system update. This will install a default NAND and wipe your hacks!**

This guide will walk you through updating your Kernel/Dashboard to  latest version (currently 17511). Keeping your Kernel/Dashboard up to  date ensures that you can run newer games in your console and give you  the latest features implemented in the official dashboard. By following  this guide, the latest Kernel/Dashboard will be patched to include  Dashlaunch (using your console information) and then flashed to your  console.

A video demonstration of how to update your JTAG/RGH dashboard can be found on [MrMario2011's channel](https://youtu.be/cvd3QSNZhss?list=PL1CadovfabPskGb2Ur4kBGzD5s7DzQw5I).

------

## Requirements

- A Windows PC
- A JTAG/RGH Xbox 360
- A NAND dump (flashdmp.bin file) and your CPU Key (FUSE.txt file) - [Guide](https://360.consolemods.org/modguide/nanddump/index.html)
- A router (the Xbox 360 and your PC needs to be in same network)
- [Simple 360 NAND Flasher 1.2](http://www.homebrew-connection.org/files/xbox/nand_flasher/dl_Simple_360_NAND_Flasher_v1.2.rar)
- Unofficial [xeBuild GUI](https://mega.nz/#!Il50wSKK!8cM-a4slhEyAR3Tr4my2-G4O5XlHvEv9P_Z-ZlcSUec) (currently v2.099)

## Patching the NAND

1. Download and launch xeBuild GUI on your PC.
2. Click "Open" for "Source File" top of the window and select your "flashdmp.bin".
3. Click "Get CPUKey/CFLDV from FUSE.txt" and select your "FUSE.txt" file.
4. Verify that everything looks normal in "Motherboard information" section.
5. Verify that Kernel version 2.0.17511.0 is selected.
6. Verify that output path in top of window is good.
7. Click Generate hacked image in bottom of the window. If everything  went well, you should end up with fresh NAND file called "updflash.bin".

## Flashing your Patched NAND

1. Download Simple 360 NAND Flasher and extract it to a folder on your computer.
2. Copy updflash.bin to the same folder.
3. Launch Simple 360 NAND Flasher on your console.
4. Press A and then Start to flash your NAND. If everything went fine  you get message saying it was successful and console will shutdown.
5. Boot your console and verify that everything works. Make sure your are in latest kernel version.

## Installing the Avatar Data

1. On your PC, download the latest system update from [Xbox.com](http://www.xbox.com/system-update-usb).
2. Extract the update and copy $SystemUpdate to your USB storage  device. You might need to change $SystemUpdate to $$ystemUpdate to  bypass update blocker.
3. Plug the storage device into your Xbox. This seems to work best when in original dashboard.
4. If you see [THIS](http://i.imgur.com/ukit0G6.png), press yes. **If you see [THIS](http://i.imgur.com/h1oCEDz.png), DO NOT ACCEPT AS YOU WILL BRICK YOUR CONSOLE.**
5. The Xbox 360 will install missing data and then reboot. Verify the  installation by going to the original dashboard and checking that your  avatar has skin and does not look like ghost anymore.