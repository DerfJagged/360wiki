**The steps on this page are considered risky for your console, as there is a chance you can brick it. Please have someone else mod  your console if you are not experienced in soldering!**

------

# JTAG Hack

------

The JTAG (aka SMC) hack was the first permanent modification that  allows you to run unsigned code, mods, game backups, and homebrew on  your phat console. The hack relies on vulnerabilities in the CB  bootloader, which are only present on dashboards 7371 and lower. If you  are on a higher dashboard, take a look at the [exploit chart](http://i.imgur.com/c5BVZZO.png) and see what hack is right for you.

Note that this guide is a condensation of multiple JTAG guides, most notably the [oblivioncth's Xbox 360 Ultimate Exploit Guide](https://www.se7ensins.com/forums/threads/jtag-rgh-r-jtag-xbox-360-ultimate-exploit-guide.804054/), [Xecuter's JTAG guide](https://web.archive.org/web/20130906233032/http://team-xecuter.com/forums/showthread.php/54423-NAND-X-JTAG-Install-Guides-JTAG-KITS-2-5-8-E79), [M AzeeM K's Alternate JTAG guide](https://web.archive.org/web/20120527145714/http://team-xecuter.com/forums/showthread.php?t=55189), [X-Splinter's Matrix USB Flasher guide](http://www.360-hq.com/xbox-tutorials-162.html), as well as personal experience.

While it's recommended to read through this guide in its entirety, a video guide for JTAG can be found on [MrMario2011's channel](https://youtu.be/v9eAG3WSmU4?list=PL1CadovfabPskGb2Ur4kBGzD5s7DzQw5I).

**Note that JTAG does not support Slim/E motherboards.**

------

## Requirements

Below are the requirements to JTAG your Xbox 360. It's recommended to read ahead and choose the NAND dumping method and JTAG-specific wiring  method that's right for you, as you will need more equipment or a NAND  programmer depending on the method you choose.

To check that your console is exploitable, you must have:

1. A fat console (Xenon, Zephyr, Falcon, Opus, or Jasper model). You can look at the back of your console and check 

   this chart

    to find out what model you have. 

   - If you have a Jasper, determine whether if there is Memory Unit  built in. If it has 214MB of storage, it's a 256MB NAND. If it has 451MB of storage, it is a 512MB NAND.

2. On 

   dashboard 7371 or lower

   . If you are on the  original blades dashboard, that is sufficient. Otherwise, you can check  this by navigating to Settings > Console Settings > Hover over  System Info. Your dashboard version will be shown in the top right in  the form 2.0.xxxxx.0, where xxxxx is your dashboard version.

   - If it is on dashboard 7371, the system may not be JTAGable. You can only find out by dumping your NAND.

3. Soldering experience. The Xbox 360 is not a good place to learn to  solder. Regardless of which dumping method you choose, you will need a  soldering iron, solder, and flux.

## Reading your NAND

There are four different methods to reading your NAND chip: Nand-X,  JR Programmer, Matrix USB NAND Flasher, or a LPT cable. Consider the  pros and cons below and choose the method that's right for you. It's  recommended to avoid the LPT cable method as it is very difficult and  slow.

| Method                                                       | Pros                                                         | Cons                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **[NAND-X](https://360.consolemods.org/hardware/programmers/nandx.html)** | - Reads NANDs the fastest: 2-8 minutes - Can also program Glitch Chips | - More expensive than JR Programmer                          |
| **[JR-Programmer](https://360.consolemods.org/hardware/programmers/jrprogrammer.html)** | - Reads NANDs faster than Matrix: 3-15 minutes - Can also program Glitch Chips | - More expensive than Matrix Flasher                         |
| **[Matrix USB NAND Flasher](https://360.consolemods.org/hardware/programmers/matrix.html)** | - Cheapest option                                            | - Reads NANDs in 7-26 minutes                                |
| [ProgSkeet](https://360.consolemods.org/hardware/programmers/progskeet.html) |                                                              |                                                              |
| **[LPT Cable](https://360.consolemods.org/hardware/programmers/lpt.html)** | - Old school DIY experience                                  | **- Much more difficult** - Can't be used for programming Glitch Chips - Takes ~30 minutes for a NAND read, ~150 minutes for large 256/512 NANDs |

## JTAG-Specific Wiring

Choose the guide that pertains to you:

### [Xenon Method](https://360.consolemods.org/modguide/jtag-smc/xenon.html)

- This is the only method for Xenon motherboards. Do not use it if you have a non-Xenon motherboard.

### [Boxxdr Method](https://360.consolemods.org/modguide/jtag-smc/boxxdr.html)

- This method is for Zephyr, Opus, Falcon, or Jasper motherboards. This method may disable 5.1 audio output.

### [Boxxdr Method + Open_Tray](https://360.consolemods.org/modguide/jtag-smc/boxxdropentray.html)

- Use this method if the Boxxdr method doesn't boot, you receive E79  errors, or you have issues with HDMI. This method may cause your DVD  drive to eject on bootup. Also, your console will reboot instead of  shutting down if you turn off the console while a controller is charging via USB.

## Creating an XeBuild Image

You should now be able to turn on your Xbox 360 and boot into XeLL  and see your CPU key. With that CPU key, we can build an XeBuild image,  which is a NAND dump built specifically for your console. Ensure that  you have written down your CPU key and have powered off your console.

1. Open JRunner and select "..." next to the Source File field and  select your nanddump1.bin if not already selected. In the upper right  corner of the window, select the dashboard version you chose for the  patched dump that you wrote to the motherboard and make sure that the  "Jtag" radio button is selected, and if you have a non-Xenon console the `Aud_clamp?` box has a check in it.
2. Select the "Create Image" button in the top left of the window.  It may prompt you for your motherboard model, select it and click OK. It will build your image and save it to a numbered folder within the  JRunner directory as updflash.bin.
   - If you get an error during this step, see the troubleshooting section below.
3. Copy updflash.bin to a FAT32 formatted USB storage device and  plug it into your powered-off console. Turn on your console and it will  boot into XeLL and begin flashing your NAND. Once it has finished, it  will power off your console. Turn it back on, and it should boot to the  Microsoft dashboard, which is an indication that you've successfully  hacked your console. You're now free to install XEXmenu (instructions in section below).

- You may want to leave your Xbox 360 disassembled so that you can:
  - ...[disable the eFuse-blowing circuit](https://360.consolemods.org/repairguide/disableefuseburn.html) so that you can't accidentally install official updates on your console.
  - ...check what it's running temperatures are so that you can judge whether it'd be a good idea to use [cooling mods](https://360.consolemods.org/repairguide/improvecooling.html) to avoid overheating issues. This is recommended for all fat consoles, particularly Xenons.

## Installing XeXMenu

1. Plug a flash drive into your Xbox 360 and navigate to Console  Settings > Storage. Select the flash drive and allow it to format the flash drive as a system drive. 
2. Extract the `CODE9999` folder from the [XeXMenu 1.2 rar](http://www.mediafire.com/file/7orm0jrkncrzo1w/xexmenu12live.rar/file) to your Desktop.
3. Plug the flash drive into your PC. Open [Xplorer360](http://www.mediafire.com/file/zb6ic4036c6nmpg/Xplorer360.exe/file) and select Drive > Open > Harddrive or Memcard. On the left-hand  side, select Partition 3, then right-click the Content folder, select  "New Folder", and name it `0000000000000000` (16 zeroes). Open the new folder, then drag the `CODE9999` folder into it.
4. Select Drive > Close, then close Xplorer360. Safely eject your flash drive and plug it into your Xbox 360. Navigate to the Demos  section of your dashboard, and it should list XeXMenu there. Select it  to launch it. 
   - You can install XeXMenu to your hard drive by going to Console  Settings > Storage, and copying it from your flash drive to the hard  drive.

From here, you can install any homebrew or mods that you want. See [this page](https://360.consolemods.org/modguide/recommendedsetup.html) for a list of recommended modifications and applications to install.

If you are on dashboard 7371: If the console manufacture date on the back is BEFORE 6-1-2009 then it is JTAGable, otherwise it is **not**. If you want to be sure that it is exploitable, a NAND dump will be able to tell you what CB (bootloader) version your console is on, as the CBs on some consoles running 7371 differ. The following [chart](http://i.imgur.com/On7Sazo.jpg) details which bootloaders are exploitable by the JTAG/SMC exploit, so  make sure this matches if you wish to double-check via NAND dump.

