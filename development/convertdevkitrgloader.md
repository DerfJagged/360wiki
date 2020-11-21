# Converting to a Devkit (RGLoader)

------

**Read this page in it's entirety before following the tutorial**

RGLoader is a tool used to build a devkit NAND out of your own NAND  dump. This devkit NAND can then be flashed onto your console, which  enables debug features not otherwise available on a RGH/JTAG. This also  installs xshell, the official development dashboard.

------

**Keep in mind the following:**

- This has a significant risk of going wrong and bricking your console, especially if it is a JTAG. 
- (may be different in new versions) RGloader overwrites XeLL, so the  only way to fix it is to use a hardware flasher to flash your old NAND  dump.
- DashLaunch will not work with a devkit NAND. However, any modifications to the SMC (such as fan settings) will be kept.
- Fakeanim does not work with a devkit NAND, you will need to remove the `;` and edit the path to your fakeanim in rgloader.ini if you wish to use one.
- By default, it will boot into the xshell dash. You can change this  by changing the path to a different dashboard's XEX in rgloader.ini.

[MODDED WARFARE's Tutorial](https://www.youtube.com/watch?v=YeFZd6R3K90)