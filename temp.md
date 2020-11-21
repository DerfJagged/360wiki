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