# XexDash

------

[XexDash](http://www.mediafire.com/file/n9pla9aa3gk1s3o/XexDash_v0.03.zip/file), not to be confused with the more popular [XeXMenu](https://360.consolemods.org/software/utilities/xexmenu.html), is a minimal custom dashboard capable of launching game backups, FTP,  and changing fan speeds. On release, XexDash was used for supporting  Chinese and Japanese characters in game and folder names, a feature that caused issues on other dashboards.

- The default username/password for FTP is "xbox" and "xbox".
- If you have issues using FTP after using this dashboard, delete the `XexDash.xml` file it generated on hdd1:. You may need to completely remove the dashboard and restart your Xbox 360 to get it to work. 

------

## Installation

### As a Demo Shortcut

Extract XexDash_Dashboard.zip and copy the folder "C0DE0003" to `Hdd1:\Content\0000000000000000` or `usb1:\Content\0000000000000000`. Launch it from the Microsoft dashboard by navigating to Game Library > Demos > XexDash.

### As a XEX

Extract XexDash_Xex.zip and copy the folder "XexDash" to your Xbox  360. Use a file manager to navigate into the folder and launch it by  selecting the .xex.

## Controls

- DPAD: Up/down/left/right
- LT/RT/LB/RB: Page up/down on games
- A: Enter/Confirm
- Y: Menu
- X: Sort games by name
- B: Readme
- Back: Return to Dashboard

## Game Launcher:

Copy your game files of an Xbox or Xbox 360 game to a folder inside of `Hdd1:\hidden`, `Usb0:\hidden`, `Cdrom0:\hidden`, or `Devkit:\hidden`. From the main screen of XexDash, press Y to open the menu, then select  Driver Disk, and choose the device holding the game files. It will  populate a list of your games. Hover over a game and it will list the  title ID in the top left of the screen, and you can launch it by  pressing A. 

- If you wish to add cover art to the game, place a picture named `default.png` in the game folder and it will display in the bottom left corner.

## FTP Server

Your IP is listed in the bottom right of the screen. You can connect to it at port 21 with the username `xbox` and password `xbox`. 

## Menu

- **Driver Disk**: Selects the device to load the game list from.
- **Type**: Change the type of game to regular game or XBLA game.
- **Language**: Change the language to English, Japanese, or two dialects of Chinese.
- **Set**: Press left or right on the DPAD to select  where it pulls a background image from. The easiest way is to set it to  [system] and place a `background.jpg` in .../XexDash/media.
- **Update**: Previously would update the dashboard. No longer functional.
- **Fan**: Press left or right on the DPAD to change the  fan speed by 5%. Setting applies from when you open XexDash until Xbox  is shut off.
- **Return to XDK**: Returns to the XDK menu, or if not installed, your default dashboard.
- **Return to Dash**: Returns to your default dashboard.