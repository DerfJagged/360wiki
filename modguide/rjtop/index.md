**The steps on this page are considered risky for your console, as there is a chance you can brick it. Please have someone else mod  your console if you are not experienced in soldering!**

------

# R-JTOP Hack

------

The R-JTOP hack was the first *[open source](https://github.com/DrSchottky/R-JTOP)* modification that allows you to run unsigned code, mods, game backups,  and homebrew on phat consoles. The hack relies on vulnerabilities in  dashboard 15572 and later. It is essentially an open source  implementation of the R-JTAG hack and achieves the same result through a different method. This should only be used if your console doesn't work well with RGH 1.2 or RGH 2.0. It is useful, as it can be done more  cheaply than an R-JTAG, but it is lesser used and therefore you will not receive much support if you run into issues. It's recommended to take a look at the [exploit chart](http://i.imgur.com/c5BVZZO.png) and see what hack is recommended for your console.

**Note that R-JTOP does not support Slim/E motherboards.**

------

## Requirements

Below are the requirements to R-JTOP your Xbox 360. It's recommended  to read ahead and choose the NAND dumping method and R-JTOP specific  wiring that's right for you, as you will need a NAND programmer and  potentially more equipment depending on which methods you choose.

To check that your console is exploitable, it must meet the following conditions. It must be:

1. A fat console (Xenon, Zephyr, Falcon, Opus

   untested

   , or Jasper model). You can look at the back of your console and check 

   this chart

    to find out what model you have. 

   - If you have a Jasper, determine whether if there is Memory Unit  built in. If it has 214MB of storage, it's a 256MB NAND. If it has 451MB of storage, it is a 512MB NAND.

2. On 

   dashboard 15572 or higher

   . You can check this by navigating to Settings > Console Settings > Hover over System  Info. Your dashboard version will be shown in the top right in the form  2.0.xxxxx.0, where xxxxx is your dashboard version.

   - If it is on a lower dashboard, you can update it to the latest.

3. Soldering experience. The Xbox 360 is not a good place to learn to  solder. Regardless of which dumping method you choose, you will need a  soldering iron, solder, and flux.

You will also need:

- A NAND reader that can program glitch chips (JR Programmer, NAND-X, or two Matrix USB NAND Flashers)
- A xc2c64a based glitch chip (CoolRunner 3, CoolRunner rev C/D, or Matrix Glitcher V1/V3) or the ability to compile [the source](https://github.com/DrSchottky/R-JTOP) for another chip
- [R-JTOP timing files](https://drive.google.com/file/d/17xM32rmkUppnJn4HmbqiPMApD74ucbm3/view)
- [J-Runner](https://www.modconsoles.fr/hitcounter/counter.php?file=JRunner_V0.5.zip)
- Equipment listed in the relevant R-JTOP specific wiring below

## Dumping your NAND

There are three different methods to making a dump of your NAND chip: Nand-X, JR Programmer, or a Matrix USB NAND Flasher. While an LPT cable can be used, they cannot be used to flash glitch chips, so they will  not be covered here as you will need one of the other devices anyway.  Consider the pros and cons below and choose the method that's right for  you. Once you have decided on a method, select the guide below and  follow it to get a NAND dump, patch the dump, and write the dump to your motherboard. Once you've completed one of the pages below, continue to  the next section.

| Method                                                       | Pros                                                         | Cons                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **[Nand-X](https://360.consolemods.org/hardware/programmers/nandx.html)** | *- Dumps NAND faster than JR Programmer; 2-8 minutes* **- Can also program RGH glitchchips** | - More expensive than JR Programmer                          |
| **[JR Programmer](https://360.consolemods.org/hardware/programmers/jrprogrammer.html)** | *- Cheaper than Nand-X* **- Can also program RGH glitchchips** | - More expensive than Matrix                                 |
| **[Matrix USB NAND Flasher](https://360.consolemods.org/hardware/programmers/matrix.html)** | *- Cheapest option* **- Dumps NAND at same speed as NAND-X** | - Can't be used for programming RGH glitchchips unless you modify it per the tutorial on it's page. |

## Programming the Glitch Chip

1. Connect the glitch chip to your programmer.
2. Open J-Runner and navigate to Advanced > Custom Nand/CR functions > xsvf, and choose the file corresponding to your console model.
3. Click RUN and it will flash the glitch chip. If it fails, check if  there is a switch on the programmer to set it into programming (or  "PRG") mode.

## R-JTOP Specific Wiring

The wiring for R-JTOP is the same as the wiring for the JTAG hack. Choose the guide that pertains to you:

### [Xenon Method](https://360.consolemods.org/modguide/jtag-smc/xenon.html)

- This is the only method for Xenon motherboards. Do not use it if you have a non-Xenon motherboard.

### [Boxxdr Method](https://360.consolemods.org/modguide/jtag-smc/boxxdr.html)

- This method is for Zephyr, Opus, Falcon, or Jasper motherboards. This method may disable 5.1 audio output.

### [Boxxdr Method + Open_Tray](https://360.consolemods.org/modguide/jtag-smc/boxxdropentray.html)

- Use this method if the Boxxdr method doesn't boot, you receive E79  errors, or you have issues with HDMI. This method may cause your DVD  drive to eject on bootup. Also, your console will reboot instead of  shutting down if you turn off the console while a controller is charging via USB.

## Glitch Chip Wiring

The wiring for R-JTOP is the same as the wiring for RGH 1.2.

### [CoolRunner rev C/D](https://web.archive.org/web/20160118143255im_/http://s15.postimg.org/avcw9muuj/coolrunnerrevcrgh12.jpg)

### [CoolRunner 3 Lite](https://web.archive.org/web/20161015093429im_/https://s1.postimg.org/p2lvareov/cr3litergh12.jpg)

### [Matrix Glitcher](https://web.archive.org/web/20170711063146im_/http://s28.postimg.org/j48ozimcd/matrixglitcherrgh12diagram.jpg)

### [Squirt](https://web.archive.org/web/20160118143256im_/http://s12.postimg.org/77xf0z52l/squirtrgh12installdiagram.jpg)

### [X360 ACE](https://web.archive.org/web/20161015093417im_/https://s4.postimg.org/gtnd5nknx/x360acergh12phatinstalldiagram.png)

- Note that the X360 ACE requires you to compile timing files for it  and needs a 22K resistor soldered on the PLL line. It may require  removal of a resistor or diode on the chip itself depending on the  version.

## Creating an XeBuild Image

You should now be able to turn on your Xbox 360 and boot into XeLL  and see your CPU key. With that CPU key, we can build an XeBuild image,  which is a NAND dump built specifically for your console. Ensure that  you have written down your CPU key and have powered off your console.

1. Open JRunner and select "..." next to the Source File field and  select your nanddump1.bin if not already selected. In the upper right  corner of the window, select the dashboard version you chose for the  patched dump that you wrote to the motherboard and make sure that the  "Jtag" radio button is selected, the `R-jtag` box has a check in it, and if you have a non-Xenon console, the `Aud_clamp?` box has a check in it.
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