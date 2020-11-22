# Frequently Asked Questions

**Q. Why did you make this wiki? There's other wikis out there.**

A. This wiki is the wiki to outwiki all wikis. The features provided by GitHub allow this to be so versatile, open, and community-built wiki for the Xbox scene. And **THAT**'s cool.

Here you'll find most of the info you'll need to start using homebrew on your Xbox 360. If a question isn't here that  you feel should be, please submit an issue.

------

## FAQ

**Q. What is the point of an RGH/JTAG?**

A. The intent of an RGH/JTAG is to allow execution of homebrew software on the Xbox 360. Custom firmware will allow you to:

- Play backups of Xbox 360 / Xbox / DVDs natively and region free, even on non backwards-compatible models.
- Emulate retro games with [RetroArch](emulators-ports/retroarch.md) or [stand-alone emulators](emulators-ports/index,md).
- [Rip Xbox 360 / Xbox / DVD discs](ultimate-mod-guide/backupgames.md) to your hard drive.
- [Mod games offline or online](ultimate-mod-guide/gamemodding/index.md).
- [Convert your console into to a developer console (devkit).](development/convertdevkitrgloader.md)
- Play games stored on an external drive, or even games stored on [a SMB enabled device on your network](Software/Utilities/connectx.md).
- [Unban your console](preservation-repair/Unbanconsole.md).
- Change the [boot up animation and sound](ultimate-mod-guide/custombootanims.md).
- [Use Linux](development/installlinux.md).
- Create and use cheats for games
- Put a completely new DVD drive into your console with your  motherboard without having to take the drive apart (if you have the DVD  key).
- [Install homebrew games and apps](ultimate-mod-guide/gamebackups/installgamesappsdlc.md).

**Q. Does it matter what model of Xbox 360 I have, or can all models be exploited?**

A. All models can be exploited in one way or another *except* the latest version (Winchester motherboards). You can find more information [here](ultimate-mod-guide/identifyconsole/motherboard.md).

**Q. Does it matter what dashboard version I'm on?**

A. No, you can hack any dashboard, though earlier dashboards may be  able to use easier / more reliable hacks. You can find more information [here](ultimate-mod-guide/identifyconsole/dashboard.md).

**Q. Can you hack a console without soldering?**

A. JTAG/RGH require soldering. It is **highly**  recommended to learn how to solder very well and practice on junk  electronics before trying to hack an Xbox 360 as it has rather small and crowded solder points. Drive flashing to run backups of your games does not require soldering.

**Q. What equipment do you recommend for soldering?**

A. - A soldering iron with a controllable temperature knob, the higher the wattage the faster it will heat up - Leaded solder (*not* lead free) - No-clean liquid flux (Kester 951 preferably)  - 30AWG solid core wire, preferably shielded (28AWG is a more expensive but easier to work with) - Wire strippers that can handle 30AWG wires - Flush cutters (any wire cutter will do, but flush ones are more precise) - A brass wool tip cleaner - Isopropyl alcohol (90% higher) - Cotton swabs

**Q. What should I do if I ripped off a soldering pad?**

A. Look online for an alternate point to solder onto. Practice more on junk electronics before attempting to continue.

**Q. Can you hack consoles without buying extra hardware?**

A. Unless you pay someone else to do it for you, no.

**Q. What should I install on my RGH/JTAG?**

A. See [this list](Software/index.md) of recommended software to install.

**Q. Can I play online safely?**

A. In short, no. RGH/JTAGs get banned within hours unless you use a (usually) paid service such as NiNJA or xbOnline to keep you from  getting banned. Xbox 360's with flashed drives or ODEs are susceptible  to a ban when playing online, with ban waves occurring in the past. With Microsoft slowing the pace of updates, it may be safer to play online  with flashed drives or ODEs at this point.

**Q. Can I dual boot an official NAND and a modded NAND to go online safely?**

A. Yes. If you install a TX DemoN, Squirt Dual NAND, Matrix Trident,  or "NAND Sandwich mod", you will have a second (or third with Trident)  NAND to boot from. This allows you to have one unmodified NAND for safe  online play, and a second modified NAND for offline play.

**Q. Can I update my games without going on XBL?**

A. Yes. Aurora can download updates from XboxUnity, which hosts game  updates. They can also be downloaded from other sources and applied manually as well.

**Q. Can I use the Internet or apps (such as Netflix) on my RGH/JTAG without connecting to XBL?**

A. No. All apps, other than [Netflix](Software/Apps/Netflix.md), require an Xbox Live connection.

**Q. Do I need my DVD drive connected to boot the Xbox?**

