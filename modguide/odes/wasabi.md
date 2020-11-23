# Wasabi 360 ODE

------

The Wasabi 360 Ultra is an ODE (Optical Drive Emulator) that allows  you to emulate your Xbox 360’s optical disc drive and run Xbox 360 or  original Xbox ISO’s from an eSATA or USB (adapter required) storage  device.

Safe for live?

Description, user manual, update link

------

## Modes of Operation

## AP25 Setup

## HDD Setup

## Automatic Key Extraction

Hold the Left button on the Wasabi while powering on your console.  Once you are on the dashboard, navigate to the Picture Viewer section  and see if there is a folder indicating a successful key extraction.  Reboot your console and the Wasabi will be usable.

Slim Hitachi drives and Lite-On 16D5S drives are supported by Wasabi360S providing that you have the drive key

## Updating the Firmware

You can check your firmware version by holding the UP button on the  Wasabi 360 Ultra while turning on your console, then browsing to the  Picture Viewer to see the version listed there. Reboot your console to  return it to normal operation. If you are not on the latest version,  download the latest firmware update and follow these steps:

1. Place the `wasabi‐update.bin` file into the `wasabi` folder on your Wasabi 360 Ultra’s HDD. 
2. Power off your Xbox 360, and power on your HDD.
3. Ensure that pass‐through mode is selected on the Wasabi, by placing the mode switch in the correct position.
4. Hold down the SELECT button on the Wasabi 360 Ultra control panel.
5. While holding down the SELECT button, turn on your Xbox 360. A blue  LED should start blinking on your Wasabi 360 Ultra. This indicates that  the update process is underway and you can let go of the SELECT button. **Do not turn off your Xbox 360 or unplug the Wasabi 360 Ultra until the update is complete!**
6. After a few moments, a green LED should turn on to indicate that the update was successful. If the update failed, a red LED will turn on  instead. Turn off your Xbox 360.
7. Select emulation mode by placing the mode switch in the correct position and continue normal use.

## Troubleshooting

You may see an error message instead of the list of ISOs in the Video Library on the dashboard as follows: 

- **NTFS cluster size is not 4kb** - Non‐standard cluster sizes are not supported, your external hard drive must be formatted  with NTFS using the standard 4kb cluster size
- **HDD not NTFS formatted** - Your external hard drive  connected to the Wasabi 360 Ultra MUST be formatted with NTFS. Other  file system formats such as FAT32 are not supported.
- **HDD not connected** - An external hard drive could  not be detected. Check that the HDD is properly connected to the Wasabi  360 Ultra and reset the Xbox 360.
- **ODD not connected** - The ODD connection could not be detected. The original disc drive for your Xbox 360 must be connected  as per the instructions in the installation manual. Check the connection and try again.
- **\wasabi\key.bin not found** -The Key.bin file was not found on your HDD. Ensure that your Key.bin file is placed on the HDD  according to the preceding instructions or perform automatic key  extraction following the steps in a section above.