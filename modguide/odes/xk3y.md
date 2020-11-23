# XK3Y (X360KEY) ODE

------

The XK3Y is an Optical Drive Emulator (ODE). This device sits between your DVD drive and motherboard and can serve up ISO files from a USB  storage device in place of discs. The XK3Y, like any ODE, relies on you  dumping your own DVD key for your target console. The XK3Y comes in the  original form and the later revision, the XK3Y-Reloaded which is a  smaller board that appears to be prone to more issues. There are five  modes of operation: ISOMenu, DVDMenu, Remote (extra hardware), and WiFi  (extra hardware), and passthrough mode (disabled). The full manual can  be found [here](http://www.mediafire.com/file/wt1716qz3q3fq9q/Xk3yManual.pdf/file), and a massive XK3Y guide can be found [here](https://www.se7ensins.com/forums/threads/se7ensins-official-x360key-thread.591545/).

**Do not insert a hard drive or flash drive into the USB adapter dongle while the console is powered on.**

**You must stealth patch your games using ABGX in order to play online safely.**

------

## Installation

1. The most difficult and important step is to dump your DVD key  and/or DVD firmware (which includes the DVD key). This can be done by  dumping the NAND of the Xbox or by using a Maximus Lizard, an X360 USB  Pro, or with Jungle Flasher (specific drives only). 
   - (Slims) Rename your firmware dump to `dummy.bin`. If you  dumped your firmware with a Maximus Lizard, proceed to the next step. If you used a X360 USB Pro or Jungle Flasher, you will need to test  different ALTSLIMFW values in xkey.cfg (discussed later) to get it to  work properly due to there being multiple firmware versions for each  drive which are only detected by the Maximus Lizard. 
   - (Phats) You will need a full dump of your DVD drive, Rename it to `firmware.bin`.
2. Plug your SD card into a SD card reader and into your PC. It may  complain about needing to format partitions, which you should say "No"  or "Cancel" to. It should pop up one usable partition called XKEY. If  there are any files present, delete them..
3. Download and extract [JungleFlasher](http://www.mediafire.com/file/wo646d43l2irend/JungleFlasher.0.1.96.Beta%28323%29.rar/file) and open JungleFlasher.exe. You may receive an error when opening on a  64-bit PC, missing ports, or missing files, which you can ignore.  However, if you receive an error about `libusb0.dll` missing, you will need to copy `libusb0.dll` from the "libusb` folder into the main Jungle Flasher folder in order for the program to run.
4. Select the Open Source Firmware button on the right-hand side and choose your DVD firmware dump. This will populate your DVD drive  information in the top half of the window, including your DVD key.  Select "No" if prompted to auto-load a firmware. Alternatively, if you  know your DVD key, you can select the stock firmware for your DVD model  and select "No" if prompted to auto-load a firmware or set the DVD key. 
5. Download the [stock firmware](http://beta.ivc.no/wiki/index.php/Xbox_360_DVD_Drive_Firmware) for your DVD model. Select the Open Target Firmware button on the  right-hand side and choose it. If you are using a stock firmware as your Source firmware, select the "Manual Spoofing" button on the right-hand  side, enter your DVD key in the top field. Select the drop down for  "Spoofed As" at the bottom of the screen, but don't select an option,  and press OK. 
6. Click the Save to File on the right-hand side and save it as `dummy.bin` (slims) or `firmware.bin` (phats) on your XK3Y SD card. Ensure that the name is all lowercase. At this point, safely eject the SD card and plug it back into your  powered-off Xbox 360.
7. Plug your USB storage device that you plan on using into your PC. Ensure that it is formatted as NTFS or ext4. Place your ISOs into a  folder called `games` (all lowercase) on your USB storage  device. You may have any folder names or sub-folder structure you want,  so long as everything is contained in the `games` folder. 
8. Follow the pictures found in the [official manual](http://www.mediafire.com/file/wt1716qz3q3fq9q/Xk3yManual.pdf/file) to physically install the XK3Y in your system. Double check that the  SATA and power plugs are in the correct places on the XK3Y. **Especially check that the ribbon cable is plugged in correctly, with the blue tab  facing up on the XK3Y side, and the blue tab facing away from the  console on the USB adapter dongle. Reversing this may kill your XK3Y**.
9. Follow the instructions for your desired mode of operation from the sections below. 

### ISOMenu

ISOMenu mode allows you to choose your game using the System Music player.

1. Download the [latest XK3Y firmware](http://www.mediafire.com/file/5v7sxmpiprqgn23/XK3y-02.01-4.zip/file). Edit the included xkey.cfg and set `MENUISO=Y` and `MENUDVD=N` and save it. You can also set `RESUMELAST=Y` to make it pull up the last played disc first instead of having to select the game every time.
2. (Slims) If your DVD firmware was dumped using a X360 USB Pro or  Jungle Flasher, you may need to set a value for ALTSLIMFW in xkey.cfg as follows:
   - For Slim consoles that say 0225 in Jungle Flasher but are 9504 labeled use the value ALTSLIMFW=7
   - For Slim consoles that say 0401 in Jungle Flasher but are 0225 labeled use the value ALTSLIMFW=8
   - For all other slim consoles, if you get errors when trying to launch a game ISO (like play DVD) try values from 1 to 6.
   - If you do not get errors then do not change the default value of 0.
3. Copy `rootfs`, `uImage`, and `xkey.cfg` to the root of your USB storage device. Safely eject your USB storage device and plug it into your powered-off Xbox 360.
4. Power on the Xbox 360 and let it sit for five minutes. This ensures that the XK3Y has enough time to apply its update.
5. Reboot the Xbox 360. 

From now on, you should be able to press the A button on the "Open  Tray" option, which will not open your disc drive but rather pretend to  open and close it again, inserting a virtual "Mixed Media Disc". From  here, you can press the Guide button, scroll to the right and choose  Select Music, select Current Disc, select your game, then upon seeing  the "Eject to Load" icon, press the Guide button, and Y to eject and  start the game. This also can be done through the Pictures Viewer.

### DVDMenu

DVDMenu mode allows you to use a custom made DVD menu to choose your  game. You can customize the menu with backgrounds, music, and trailers,  and it will automatically pull down cover art and metadata for the games when you build the menu. It is NOT dynamic, meaning that you will need  to compile a new menu every time you add a new ISO.

1. Download and install [DVDStyler](http://www.dvdstyler.org/en/downloads) (version 2.5+ required).
2. Download and extract [XKeyBrew](https://bitbucket.org/Badisi/xkeybrew/wiki/Home). Right-click xkeybrew.exe and select "Run as Administrator". If not  automatically prompted with options, move your cursor to the right edge  of the screen and select the Options button.
3. With your USB storage device plugged into your PC, select the "games" folder that holds your ISOs on the storage device.
4. (optional) Select the path to where you have ABGX installed. This  will show an icon on the main menu of the game library allowing you to  run the selected game through abgx360 to patch games to be Xbox Live  "safe".
5. Leave the rest of the settings alone unless you want to change them, and click Save.
6. Move your cursor to the right edge of the screen and select the  DvdMenu button. Select a theme from the drop down menu in the top right  and check the box next to any of the games that you want to add. You can click the picture of any game and edit the details if you wish.
7. Move your cursor to the right edge of the screen and select the icon which looks like an arrow pointing down into a tray.
8. Ensure all of the advanced options are selected, and "Open with  DVDStyler" is deselected. Select the path to DVDStyler.exe, which should be under `...\Program Files\DVDStyler\bin\`. 
9. Click Build. DVDStyler will be opened and will generate two new files in your `games` folder.
10. Download the [latest XK3Y firmware](http://www.mediafire.com/file/5v7sxmpiprqgn23/XK3y-02.01-4.zip/file). Edit the included xkey.cfg and set `MENUISO=N` and `MENUDVD=Y` and save it. You can also set `RESUMELAST=Y` to make it pull up the last played disc first instead of having to select the game every time.
11. (Slims) If your DVD firmware was dumped using a X360 USB Pro or  Jungle Flasher, you may need to set a value for ALTSLIMFW in xkey.cfg as follows:
    - For Slim consoles that say 0225 in Jungle Flasher but are 9504 labeled use the value ALTSLIMFW=7
    - For Slim consoles that say 0401 in Jungle Flasher but are 0225 labeled use the value ALTSLIMFW=8
    - For all other slim consoles, if you get errors when trying to launch a game ISO (like play DVD) try values from 1 to 6.
    - If you do not get errors then do not change the default value of 0.
12. Copy `rootfs`, `uImage`, and `xkey.cfg` to the root of your USB storage device. Safely eject your USB storage device and plug it into your powered-off Xbox 360.
13. Power on the Xbox 360 and let it sit for five minutes. This ensures that the XK3Y has enough time to apply its update.
14. Reboot the Xbox 360. 

From now on, you should be able to press the A button on the "Open  Tray" option to boot into the DVD menu, press A to select the game you  want to play, then press the Guide button, Y to go to the Dashboard, and Y again to eject the tray and start the game.

### Remote (extra hardware)

The XK3Y Remote is an LCD screen that you plug your USB storage  device into and use buttons to select a game. After making your  selection, you can press the A button on the "Open Tray" option on the  dashboard and it will automatically load the game. By default, if the  Remote is receiving power, it will show the XK3Y logo on screen until it starts a connection with the XK3Y main board. If it does not prompt you to select a game, check all cable connections.

### WiFi (extra hardware)

The WiFi dongle is an extra piece of hardware that can be used to  select games using a web browser on another device such as a phone. The  device should also have come with a unique ID for the device, similar to a serial key for it. You will need a USB hub to be able to support both the WiFI dongle and your external USB storage device.

1. Download the [latest XK3Y firmware](http://www.mediafire.com/file/5v7sxmpiprqgn23/XK3y-02.01-4.zip/file). Edit the included xkey.cfg and save after setting the following. The  internet related values are correct if your XK3Y remote says "Network  OK" and an IP is shown under the About section of the System Music  player or Pictures Viewer.
   - `MENUISO=N`
   - `MENUDVD=N`
   - `KEY=YOUR_UNIQUE_ID` (the one provided to you)
   - `SSID=YOUR_WIFI_NETWORK_NAME` (case sensitive)
   - `PSK=YOUR_WIFI_PASSWORD` (leave `#` in front of this line if you have no password or use WEP)
   - `WEP=YOUR_HEX_WEP_KEY` (leave `#` in front of this line if you have no password or use WPA/WPA2)
   - `IP=IP_YOU_WANT_XK3Y_TO_USE` (leave `#` in front of this line unless you have reserved a specific IP address)
   - `NETMASK=SUBNET_MASK_TO_USE` (leave `#` in front of this line unless you need to use a subnet mask other than the default 255.255.255.0)
   - You can also set `RESUMELAST=Y` to make it pull up the last played disc first instead of having to select the game every time.
2. (Slims) If your DVD firmware was dumped using a X360 USB Pro or  Jungle Flasher, you may need to set a value for ALTSLIMFW in xkey.cfg as follows:
   - For Slim consoles that say 0225 in Jungle Flasher but are 9504 labeled use the value ALTSLIMFW=7
   - For Slim consoles that say 0401 in Jungle Flasher but are 0225 labeled use the value ALTSLIMFW=8
   - For all other slim consoles, if you get errors when trying to launch a game ISO (like play DVD) try values from 1 to 6.
   - If you do not get errors then do not change the default value of 0.
3. Copy `rootfs`, `uImage`, and `xkey.cfg` to the root of your USB storage device. Safely eject your USB storage device and plug it into your powered-off Xbox 360.
4. Power on the Xbox 360 and let it sit for five minutes. This ensures that the XK3Y has enough time to apply its update.
5. Reboot the Xbox 360. 

From now on, you should be able to plug your XK3Y's IP address into a web browser (or use a bookmark to it) and select a game and choose  Play. The interface supports touch screens to swipe to change the  selected game. After making your selection, you can press the A button  on the "Open Tray" option on the dashboard and it will automatically  load the game.

## SD Card Recovery

In the event that your SD card randomly corrupts or you accidentally  format a partition, these steps will restore it to factory default. This can also be used to create a new XK3Y SD card from an SD card of any  size. 

1. Download and extract [USB Image Tool](http://www.mediafire.com/file/1ec722ohcvio1h1/usbit_v1_59.zip/file) and the [XK3Y SD Card Image](http://www.mediafire.com/file/5fqybr87uefiled/xkey_110mib_microsd_image_v1_30.7z/file).
2. Plug your SD card into your PC and note the drive letter that it assigns the XKEY partition. 
3. Right click and run USBIT as Administrator. Ensure that it is set to Device Mode in the top left instead of Volume Mode. Select the same  drive letter noted in the previous step in the left hand side. 
4. Select the Restore button and choose `FW1.30.img`. It will flash the image to the SD card.
5. When it is finished, close the program and safely eject the SD card  and insert it into your XK3Y by pressing it in until it clicks and  springs back. You will need to update the XK3Y to the latest firmware,  as it is on the factory firmware version 1.30.

## Tips

- Passthrough mode is essentially disabling the XK3Y to allow you  to play a physical disc. You can enable this by pressing Eject to power  on the console. You can not change between Passthrough and the other  emulation modes without powering off the console.
- To switch discs during a multi-disc game, press Eject on your  console and wait for the "wrong disc" message to appear, then press OK  and select your new ISO as your normally would. If using MenuISO, you  will need to press the physical Eject button instead of pressing a  button to fake eject the disc.
- Hard drives can be of any size, but must be broken into 2TB or smaller partitions if they are above 2TB in size.
- If you have your DVD key, you do not need a dump of your own DVD firmware. You can use a [stock firmware](http://beta.ivc.no/wiki/index.php/Xbox_360_DVD_Drive_Firmware) that matches your model and DVD firmware version.
- After loading the Mixed Media Disc, the "About" folder in the  System Music player or Pictures Viewer will show you some information  about your XK3Y such as the currently installed firmware version and the IP address of the XK3Y if using the WiFi dongle.
- The original team behind XK3Y had admitted to spreading a rumor  that MenuISO wasn't safe online in order to push more Remote and WiFi  device sales. All methods of using XK3Y are safe, so long as you stealth patch your games using ABGX.

## Troubleshooting

- "Mixed Media Disc" doesn't show up
  - Double check that your SATA cables are plugged in to the correct sockets on the XK3Y.
  - Ensure your `firmware.bin` (phat) or `dummy.bin` (slim) is named exactly as shown here.
  - If you spoofed a stock firmware to your DVD key, make sure you  entered your DVD key correctly and set it to spoof to the same firmware  name.
  - Make sure you did not use a flashed firmware as the source or target firmware unless your DVD drive is actually flashed with a custom  firmware
  - Make sure  your USB storage device is formatted as NTFS or ext4.
  - Make sure that your SATA cables are plugged completely in.
  - If your hard drive is not externally powered, it may be drawing too  much electricity from the USB ports. Test a flash drive in the console  or try using a USB Y-splitter cable to get power from two ports at once.
  - Make sure that the ribbon cable is plugged in correctly with the  blue tab facing up on the XK3Y side, and the blue tab facing away from  the console on the USB adapter dongle. Reversing this may have killed  your XK3Y.
- The drive is stuck on "Close Tray" after opening it.
  - Wait at least 1 minute and try rebooting the console. It may have  updated during that bootup, which disables the automatic tray closing  until you reboot.
- The drive instantly goes back to "Open Tray" when you select it.
  - This can be a sign that your USB storage device is incompatible. Try another USB 2.0 or 3.0 hard drive or flash drive. 
  - Make sure that you named your DVD firmware dump `dummy.bin` if it is a slim console, or `firmware.bin` if it is a phat console.
- Blue LED on the XK3Y is flashing
  - This indicates that your SD card is not detected or your `firmware.bin` (phat) or `dummy.bin` (slim) is missing/invalid. Make sure that you push the SD hard in until it clicks and springs into place.
- You get an E64 error.
  - File extensions may be hidden on your PC, so you may be naming your files `firmware.bin.bin` or `dummy.bin.bin` on accident.
  - Complete the section above for SD card recovery. This is likely due to random SD card corruption or a bad firmware update.
  - Your drive firmware needs to be updated to a version after the Mid 2011 update from Microsoft.
  - You selected the wrong Target Firmware type in Jungle Flasher.
- USB storage device not detected
  - Ensure the storage device is formatted to NTFS or ext4.
  - Ensure the `games` folder is present on the storage device. It must be all lowercase.
  - Make sure that your ISO filenames do not start with an underscore. 
  - Make sure that your games are in the games folder.
  - Try downloading a fresh xkey.cfg, as yours may be messed up.
  - Try pulling the hard drive USB plug slightly out of the USB adapter dongle.
- The Xbox 360 reboots every 5 to 10 minutes
  - The XK3Y is not compatible with your Xbox 360. It is unknown what  causes this. The unit will likely work fine in another Xbox 360. 
- Remote screen is stuck on "UPDATE STARTED".
  - Try putting the most recent update files on your storage device.
- DVDMenu / WiFi / Remote won't work
  - Make sure you have the correct option enabled in xkey.cfg, and the other options disabled.
- DVDStyler prompts you to insert a DVD to burn
  - Close out of the program and run XKeyBrew as administrator. 
- Games will not load
  - Try using a different ALTSLIMFW value if you have a slim, or a  different firmware sub-version if you are using a stock firmware file  (such as MS28 vs MS25).
  - XGD3 games will not load on a drive using firmware before the Mid 2011 update from Microsoft.
- Black screen and 1 red LED on your console
  - You are trying to boot up an XGD3 game. You will need to use drive firmware newer than the Mid 2011 update from Microsoft.
- Games crash after a while
  - Your hard drive may be going into sleep mode if it's not actively reading often. You can try editing xkey.cfg and set `HDKEEPALIVE=0` to `HDKEEPALIVE=60`. This will poll the hard drive every 60 seconds to keep it awake.