i am temporary. i am here to hold things that need to get sorted out



# Miscellaneous Info

------

This stuff is kept here for archival purposes and may be moved to other pages in the future.

------

[How the TrueSkill Matchmaking system works](https://web.archive.org/web/20070103052751/http://research.microsoft.com:80/mlp/trueskill/Details.aspx)

[Info on the burnable Kiosk Disc](https://web.archive.org/web/20070125234138/http://www.xbox-scene.com:80/xbox1data/sep/EEFVyAAAuFzsesrMmN.php)

[First teaser commercial](https://drive.google.com/open?id=0B93MDqtePlcDaGxIMURHd0dNb00) (name was not known at the time)

[22C3](https://www.youtube.com/watch?v=xlSOAsLSYzE)

[2008 Google Talk - The Xbox 360 Security System and Weaknesses](https://www.youtube.com/watch?v=uxjpmc8ZIxM)

[HD-DVD Emulator](http://codeasm.com/xbox/files/HDDVD) 

[Editions Pictures](http://www.xboxaddict.com/forums/showthread.php?85650-Hellonearth159-s-Console-Collection)

[Info on each exploit type](https://www.se7ensins.com/forums/threads/the-science-behind-exploited-hacked-consoles-how-a-jtag-rgh-works.1498827/)

Backup these files:

- http://www.360-hq.com/xbox360-homebrew-184-Bluebars.html
- http://www.360-hq.com/xbox360-homebrew-33-PPC_Altivec_support_for_IDA.html

## Notes

- RGH 1.2 uses PLL instead of IC2 to slow clock; RGH 2 glitches before eFuse check
- ABGX does hash checks on ISOs
- Using this command will make a debug build bootable on JTAG/RGH: `xextool.exe -rm -md default.xex > default_dev.xex` OR use x360gamehack 6.3 by xorloser
- NTFS and exfat not supported on Xbox 360
- The only option for Corona v2/v4 for dumping the NAND is the SD card method
- To fix a sidecar that had a bad FPGA flash (red ring), remove the sidecar. launch Xbox360 Command Prompt, turn the XDK on, set the XDK to default in Neighborhood, plug the DVDEMU port on the sidecar into your  PC via USB, enter `xkd /i:0`, followed by `y`. It will write all 46 blocks and reboot when completed.
- List of known certified developer networks: 
  - CertNet
  - GSM
  - int2
  - Int2Net
  - Int2Net(NULL_AES)
  - PartnerNet
  - ProductionNet
  - StressNet1
  - StressNet2
  - TestNet
  - TestNet(NULL_AES)
  - TestNetMain
  - TestNetShip
  - VintNet
  - VinNet
- Medusa is a device that connects to Xbox 360 Kiosks to:
  - Block access to Xbox LIVE
  - Block access to settings
  - Automate demo time (OFF/5MINS/10MINS/15MINS)
  - Can access "Retailer Specific" images
  - (rumor) Block wireless controllers
  - Block exiting the demo disc
- Recommended chips for RGH
  - Xenon/Zephyr/Trinity/Corona - Ace v3
  - Falcon - Revc or Matrixx
  - Jasper/Kronos - Revc
- GTA5 disc 2 shouldn't be installed to hard drive as it causes pop in issues

# 360 Hacks To-Do List

------

## Upcoming additions

- Everything that has been ~~striked through~~ on the index page
- **Drive flashing page**
- [Integrate this stuff](https://www.reddit.com/r/360hacks/comments/8y9jql/start_here_everything_you_need_to_know_about_xbox/)
- Add to FAQ:
  - Why dash 7371 isn't always JTAGable, and maybe how to check it
  - The difference between JTAG and RGH
  - Power Supply region incompatibility [1](https://support.xbox.com/en-US/xbox-360/console/power-supply)
- Video mode reset combo in troubleshooting page (Y + RT)?
- Link to drive firmwares and timing files
- XGD3 Game Burning [1](https://digiex.net/threads/burn-xbox-360-xgd3-iso-games-with-the-burnermax-payload-tool.15066/)
- Xbox 360 SMC Power Mode Editing (Fixes Falcon Freezing on RGH2 [1](https://web.archive.org/web/20160820152200/https://www.se7ensins.com/forums/threads/xbox-360-smc-power-mode-editing-fixes-falcon-freezing-on-rgh2.1166312/) [2](https://web.archive.org/web/20170906105251/http://falconfreeze.weebly.com/)
- Add this to board identification? [1](http://i.imgur.com/yVQf5D2.jpg)
- More homebrew [here](http://www.homebrew-connection.org/files/xbox/) 
- Custom Profile Pic [safe](https://www.xpgamesaves.com/threads/custom-gamer-picture-tut-use-any-image.130222/) / [profile mod](https://www.thetechgame.com/Tutorials/id=2974/c=2814/how-to-make-mod-your-own-gamer-picture.html)
- Add Unofficial Xbox Backwards Compat page [1](https://docs.google.com/spreadsheets/d/1uU9j4X-WK01UZuZzv6FuDkYakmkke2X9rB14j2n4YRw/edit#gid=0)
- [Fixing Battery Charge Pack](https://technofaq.org/posts/2012/11/xbox360-rechargable-battery-pack-not-charging-the-fix-is-here/) 
- Verify names are correct for ConnectX plugin settings in Aurora on [this page](https://www.reddit.com/r/360hacks/wiki/connectx)
- Get hi-res pictures of all motherboards top/bottom and redo JTAG/RGH pictures
- Alternate solder points page for JTAG/RGH
- [MilkyTracker](http://www.360-hq.com/xbox360-homebrew-215-Milkytracker.html)
- Subsection for LibXenon emus?
- Check out [Viper360](http://www.360-hq.com/xbox360-homebrew-91-Viper360.html) and XPRemap
- What is the exact name of the "update firmware" menu tab in JRunner for NAND-X?
- Fixing bad NAND [1](https://www.youtube.com/watch?v=t-UcPyO-a1M&list=PLn7ji3VsPy3G08cHNCHyT4Yj-WWYhw8D7&index=29) (Corona too) [2](https://www.youtube.com/watch?v=-G7i0_1gEC8&list=PLn7ji3VsPy3G08cHNCHyT4Yj-WWYhw8D7&index=32) [3](https://www.youtube.com/watch?v=ocaFVmMJc50&list=PL1CadovfabPskGb2Ur4kBGzD5s7DzQw5I&index=33) (note that 4GB slims with EMMC often corrupt themselves on their own, and there's a way to replace the EMMC with a NOR)
- Sonus 360 [1](https://www.youtube.com/watch?v=-pThJ-jallE&list=PL1CadovfabPskGb2Ur4kBGzD5s7DzQw5I&index=35)
- **Convert DLC/game region**
- What does XCE Tools stand for? Xbox Cheat Engine? Is  JRPC/RPC/XRPC.xex official tools? What's the differences? Does Peekpoker need all of them?
- Xbox 360 XISO Extract
- Archive mod tools, maybe integrate some?
- Credits from [xbins](https://www.xbins.org/applist.php+&cd=4&hl=en&ct=clnk&gl=us)
- Credit Horizon (staff of TTG/XboxMB) and Modio devs 
- DRM free game content?
- How to recover deleted data with FATXplorer [1](https://fatxplorer.eaton-works.com/download/)

------

- After JTAG/RGH/Drive Flashing pages are finished, crosspost the  history page and Xbox history page on Se7ensins, The Tech Game,  Modnetwork, and the Xbox360ISO.
- *Nothing else planned! Suggest something :)*

Firstly, mot of this post is me aggregating the info and links together, so  please excuse my copy-pasting, but at least I give credit! Also, I will  come back and edit and create a proper comprehensive guide, I am just  extremely tired right now and wanted to make something real quick to put some basic info in people's noggins.

https://www.se7ensins.com/forums/threads/the-science-behind-exploited-hacked-consoles-how-a-jtag-rgh-works.1498827/

From https://www.se7ensins.com/forums/threads/xbox-360-modding-useful-information-files-references-and-more.1003653/

**Xbox 360 Modding: Useful Information**

**Hey  and welcome to my thread with important links/information on Xbox 360  Modding! This thread is designed for people both new and experienced,   and is hopefully a good place to find what you may need in your journey  through 360 modding. The goal of this thread is simple: To provide a   good number of links to things you may find handy such as guides,   files/programs, tutorials, pictures, etc. I tried to set it up so that   the things here are what you might call "essential"**

**Here  you can find things like the latest version of dashlaunch, xeBuildGUI,  etc, and references like the Team Xecuter forums directions on   installing the Coolrunners. Just  take a look under the section of mods  you are interested in and you may  find something you need. I will try  and keep this as updated as  possible and add more links as I think of  them! Feel free to report  downed links or outdated info, or suggest  links!**

Note:  If a  program does not have a version next to it that is because its  link is  to a download page so the link will always be to the latest  version as  the site updates their downloads

**JTAG/RGH/R-JTAG**

**Guides/Tutorials/References:**
[[JTAG/RGH\] Xbox 360 Ultimate Exploit Guide ](http://www.se7ensins.com/forums/threads/jtag-rgh-xbox-360-ultimate-exploit-guide.804054/)- Comprehensive JTAG/RGH/R-JTAG
modding guide by yours truly

[Xbox 360 Homebrew Hacks - JTAG/RGH/RGH2/R-JTAG ](http://www.se7ensins.com/forums/threads/xbox-360-homebrew-hacks-jtag-rgh-rgh2-r-jtag.623614/)- A good explanation about the different NAND based hacks
[Beginners Guide To Using a JTAG ](http://www.se7ensins.com/forums/threads/beginners-guide-to-using-a-jtag.197037/)- A little dated, but still gives a great basic intro to using NAND modded consoles
[How to check if your Console is JTAG-able ](http://www.se7ensins.com/forums/threads/how-to-check-if-your-console-is-jtag-able.271521/)-  Most consoles are RGHable or R-JTAGable (or it is easy to make them   that way), but knowing if a console is JTAGable can sometimes be a   little harder.
[How to Update A JTAG or RGH Console ](http://www.se7ensins.com/forums/threads/how-to-update-a-jtag-or-rgh-console.800947/)- A great guide on how to update your NAND modded console to the latest dash
[[JTAG/RGH/General\] How to Solder Properly (Relative to the Xbox 360) ](http://www.se7ensins.com/forums/threads/jtag-rgh-general-how-to-solder-properly-relative-to-the-xbox-360.919050/)- Another guide by me. Helpful for people that are new to soldering
[Xecuter CoolRunner Installation Guides ](http://team-xecuter.com/forums/forumdisplay.php?f=175)- The official TX sub-forum for the Coolrunner installation diagrams
[Xecuter CoolRunner / CR3 Lite Support ](http://team-xecuter.com/forums/forumdisplay.php?f=174)- The official TX sub-forum for general Coolrunner information
[Xecuter CR3 PRO Support ](http://team-xecuter.com/forums/forumdisplay.php?f=199)- Same as above but for the CR3 Pro
[Xecuter R-JTAG Installation & Setup Guide *** UPDATED JULY 26th 2013 ](http://team-xecuter.com/forums/showthread.php?t=135779)- The official TX thread for the R-JTAG hack installation information
[Xecuter R-JTAG Support ](http://team-xecuter.com/forums/forumdisplay.php?f=240)- The official TX sub-forum for general R-JTAG information

**Programs/Tools/Files:**
[Dashlaunch (3.10)](http://www.realmodscene.com/index.php?/topic/2456-dashlaunch-310/)  - A fantastic plugin for JTAG/RGH/R-JTAG consoles that is pretty much  standard these days. It allows you to boot right to an .xex (i.e. FSD)  and has some other pretty useful features
[Freestyle Dash 3 (Rev 775)](http://www.realmodscene.com/index.php?/topic/2090-f3-rev-775/) - A great dashboard replacement that is organized, cool looking, and customizable. Also pretty standard.
[Simple 360 NAND Flasher](http://www.homebrew-connection.org/simple-360-nand-flasher-v1-2-by-swizzy-corona-4gb-nand-dump-and-write-support-added/) - An incredibly useful tool that allows you to write/read your 360s NAND from the console itself.
[List of Emulators for the 360](http://dev360.wikia.com/wiki/List_of_Emulators)
[XEXMenu (1.1)](http://digiex.net/downloads/download-center-2-0/xbox-360-content/libxenon-homebrew-jtag-reset-glitch-content/11096-xexmenu-1-1-download-xex-menu-iso-live-xex-file-manager-xbox-360-a.html)  - A simple file explorer with a few additional features. Was mainly   used before FSD became popular. Comes in LIVE container and ISO forms.
[360MPGUI](http://www.realmodscene.com/index.php?/topic/100-360mpgui-v1092-added-offline-2-online-profile-maker-nxeart-extractor/) - A multi-tool program with many features. Great for extracting ISOs.
[Auto Xbins (2013)](http://digiex.net/downloads/download-center-2-0/xbox-360-content/apps-pc/3134-auto-xbins-2008-2013-a.html) - A tool that automatically connects you to the xbins FTP. A great resource for programs, emulators, etc.
[xeBuildGUI (2.091)](http://www.homebrew-connection.org/xebuild-gui-2-091-16537-kernel-support-added/)  - A tool that allows you to create NAND images for your console   (JTAG/RGH/R-JTAG and retail). It is used a lot and very easy to use.
[J-Runner (Beta 3 Build 1)](http://team-xecuter.com/forums/showthread.php?t=82434)  - Another tool that allows you to create NAND images for your console  (JTAG/RGH/R-JTAG and retail), but also works directly with Team Xecuter  hardware such as the NAND-X and the DemoN. Also very popular and easy  to  use. It also can self update.
[360 Flash Tool (0.97)](http://www.realmodscene.com/index.php?/topic/51-360-flash-tool-v097/) - A great tool for working with NAND images, KVs, etc.

**DVD Drive Mods**

**Guides/Tutorials/References:**
[Team Xecuter JungleFlasher Tutorials](http://team-xecuter.com/forums/forumdisplay.php?f=136)  - The official TX sub-forum that has a tutorial on how to flash every  single drive. The only negative is that it assumes you are using their  equipment which might not be the case. Still very helpful though  because  it shows the process of using JungleFlasher, and is by far the  best at  doing so
[How to Easily Identify Your Xbox 360 DVD Drive ](http://www.se7ensins.com/forums/threads/how-to-easily-identify-your-xbox-360-dvd-drive.92931/)- This only covers phat drives
[How to Flash any Xbox 360 Drive with a Laptop ](http://www.se7ensins.com/forums/threads/how-to-flash-any-xbox-360-drive-with-a-laptop.97270/)- Only for phat drives
[LIST so far of burnermax payload tool compatible drives ](http://www.se7ensins.com/forums/threads/list-so-far-of-burnermax-payload-tool-compateble-drives.894861/)- Drives that work with the BurnerMAX Payload tool for burning XGD3 games
[[TUT\] How to correctly burn XGD3 games](http://www.se7ensins.com/forums/threads/tut-how-to-correctly-burn-xgd3-games.798973/)
[Se7enSins Official x360key Thread ](http://www.se7ensins.com/forums/threads/se7ensins-official-x360key-thread.591545/)- A great thread that talks about how to use the xk3y x360key

**Programs/Tools/Files:**
[Jungle Flasher](http://jungleflasher.net/downloads.html) - Pretty much the sole program used for flashing drives.
[Kprobe (2.5.2)](http://team-xecuter.com/forums/showthread.php?t=73298) - A program that is used to test the quality of your burns. Only works with Liteon Drives.
[agbx360](http://abgx360.net/download.php) - The program that stealth patches your games. Used all the time
[ImgBurn](http://www.imgburn.com/index.php?act=download) - A common program that pull use to burn their games
[Xbox 360 Backup Creator (2.9)](http://www.realmodscene.com/index.php?/topic/584-xbox-backup-creator-v29-build0425-by-redline99/) - A decent program with many ISO/Disk tools.
[C4E’s BurnerMAX Payload Tool (0.15) ](http://team-xecuter.com/forums/showthread.php?t=97272)- A program that allows drives other than an iHas 124B to burn XGD3 Games
[k3y Forums](http://k3yforums.com/index.php) - The offical xk3y forums. Useful for getting firmware updates and support
[iXtreme LT+ 3.0 Download ](http://www.ixtreme.net/ixtreme-lt-lite-touch-download/21442-ixtreme-lt-3-0-download.html)- The latest iXtreme modded firmware.

**USB/HDD Transfer/Save Game Mods**

**Guides/Tutorials/References/Files:**
[The Possibilities of USB/Transfer Cable Modding ](http://www.se7ensins.com/forums/threads/the-possibilities-of-usb-transfer-cable-modding.186848/)- An overview of USB/HDD Transfer modding

**Programs/Tools:**
[USBXTAFGUI (v44)](http://digiex.net/downloads/download-center-2-0/xbox-360-content/apps-pc/4046-usbxtaf-xbox-360-usb-storage-explorer-xplorer-usbxtaf-v44-download.html) - A good simple program that can browse FATX partitions (i.e. Xbox 360 Hard Drives, MU, and USB MU)
[Modio](http://www.game-tuts.com/community/modio.php)  - A well known USB modding program. You can browse HDDs and USB MUs   with it, easily move and resign/rehash saves, and download pre-modded   save games.
[Hoizon (2.2.2.0)](http://digiex.net/downloads/download-center-2-0/xbox-360-content/apps-pc/10310-horizon-xbox-360-usb-modding-tool-download-2-2-2-0-a.html) - Similar to Modio but with some better functionality. However the better parts costs money in the form of a membership
[HxD](http://mh-nexus.de/en/hxd/) - A pretty good free HEX editor

https://community.wemod.com/t/everything-you-need-to-know-on-modding-for-xbox-360/4824



None of this is mine(as of writing this), I will make this properly done and have a full guide from beginning to end on all types of mods from  LEDs to fans to running backups from a harddrive, etc. But for now,  enjoy! Also, mods: can this get a pin? Probably after it's done, but may as well ask now anyways.



I didnt find this tutorial and I think it beats the ones listed above https://www.se7ensins.com/forums/threads/rgh-1-2-start-to-finish-tutorial-how-to-get-a-cr4-like-experience-phats-only.1349194/

You can download and install title updates (TU) yourself without the use of xbox live.

