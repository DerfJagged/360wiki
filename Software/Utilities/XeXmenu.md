# XeXMenu

------

[XeXMenu](https://mega.nz/file/9AlUmDZK#oykniipcx80kvuRxLaqY8NtPMJYKHW1ZYpqYfcAZsLA) is a dashboard for the Xbox 360. It is often recommended in JTAG/RGH  tutorials as the first dashboard to be installed as it has an installer  that shows up under the Games library in the official dash. However, it  is limited in function compared to more feature rich dashboards such as [Freestyle Dash](https://360.consolemods.org/software/dashboards/fsd.html) or [Aurora](https://360.consolemods.org/software/dashboards/aurora.html).

A video demonstration of installing XeXMenu can be found on [MrMario2011's channel](https://youtu.be/w5xVFNkxv-I?list=PL1CadovfabPskGb2Ur4kBGzD5s7DzQw5I).

- The default username/password for FTP is "xbox" and "xbox".

------

## Installation

1. Plug a flash drive into your Xbox 360 and navigate to Console  Settings > Storage. Select the flash drive and allow it to format the flash drive as a system drive. 
2. Extract the `CODE9999` folder from the [XeXMenu 1.2 rar](http://www.mediafire.com/file/7orm0jrkncrzo1w/xexmenu12live.rar/file) to your Desktop.
3. Plug the flash drive into your PC. Open [Xplorer360](http://www.mediafire.com/file/zb6ic4036c6nmpg/Xplorer360.exe/file) and select Drive > Open > Harddrive or Memcard. On the left-hand  side, select Partition 3, then right-click the Content folder, select  "New Folder", and name it `0000000000000000` (16 zeroes). Open the new folder, then drag the `CODE9999` folder into it.
4. Select Drive > Close, then close Xplorer360. Safely eject your flash drive and plug it into your Xbox 360. Navigate to the Demos  section of your dashboard, and it should list XeXMenu there. Select it  to launch it. 
   - You can install XeXMenu to your hard drive by going to Console  Settings > Storage, and copying it from your flash drive to the hard  drive.

## Controls

- **Back**: Visual control list
- **Start**: Launch selection
- **LB/RB**: Change menu
- **DPAD Left/Right**: Change directory
- **Y**: Rescan devices / file context menu
- **A**: Launch selection
- **B**: Back (in file manager)

## Discovery Menu

### Games Discovery

Any games in hdd1://Games will be listed here and launchable. Press left/right on DPAD to change to different directory.

### Emulators Directory

Any emulators in hdd1://Emulators will be listed here and launchable. Press left/right on DPAD to change to different directory.

### Applications Directory

Any emulators in hdd1://Apps will be listed here and launchable. Press left/right on DPAD to change to different directory.

## File Manager Menu

Your files and folders are listed for the selected device (hdd1, usb0, usb1, or Flash). **Do not touch your files in flash unless you know what you are doing**. Press Y to open the context menu on any file or folder for  Copy/Cut/Paste/Delete/Create/CopyDVD/PatchXex options. Press left/right  on DPAD or X to change to different directory.

### CopyDVD

This option will copy the contents of an inserted DVD to the current  directory in the file manager. A full tutorial can be found [on the game backups page](https://360.consolemods.org/modguide/gamebackups/backupgames.html).

### PatchXex

This option will patch games to run from your hard drive instead of DVD.

## Configuration

- **Skin**: Allows you to change the XeXMenu skin. By default, there is 26 skins installed
- **Enable skin auto scaling**: Resizes the skin to fit your TV
- **Auto extract games title**: Uses the official game title from the ISO of the game instead of the filename
- **Discover only default.xex**: Only shows default.xex files in the file discovery menus, ignoring any XEX not named "default"
- **Sensor**: Displays CPU/GPU/EDRAM/Motherboard temperatures
- **SMC Version**: Shows the System Management Controller version.