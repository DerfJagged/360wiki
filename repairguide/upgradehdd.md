# Upgrading your Hard Drive

------

This guide will walk you through installing a new hard drive. While  this is easy on a JTAG/RGH, unmodified consoles need special handling to make it be recognized by the Xbox operating system.

A guide for using HDDhackr for stock consoles can also be found on [MrMario2011's channel](https://youtu.be/XIrW4pzVNmk?list=PL1CadovfabPskGb2Ur4kBGzD5s7DzQw5I).

------

## Installing New Hard Drive in RGH/JTAG

The size limit for an internal hard drive on a JTAG/RGH console is 2TB.

- You will need:
  - A Windows computer or Windows virtual machine
  - 7zip/WinZip/WinRAR or your choice of extraction program.
  - A USB storage device
  - Dashlaunch and XeXMenu both installed in order to completely set up the hard drive.
  - (For fat consoles) T6 and T10 Torx screw drivers
  - (Optional for slim/E consoles) An [internal HDD support enclosure](https://www.ebay.com/itm/250GB-Internal-Xbox-360-Slim-Hard-Drive-Disk-Case-for-Microsoft-Xbox-360-Game-/392064624098)

1. If you have a slim/E model, insert the hard drive. If you have a fat console, take apart the Xbox hard drive container and replace the hard  drive inside. Note that on fat models, you will have to remove the shiny Microsoft warranty sticker to get to a screw on the outside.
2. Turn your Xbox on and navigate to Console Settings → System Info,  and find your console's serial number and write it down. This is also  available on the back of your console.
3. Navigate to Storage. The hard drive will be listed as unformatted. 
4. Select the unformatted hard drive and choose Format, and Yes. You will be prompted to put in your serial number.
5. Create a new profile on your hard drive.
6. Install both Dashlaunch and XeXMenu. Alternatively, you can just copy everything over from your old hard drive or USB device.
7. On your PC, download the latest system update from [Xbox.com](http://www.xbox.com/system-update-usb).
8. Extract the update and copy $SystemUpdate to your USB storage  device. You may need to change $SystemUpdate to $$ystemUpdate to bypass  Dashlaunch's update blocker setting.
9. Plug the storage device into your Xbox. This seems to work best when in original dashboard.
10. If you see [THIS](http://i.imgur.com/ukit0G6.png), press yes. **If you see [THIS](http://i.imgur.com/h1oCEDz.png), DO NOT ACCEPT AS YOU WILL BRICK YOUR CONSOLE.**
11. The Xbox 360 will install missing data and then reboot. Verify the  installation by going to the original dashboard and make sure that your  avatar has skin and is completely a pale white color.

- If you wish you play original Xbox games on your 360, [see this page](../ultimate-mod-guide/xboxemu/index.md) to set up the original Xbox files.

## Installing a New Hard Drive in a Stock Console

For stock consoles, you must have a 500GB, 320GB, 250GB, 120GB, 60GB and 20GB **Western Digital** hard drive with a serial number ending in  BEAS/BEVS/BEVT/BPVT/LPVT/BEKT/BJKT/BPKT/BUDT/HLFS/BLFS. Non-Western  Digital drives may be forced to work via [this tutorial](https://digiex.net/threads/xbox-360-how-to-flash-your-hddss-bin-in-windows.8569/), but it is risky and may render the drive unusable.

- You will need:
  - A Windows computer or Windows virtual machine
  - 7zip/WinZip/WinRAR or your choice of extraction program.
  - [Bootable USB Drive Creator Tool](https://digiex.net/attachments/bootable_usb_drive_creator_tool-rar.3435/)
  - [HddHackr](http://www.mediafire.com/file/t6l5o5duaw92qtm/HddHackr_v1.40_Build_20130303.rar/file)
  - (For fat consoles) T6 and T10 Torx screw drivers
  - (Optional for slim/E consoles) [An internal HDD support enclosure](https://www.ebay.com/itm/250GB-Internal-Xbox-360-Slim-Hard-Drive-Disk-Case-for-Microsoft-Xbox-360-Game-/392064624098)

1. Plug your flash drive into your computer.
2. Download [Bootable USB Drive Creator Tool](https://digiex.net/attachments/bootable_usb_drive_creator_tool-rar.3435/) ([mirror](http://www.mediafire.com/file/hgnnc1sctoh24dx/Bootable_USB_Drive_Creator_Tool.rar/file))and extract it to your desktop. Right click the EXE and run as  administrator. If your flash drive information does not populate the  fields, select your flash drive from the Device drop down menu. 
3. Ensure "FAT32" is selected in the File System drop down menu,  ensure that Quick Format and Create Bootable drive are checked. Select  the "..." and select the MS-DOS folder under USB Drive Boot Files and  click OK. Click Start to format the drive.
4. Download the HDD security sector corresponding to your new hard drive from the list below and extract the .bin file.
   - [500GB](http://www.mediafire.com/file/1vxrh9q8dspo7ud/500GB_HDDSS.zip/file)
   - [320GB](http://www.mediafire.com/file/f8ia89pa6ha0h39/320GB_HDDSS.zip/file)
   - [250GB](http://www.mediafire.com/file/ad6i5jou0v2ll58/250GB_HDDSS.zip/file)
   - [120GB](http://www.mediafire.com/file/9b91lcp2aheyiv2/120GB_HDDSS.rar/file)
   - [60GB](http://www.mediafire.com/file/35l5534eh8au6g2/60GB_HDDSS.rar/file)
   - [20GB](http://www.mediafire.com/file/z23p2cg7b752hrz/20GB_HDDSS.rar/file)
5. Extract the chosen HDDSS.zip and rename the .bin to "HDDSS.BIN". 
6. Extract HddHackr and move all of the files onto your bootable USB drive.
7. Shutdown your PC. It's highly recommended to disconnect the hard  drives in your computer to prevent accidental wiping of the wrong drive. Connect your new hard drive and ensure that the bootable USB is plugged in. 
8. Turn your PC back on, and tap the button to get into your BIOS  (usually F2). Find the option for SATA Operation Mode and ensure it is  set to "ATA" or "Disable AHCI" or "Legacy". Save changes and let your  computer reboot. It should boot into a black DOS prompt automatically.  If not, you may need to press a button to go into a boot menu for your  PC and choose the flash drive.
9. Type `hddhackr` and press Enter. All connected hard  drives should be listed. If they are not, try changing your BIOS  settings as mentioned in the above step. If it still doesn't work, you  can try the "risky" method to force the hard drive to work via [this tutorial](https://digiex.net/threads/xbox-360-how-to-flash-your-hddss-bin-in-windows.8569/). 
10. Press the number corresponding to your hard drive  (distinguishable by the serial number) and you will be asked if you want to dump, flash, or restore the firmware on the drive. 
11. Press F to flash. Type in `HDDSS.BIN` and press Enter. You will be presented with a message saying that the information in  HDDSS.BIN does not match the drive’s firmware info, and it asks if you  want to flash it. Press Y and Enter. 
12. It will ask if you want to create partitions 0, 2, and 3. Press Y and Enter. The drive will format and flash itself.
    - UNDO.BIN will be created on your USB drive. If you ever need to roll back to your original drive firmware, you can flash this to the drive.
13. Power off your PC and remove the hard drive. 
14. If you want to restore the original Xbox emulator or move your  old content to your new drive, follow the section below. Otherwise, if  you have a slim/E model, insert the hard drive. If you have a fat  console, take apart the Xbox hard drive container and replace the hard  drive inside. Note that on fat models, you will have to remove the shiny Microsoft warranty sticker to get to a screw on the outside. When you  boot up your Xbox 360, you may be prompted to update your system  software.

## Restoring Original Xbox Emulator and User Content

To install reinstall the original Xbox emulator and move your old  content to the new drive, you will have to connect your old Xbox 360  drive to your computer move the content over. If you do not have an old  hard drive, you can manually install a the original Xbox emulator files.

##### If you have an old hard drive

1. With your PC off, connect your old hard drive to your PC and power it on.
2. Download and extract [Xplorer 360 Extreme 2](http://www.mediafire.com/file/d6nbcpia1k718n0/Xplorer360Extreme2.7z/file) and run it as administrator. Select Drive > Harddrive or Memorycard. 
3. Select Drive > Backup Partition 2, and save it. 
   - If you want to save your old content, you can open Partition 3 > Content, and save all of the data to your PC. 
4. Shutdown Windows, disconnect your old hard drive and connect the new one.
5. Run Xplorer 360 Extreme 2 as administrator and select Drive >  Restore Partition 2, and select the backup you had made from the old  drive. **Do not add your Partition 3 content at this point as it will break the partition**.
6. Close Xplorer360.
7. Download and launch [Party Buffalo](http://www.mediafire.com/file/3o078plegbxzjvz/Party_Buffalo_Xbox_360_Drive_Explorer_2.0.1.0.zip/file) and open your flash drive. You can drag all of your Partition 3 content onto the window. Close the program and unplug your hard drive when you  are finished.
8. If you have a slim/E model, insert the hard drive. If you have a  fat console, take apart the Xbox hard drive container and replace the  hard drive inside. Note that on fat models, you will have to remove the  shiny Microsoft warranty sticker to get to a screw on the outside. When  you boot up your Xbox 360, you may be prompted to update your system  software.
   - If some saves do not work, they may need to be resigned to your profile. This is a per-game basis.

##### If you do not have an old hard drive

1. With your PC off, connect your new hard drive to your PC and power it on.
2. Download and extract the [backwards compatibility partition](http://www.mediafire.com/file/muadxynsm5fd5ol/Partition2.rar/file).
3. Run Xplorer 360 Extreme 2 as administrator and select Drive >  Restore Partition 2, and select the Partition2.bin that you had  downloaded. Close Xplorer360 and remove your drive. 
4. If you have a slim/E model, insert the hard drive. If you have a  fat console, take apart the Xbox hard drive container and replace the  hard drive inside. Note that on fat models, you will have to remove the  shiny Microsoft warranty sticker to get to a screw on the outside. When  you boot up your Xbox 360, you may be prompted to update your system  software.
   - If some saves do not work, they may need to be resigned to your profile. This is a per-game basis.