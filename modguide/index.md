## Why Mod your console

There's loads of features described below that speak for themselves as to why you would want to, so read on.

## Identifying your console

You'll need to gather some information about your console before you begin in order to determine what mods you will be doing.

[Identifying your Model](https://360.consolemods.org/modguide/identifyconsole/model.html)

[Identifying your Motherboard](https://360.consolemods.org/modguide/identifyconsole/motherboard.html)

[Identifying your Disk Drive](https://360.consolemods.org/modguide/identifyconsole/dvddrive.html)

[Identifying your Dashboard](https://360.consolemods.org/modguide/identifyconsole/dashboard.html)

## Choosing your mods

Now that you've identified important information about your console, it's time to decide on what mods you'll do.

##### [Disk Drive Flashing](https://360.consolemods.org/modguide/odd/oddflashing.html)

Flashing an Xbox 360 DVD drive involves overwriting the DVD drive  firmware with a custom firmware (usually LT3) that allows the running of burned DVDs. With this you can play some game mods, so long as they are running signed XEX files, as this mod does not allow running unsigned code by itself. This can be done with as little as a USB device, but may range in materials and difficulty, up to and including drilling into a chip with a very small dremel tool (known  as the "kamikaze" hack). This allows you to play game backups and some game mods on your Xbox 360. You can play on Xbox Live with relatively low risk of being banned as long as you stealth patch your games. This can be done with any Phat model drive and most Slim and E consoles. Refer to the tutorial for more information.

##### [Disk Drive Emulator](https://360.consolemods.org/modguide/odes/index.html)

An Optical Drive Emulator is a device that allows you to run game backups on a Xbox 360, without requiring a jailbroken  console or custom dashboard. The majority of consoles are compatible, with some newer slims requiring the console to be RGH exploited to function correctly, and the newest motherboards (Winchester) not being compatible. Please refer to your ODE of choice for compatibility information, functionality, and safety on Xbox Live.

##### Unsigned Code Mods

These are where the system is modified to run unsigned code. This includes [RGH](https://360.consolemods.org/modguide/rgh/index.html)/[JTAG/SMC](https://360.consolemods.org/modguide/jtag-smc/index.html)/[R-JTAG](https://360.consolemods.org/modguide/rjtag/index.html)/[R-JTOP](https://360.consolemods.org/modguide/rjtop/index.html). Often, people will install a freeboot image to NAND, some essential utilities, a custom dashboard, and homebrew. These mods will allow you to play modified game backups and do much much more with your console. Refer to the following chart to determine which you should do:

![exploitchart](/media/guides/unsignedcodemods/exploitchart.png)

From here you can: 

| Add Custom Boot animations | Run Linux | [Use a Stealth Server to Play on Xbox Live](https://360.consolemods.org/modguide/xboxlive/stealth.html) |      |      |
| -------------------------- | --------- | ------------------------------------------------------------ | ---- | ---- |
|                            |           | Use [LiNK](https://360.consolemods.org/software/networking/link.html) or [XLink Kai](https://360.consolemods.org/software/networking/kai.html) to play online over emulated System Link |      |      |
|                            |           |                                                              |      |      |
|                            |           |                                                              |      |      |



##### [King Kong Shader Exploit](kkexploit.md)

This is an older exploit only available on very old kernel/dashboard versions and is only useful to run Linux and cannot modify the Xbox 360 Operating System in any functionally useful manner. Aside from running Linux on your own console, this exploit is entirely useless and only listed for historic reasons.

#### Congratulations! You have successfully modded your console after following the respective tutorials! You might be interested in moving forward from here by: 

| Installing Games/Apps/DLC | Playing on Xbox Live |      |      |      |
| ------------------------- | -------------------- | ---- | ---- | ---- |
|                           |                      |      |      |      |
|                           |                      |      |      |      |
|                           |                      |      |      |      |



## Installing Games, Apps, and DLC

## Playing on Xbox Live

## Custom Boot Animations

## [Modding Gamesaves](savegamemodding/index.md)

## [Modding Games](gamemodding/index.md)

## Working with the Filesystem

## Introduction to XeLL

## Backing up Games

## Installing the Hacked Compatibility Files

## Dumping NAND

## Updating system

[Installing Linux](development/installlinux.md)

# Recommended Setup

------

This page will lead you through the basic setup of your console and [/u/Derf_Jagged](https://www.reddit.com/u/Derf_Jagged)'s recommendations of what to install. This list assumes that you have a freshly JTAG/RGH exploited console. 

------

1. If you have an early phat model, check the [cooling improvements page](https://360.consolemods.org/repairguide/improvecooling.html) for ideas to lower your system temperatures. 
2. [Disable the eFuse Burning Circuit](https://360.consolemods.org/repairguide/disableefuseburn.html) so that you never have to worry about accidentally updating your system with an official update.
3. [Save a backup dump of your NAND and KV info](https://360.consolemods.org/modguide/nanddump/index.html) to somewhere safe if you don't already have one. 
4. [Install XeXmenu](https://360.consolemods.org/software/utilities/xexmenu.html). 
5. [Install Aurora](https://360.consolemods.org/software/dashboards/aurora.html) and set paths to scan for games. Keep XeXmenu installed as a backup.
6. Install DashLaunch and:
   - Set target temperatures for fans to 60°C for CPU/GPU/EDRAM.
   - Set `default` to your Aurora XEX so it loads Aurora on bootup.
   - Set `X` to boot to the Microsoft dashboard XEX (located in flash). (Unnecessary, RB will bring you to dash by default.)
   - [Block XBL](https://360.consolemods.org/modguide/preventbans.html) if you don't plan on playing online.
7. [Modify your bootanim](https://360.consolemods.org/modguide/custombootanims.html) if you want to customize your boot up animation and sound.
8. Install apps:
   - For emulating non-Xbox games: [Various Emulators](https://360.consolemods.org/software/emulators/index.html)
   - [For activating locked DLC or games](https://360.consolemods.org/modguide/gamebackups/gamepatching.html)
9. If you want to mod games, install [Xbox Neighborhood](https://360.consolemods.org/software/networking/xboxneighborhood.html) and see [this page for specific game mods](https://360.consolemods.org/modguide/gamemodding/index.html).
10. Set up [LiNK](https://360.consolemods.org/software/networking/link.html) and/or [XLink Kai](https://360.consolemods.org/software/networking/kai.html) for system link play.



## Credits

Orpheus for being super informative.