A. No, it will boot up properly without a DVD drive, however, the power button LEDs will blink unless you [apply a fix](preservation-repair/removeodd.md).

**Q. What is the "Kronos/Kronus" model Xbox 360?**

A. The Kronos is a revision of the Jasper motherboard which includes a different GPU, 65nm (versus 80nm) eDRAM which reduces its likelihood  for the E74 error, a new RF module, small component changes like  capacitors, no copper pipe on the GPU heatsink. They are treated the  same as Jaspers all around, so they really aren't considered a model on  its own.

**Q. What are the directories on my Xbox 360?**

A. See [this page](ultimate-mod-guide/filesystembasics.md) for information on what each directory contains.

**Q. What is an ODE (XK3Y / Wasabi360 / Boxzii / X360DOCK)?**

A. An Optical Drive Emulator is a device that allows you to run Xbox  and Xbox 360 game backups on an Xbox 360, without requiring an RGH/JTAG. Like with [drive flashing](ultimate-mod-guide/oddflashing.md), all phat consoles support ODEs, and all but the latest model (Winchester) slim consoles can have an ODE. See [this page](ultimate-mod-guide/identifyconsole/motherboard.md) for more details on model compatibility.

**Q. Where can I find information about XGD3 games?**

A. [This page](techinfo/fs/xdg3.md) lists all of the XGD3 games and compatible DVD burners.

**Q. Can RGH/JTAG exploited consoles play games burned to a DVD?**

A. No. This would require a flashed disc drive.

**Q. How do I play games from external?**

A. Add a path to your external hard drive for FSD/Aurora to scan games from. 

**Q. What is the AUD_CLAMP hack for JTAG installs?**

A. The JTAG hack requires an I/O line during bootup. On non-Xenon  consoles, there are no unused I/O lines. Originally, a line on the ROL  board (ARGON_DATA) was used, but this would cause issues with a spastic  ROL and E79 issues for Zephyr motherboards. On the HANA chip, DB1F1 was  later used, but this sometimes would result in boot failures and  resetting video settings. Finally, two data lines — AUD_CLAMP (mutes  analog audio) and TRAY_OPEN (controls DVD ejection) — were decided to be the de facto lines to use for JTAG installs. Using AUD_CLAMP can cause  5.1 audio output to be disabled, while TRAY_OPEN can cause the DVD tray  to eject on boot. 

**Q. Why is there no RGH1/RGH2/R-JTAG option for Xenon?**

A. RGH1/R-JTAG/R-JTOP does work, but is unreliable due to the CPU having issues with deassertion of `CPU_PLL_BYPASS`. Because of this, an R-JTAG board was never created for Xenon.. RGH2  relies on the HANA chip for operation, which isn't present on Xenon  motherboards.

**Q. What is RROD?**

