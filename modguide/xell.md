Installing Linux

# Xenon Linux Loader (XeLL)

------

Xenon Linux Loader (XeLL) is a Linux based second-stage bootloader  that runs at boot time. XeLL is capable of loading an ELF file from  network (TFTP) or CDROM (ISO9660), running apps made with libXenon, or  booting into a Linux distribution. 

XeLLous is a modification of XeLL that supports flashing NAND images  (updflash.bin), patches for rebooter images (updpatch.bin), and  obtaining CPU/DVD keys or a NAND dump via HTTP. 

XeLL Reloaded is the latest branch of XeLL, which also supports ELF file loading from USB (FAT/ext2) or HDD(FAT/ext2/XTAF). 

- RGH/JTAG exploited Xbox 360s are set up with some variant of  XeLL, but set to boot directly into a dashboard without ever showing the XeLL screen. This page assumes the user is using XeLL Reloaded. 
- On a RGH/JTAG, you can launch XeLL by holding the faceplate Sync button while booting up the console.

------

## Updating XeLL

1. Download the desired XeLL binary file and rename it to `updxell.bin`. 
2. Supply the `updxell.bin` file to XeLL via USB/CD/DVD/HDD or TFTP.
3. It should automatically find the update and flash it.
4. Reboot the Xbox 360 and the new XeLL build should be applied.

### Troubleshooting:

- **XeLL can't find `updxell.bin` / update process doesn't start**
  - Your XeLL version does not support update patches. You must rebuild  your XeBuild image the updated XeLL. From then on you can use the  automated update feature.
- **The update function reports that no XeLL binary was found in NAND**
  - Your XeLL version is too old or it's not a XeLL Reloaded binary. You must rebuild your XeBuild image the updated XeLL. From then on you can  use the automated update feature.

## Flashing a NAND Image

1. Rename the NAND image to `updflash.bin`.
2. Supply the `updflash.bin` file to XeLL via USB/CD/DVD/HDD.
3. It should automatically find the update and flash it.
4. Reboot the Xbox 360 and the new NAND image should be applied.

## Using kboot.conf

1. Read the [kboot.conf sample](https://github.com/Free60Project/xell-reloaded/blob/master/kboot.conf) which is part of every XeLL release with kboot-support.
2. Modify the file to your needs.
3. Supply it, named as `kboot.conf`, via USB/CD/DVD/HDD or TFTP.
4. Boot XeLL and wait till it loads the file and shows the config menu.
5. Navigate to the desired bootentry, and it should launch when selected. You can do this in the following ways:

- UART: 
  -  UP/DOWN to go up and down in the menu
  -  ENTER to confirm your choice
  -  C to cancel the menu
- X360 Controller (1st):
  -  DPAD-UP/DPAD-DOWN to go up and down in the menu
  -  A to confirm your choice
  -  B to cancel the menu
- X360 Media Remote:
  -  UP/DOWN to go up and down in the menu
  -  OK to confirm your choice
  -  Press the NUMBER of the desired bootentry to directly load it
  -  B to cancel the menu

## Web Interface

By default, if you boot XeLL with an ethernet cable is plugged in, it will either pull an IP from your router via DHCP or it will use the  default IP of `192.168.1.99` if you are not connected to a  router. You must unplug any wireless USB adapters if you have them  plugged in, as it will halt the boot process. By entering the IP address shown toward the bottom of XeLL on a web browser, it should pull up a  XeLL Reloaded web page. The following are displayed:

- CPU Key
- DVD Key
- Raw Flash (download): This will download a dump of your flash chip straight to the device you are using. 
- Key Vault: This will download a decrypted keyvault file straight to the device you are using. 
- Fuses: This will download a file listing the status of your CPU fuses straight to the device you are using. 
- Startup Log: This will display a text file of all the events that  have been printed to the screen since boot, some of which you can't  normally see.
- Shutdown
- Reboot

### Troubleshooting:

- **The Xbox 360 does not boot properly after flashing the NAND**
  - Either your NAND image wasn't properly remapped or bad settings were applied when building the image.
- **kboot.conf gets found but it doesn't show bootentries or autoloads a bootentry**
  - Make sure timeout is set to something higher than 0
  - Make sure you didn't forget the "" on the bootentry: `label="kernelpath params"`
  - Also take care of using a text editor which does not automatically  break lines if they are too long (will break bootentries), also it  shouldn't modify the encoding and line endings of the config