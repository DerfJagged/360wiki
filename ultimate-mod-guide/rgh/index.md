**The steps on this page are considered risky for your console, as there is a chance you can brick it. Please have someone else mod  your console if you are not experienced in soldering!**

------

# Reset Glitch Hack (RGH)

------

Reset Glitch Hack (RGH) is allows you to run unsigned code, mods,  game backups, and homebrew. The hack relies on a vulnerability in the  hardware found by GliGli that is triggered by sending a reset pulse to  the processor at a specific moment, resulting in a glitch that causes  the hash check to be valid no matter what you have flashed in place of  the stock bootloader. Since this is a glitch, the timing of when and how long the pulse should be sent is dependent on the console and it may  take many tries until it "glitches" and boots.

The RGH version are as follows: 

- RGH1 is for Phat consoles with dashboard 14699 and lower. It uses CPU_PLL_BYPASS to slow down the CPU.
- RGH2 is for Slims (but also works for Non-Xenon Phats), which uses  I2C slowdown instead of PLL slowdown, and works on any dashboard.  However, it is considered more difficult to tune, and less consistent.
- RGH1.2 combines RGH1 like PLL slowdown with RGH2 software to allow reliable glitching of Phat consoles after 14699 dashboard.
- S-RGH (Speeded-Up RGH) is a tweaked and better version of RGH2 which is far more consistent and quick.

------

## Requirements

Below are the requirements to RGH your Xbox 360. It's recommended to  read ahead and choose the NAND reading method and glitchchip specific  wiring method that's right for you, as you will need a NAND programmer  and potentially more equipment depending on which methods you choose. 

1. Check hardware compatibility. You can use [Octal's Wizard](https://identify.octalsconsoleshop.com) to find whether your board is RGHable or not.
2. Phat Consoles: Check dashboard compatibility. All dashboards are  exploitable, but if you have a Phat console the method you should use  will depend on your dashboard version.
3. Soldering experience. The Xbox 360 is not a good place to learn  to solder. Regardless of which reading method you choose, you will need a soldering iron, solder, and flux (MG 835 recommended)

## Reading your NAND

There are four different methods to reading your NAND chip: Nand-X,  JR Programmer, Matrix USB NAND Flasher, or a LPT cable. However, the  Corona v2/v4/v6 requires that you use the SD card method. Consider the  pros and cons below and choose the method that's right for you. It's  recommended to avoid the LPT cable method as it is very difficult, slow, and you will need a second device to program your Glitch Chip.

| Method                                                       | Pros                                                         | Cons                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **[NAND-X](https://www.reddit.com/r/360hacks/wiki/rgh/jr_programmer)** | - Reads NANDs the fastest: 2-8 minutes - Can also program Glitch Chips | - More expensive than JR Programmer                          |
| **[JR-Programmer](https://www.reddit.com/r/360hacks/wiki/rgh/jr_programmer)** | - Reads NANDs faster than Matrix: 3-15 minutes - Can also program Glitch Chips | - More expensive than Matrix Flasher                         |
| **[Matrix USB NAND Flasher](https://www.reddit.com/r/360hacks/wiki/rgh/matrix)** | - Cheapest option                                            | - Reads NANDs in 7-26 minutes - Can't be used for programming RGH Glitch Chips [unless you modify it](https://www.reddit.com/r/360hacks/wiki/programmer/matrix) |
| **[LPT Cable](https://www.reddit.com/r/360hacks/wiki/rgh/lpt)** | - Old school DIY experience                                  | **- Much more difficult** - Can't be used for programming Glitch Chips - Takes ~30 minutes for a NAND read, ~150 minutes for large 256/512 NANDs |
| **[SD Card](https://www.reddit.com/r/360hacks/wiki/rgh/sd_card)** | - The **only** option for Corona v2/v4/v6                    | - You still need a NAND-X or JR-Programmer to Program Glitch Chips |

## RGH Phat Wiring

### [RGH1](https://www.reddit.com/r/360hacks/wiki/rgh/rgh1)

### [RGH1.2](https://www.reddit.com/r/360hacks/wiki/rgh/rgh12)

### [RGH2](https://www.reddit.com/r/360hacks/wiki/rgh/rgh2)

### [S-RGH](https://www.reddit.com/r/360hacks/wiki/rgh/s-rgh)

### [Xenon RGH](placeholder)

## RGH Slim Wiring

### [RGH2](https://www.reddit.com/r/360hacks/wiki/rgh/rgh2)

### [S-RGH](https://www.reddit.com/r/360hacks/wiki/rgh/s-rgh)

## Installing XeXMenu

1. Plug a flash drive into your Xbox 360 and navigate to Console  Settings > Storage. Select the flash drive and allow it to format the flash drive as a system drive. 
2. Extract the `CODE9999` folder from the [XeXMenu 1.2 rar](http://www.mediafire.com/file/7orm0jrkncrzo1w/xexmenu12live.rar/file) to your Desktop.
3. Plug the flash drive into your PC. Open [Xplorer360](http://www.mediafire.com/file/zb6ic4036c6nmpg/Xplorer360.exe/file) and select Drive > Open > Harddrive or Memcard. On the left-hand  side, select Partition 3, then right-click the Content folder, select  "New Folder", and name it `0000000000000000` (16 zeroes). Open the new folder, then drag the `CODE9999` folder into it.
4. Select Drive > Close, then close Xplorer360. Safely eject your flash drive and plug it into your Xbox 360. Navigate to the Demos  section of your dashboard, and it should list XeXMenu there. Select it  to launch it. 
   - You can install XeXMenu to your hard drive by going to Console  Settings > Storage, and copying it from your flash drive to the hard  drive.

From here, you can install any homebrew or mods that you want. See [this page](https://www.reddit.com/r/360hacks/wiki/recommendations) for a list of recommended modifications and applications to install.

- Recommended chips for RGH
  - Xenon/Zephyr/Trinity/Corona - Ace v3
  - Falcon - Revc or Matrixx
  - Jasper/Kronos - Revc