A. In general, Red Ring of Death (RROD) is caused by the CPU/GPU/RAM  not making proper contact with the motherboard or are defective. One  theory is that due to the solder balls being lead free and - partially  due to cheap thermal paste - they get too hot and stress crack and cause an improper connection. This theory is demonstrated in [a write-up by bunnie](https://www.bunniestudios.com/blog/?p=223). There can be many different causes of a RROD, as documented on [our error codes page](preservation-repair/errorcodes/index.md), and sometimes the part in question may need complete replacement.

**Q. Should I do the towel trick / bolt mod to fix RROD?**

A. **NO**. The towel trick works by suffocating your  console to heat it up enough to restore the faulting part. This can  cause damage to other components on the board and is bad for your  console in general, and is almost always a temporary fix. The bolt mod  is a fix that was commonly done by GameStop and people early on which  basically replaces the X-clamps with bolts to tighten the heatsinks down more. However, this gives uneven pressure and will end up warping your  board and making the problem worse.

**Q. What is a reball/reflow?**

A. Reballing and reflowing are home remedies for fixing RROD.  Reflowing is considered a temporary fix, which involves heating up the  affected component to re-melt all of the solder balls at once so each  one flows back into place. If you apply [cooling improvements](preservation-repair/improvecooling.md) and monitor temperatures, this can be a more permanent fix. Reballing,  on the other hand, is a permanent fix which replaces all of the solder  balls with leaded solder. Reballing requires a professional rework  station to melt all of the solder balls, remove the affected component,  place new solder balls down, and reattach the component. However,  sometimes the component itself (CPU/GPU/RAM) is faulty and a reball will not permanently fix it.

**Q. What is a Lamprey? Can they make devkits?**

A. A Lamprey is an official Microsoft device that is used as a jig  for a SPI. Essentially, it can do what a hardware flasher like Nand-X or JR Programmer can do. It cannot create devkits.

**Q. How can I play multi-disc games?**

A. 

- For games that have one installation disc and one "play" disc,  such as Grand Theft Auto V, Call of Duty: Advanced Warfare, Halo 4, or  Battlefield 4; you can manually install the installation disc by  extracting the ISO and copying the "content" folder onto the root of  your Xbox 360 HDD, which will merge it into the existing content folder.
- For games that have two "play" discs, such as Rage, Dead Space 2, Dead Space 3, or Max Payne 3; it will ask you to swap discs mid-game,  FreeStyle Dash or Aurora can handle the disc swapping if you place the  extracted games into folders as follows: 
  - `...\games\<Game Name>\Disc1\`
  - `...\games\<Game Name>\Disc2\`
- *Wolfenstein: The New Order* is a special case which needs Disc 1 run as a GOD game, and discs 2 through 4 in separate disc folders.
- *Watch Dogs* is a special case in which you need to extract the contents of Disc 2 into a folder, then extract the contents of the `installation1` and `installation2` folders from Disc 1 into the folder and rename `game.xex` to `default.xex`.

------

## Definitions

| Term                                 | Definition                                                   |
| ------------------------------------ | ------------------------------------------------------------ |
| **AntiPiracy 2.5/2.6 (AP25 / AP26)** | A protection built into Xbox 360 games to prevent flashed DVD drives from running newer games. |
| **eFuse**                            | A once-writable bit embedded in the CPU. Microsoft  used them to control the system firmware version, making it impossible  to normally downgrade. |
| **Phat**                             | A first generation Xbox is known as a "phat" or "fat" console, as opposed to a "slim" console. |
| **RGH Exploit**                      | Reset Glitch Hack. The successor to the JTAG hack, it allows for maximum control over your console and the ability to run  homebrew. |
| **JTAG Exploit**                     | An exploit that allows maximum control over your  console and the ability to run homebrew. JTAG is an electronics  standard, standing for Joint Test Action Group. |
| **ODE**                              | Optical Drive Emulator. It's a device that acts as a disc drive and can run Xbox and Xbox 360 game backups. |
| **ODDE**                             | Optical Disc Drive Emulator. Another name for an ODE.        |
| **Programmer**                       | Programmer devices are used to read/write NAND dumps  on your Xbox 360 and to program modchips with timing files to better  glitch your console in a RGH install. They are essential in both RGH and JTAG installs, unless you use a LPT cable. |
| **QSB**                              | Quick Solder Board. It's a small circuit board that makes it easier to solder items together. |
| **NAND**                             | An Xbox 360's NAND chip, which the OS resides on.            |
| **GOD**                              | Games on Demand. Digital games downloaded from the Xbox Live Marketplace. |
| **KV**                               | Key Vault. It holds your console specific data such  as your DVD key, CPU Key, and a unique identifier for your console on  Xbox Live. If Microsoft bans you, your key vault is not allowed on Xbox  Live. You can obtain a new key vault from another console and apply it  to yours to unban it. |
| **FSD**                              | FreeStyle Dash. A replacement for the Microsoft NXE dashboard. |
| **NiNJA**                            | An XBLS service.                                             |
| **NXE**                              | New Xbox Experience. The dashboard layout that followed the original "blades" dashboard. |
| **PartnerNet (pNet)**                | The Xbox 360 developer network, similar to Xbox Live. At one time, JTAG exploited systems could connect, but it now it will  brick your device if you do not have a legitimate XDK. |
| **ROL**                              | Ring of Light. The LED ring on the power button of your Xbox 360. |
| **STFS**                             | Secure Transacted File System. The file system that the Xbox 360 uses for packages created and downloaded by the system. |
| **Unsigned Code**                    | Unofficial code - such as community made apps or  games - that can run on the Xbox 360. This can only be achieved through  the JTAG/RGH exploits. |
| **XBLS**                             | Xbox Live Stealth. A service that takes large measures to spoof your XBL traffic to appear to come from an unmodified console. |
| **XBLSE**                            | Xbox Live Stealth Emulated. A version of XBLS released for people to run XBLS for free at home. |
| **Xbox 360 Neighborhood**            | An official development tool used to allow developer kits to communicate with your PC. |
| **FATX**                             | File Allocation Table for Xbox. The format that the Xbox hard drive stores files in. |
| **XDK**                              | An Xbox Development Kit (also known as a devkit). This is an official console used to develop software for the Xbox 360. |
| **XEX**                              | Xenon Executable. The file type that the Xbox 360 can execute, similar to an EXE on Windows. |
| **XGD3**                             | Xbox Game Disk 3. A new format for disc games with added security over XGD2. |
