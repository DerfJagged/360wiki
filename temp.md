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