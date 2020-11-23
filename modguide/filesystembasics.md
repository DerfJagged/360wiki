# Files and Directories

------

This page describes the file systems used by the Xbox 360 as well as  what each directory is on the hard drive. Most custom dashboards have built in file browsers and provide an [FTP service](../software/filetransfer/ftp.md) for connecting to the Xbox 360 from another device. There is also  dedicated file browsing software on the Xbox 360 console, like [XeXMenu](../software/utilities/xexmenu.md).

------

## File Systems

The Xbox 360 uses various file systems for storing games, user content, and more.

- [**FATX**](http://free60.org/wiki/FATX) (File Allocation Table for Xbox) is the storage file system used on  hard drives, memory units, USB devices, and xlaunch.fdf files.
  - Windows tools: 
    - [FatXplorer](https://fatxplorer.eaton-works.com/information/)
    - [Party Buffalo Drive Explorer](https://digiex.net/attachments/party-buffalo-xbox-360-drive-explorer-2-0-1-0-zip.11993/)
    - [Xplorer360](http://theisozone.com/downloads/xbox/tools/xplorer-360/)
    - [Horizon](https://www.wemod.com/horizon)
    - [Velocity](https://github.com/hetelek/Velocity)
    - [wxHdd](http://gael360.free.fr/files/wxHdd-1.2.rar)
- [**GDFX (Game Disc Format for Xbox) / XSF**](http://free60.org/wiki/GDFX) is the file system used on Xbox 360 CD/DVD Media.
  - Windows tools: 
    - [Velocity](https://github.com/hetelek/Velocity),
    - [wx360](http://gael360.free.fr/files/wx360-1.6.rar),
    - [wxRipper](http://gael360.free.fr/files/wxRipper-1.2.rar)
- [**STFS (Secure Transacted File System)**](http://free60.org/wiki/STFS) is used for game saves, profiles, arcade games, downloadable content  and more. STFS is also referred to as CON/LIVE/PIRS files, as they are  all STFS files, just signed with a different header.
  - Windows tools: 
    - [Velocity](https://github.com/hetelek/Velocity)
    - [wxPirs](http://gael360.free.fr/files/wxPirs-1.1.rar)
- [SFCX](http://free60.org/wiki/SFCX) (Secure File Cache for Xbox) is used for cache storage for games. 
- [**NAND File System**](http://free60.org/wiki/NAND_File_System) is used to store the bootloaders, kernel, keyvault and other files on the NAND. CPU key is required to browse its contents.
  - Windows tools:
    - [360 Flash Dump Tool](https://mega.nz/#!mhwkEShZ!_UYB1tP-G4a2VGIdh68cPAplH6yUSp_9PLpvY2ri-ns)

## Root

Different file browsers for the Xbox 360 will list different  directories in root, but generally follow the name convention below.  Some file browsers won't show all directories, this changes between  implementations.

- **DVD**: Contents of current CD/DVD in the disc drive.
- **Game**: Shortcut for the currently loaded applications directory. This is directory where currently loaded .xex exists.
- **Hdd1**: Internal hard disk main partition (partition 3).
- **HddX**: [Original Xbox backwards compatibility partition](https://www.reddit.com/r/360hacks/wiki/original_xbox) (partition 2). This might not be present if it is not installed.
- **SysExt**: System extended partition.
- **System**: Contents of the NAND chip.
- **Usb0**: Contents of first plugged in USB drive.
- **Usb1**: Contents of second plugged in USB drive.

### Hdd1

Hdd1 is where all console-created and downloaded content is stored.  From here can be found for example profiles, save games, DLC, Game on  Demand games, title updates. Custom dashboard software is also usually  installed here and is where the dashboard tries to find the launch.ini  file.

##### Example Structure

> - Cache (partition 0)
>
> - Content
>
>   - 0000000000000000 
>
>     (public directory)
>
>     - 4D5307DC *(example title)*
>     - 4D5307EA *(example title)*
>     - ...other titles
>
>   - E00015BF00008BD2 
>
>     (example profile)
>
>     - 4D53880C *(example title)*
>
>     - FFFE07D1 
>
>       (profile GPD)
>
>       - 00010000 *(profile data)*
>
>     - ... other titles
>
>   - E0004EC40000CBC7 
>
>     (example profile)
>
>     - 5655002A *(example title)*
>
>     - FFFE07D1 
>
>       (profile GPD)
>
>       - 00010000 *(profile data)*
>
>     - ... other titles
>
>   - ...other profiles
>
> - FreeStyle
>
> - Aurora
>
> - launch.ini
>
> - name.txt

##### Content

- The 0000000000000000 directory is a common public or "download"  directory for all profiles in system. Everything downloaded from the  Xbox Marketplace and files installed system-wide (for example DLC and  game extra files) are stored here. Files in here are usually "PIR" and  "LIVE", meaning that they are signed with Microsoft's private key and  verified by consoles public key.

- The FFFE07D1 directory contains a profile's [Game Profile Data](https://free60.org/wiki/GPD) in the 0001000 directory which includes the profile's achievements, name, and profile settings.

- Other directories inside Content are profile directories. The  name of a directory is a profile's ID. Under here are files that are  specific to a profile, such as game saves. Files under here are usually  type of "CON" meaning that they're signed by consoles private key.

- Files inside of both the public and profile-specific directories  are directories identified by Title ID. Each game or app has its own  unique Title ID, [which can be looked up here](http://xboxunity.net/). Each Title ID directory contains directories that are identified by  type of data they hold inside them as listed below. Files inside these  directories are usually packages with STFS and can be opened with a tool such as [Velocity](https://github.com/hetelek/Velocity).

  > - 000D0000    Arcade Title
  > - 00009000    Avatar Item
  > - 00040000    Cache File
  > - 02000000    Community Game
  > - 00080000    Game Demo
  > - 00020000    Gamer Picture
  > - 000A0000    Game Title
  > - 000C0000    Game Trailer
  > - 00400000    Game Video
  > - 00004000    Installed Game
  > - 000B0000    Installer
  > - 00002000    IPTV Pause Buffer
  > - 000F0000    License Store
  > - 00000002    Marketplace Content
  > - 00100000    Movie
  > - 0x300000    Music Video
  > - 0x500000    Podcast Video
  > - 00010000    Profile
  > - 00000003    Publisher
  > - 00000001    Saved Game
  > - 00050000    Storage Download
  > - 00030000    Theme
  > - 00200000    TV
  > - 00900000    Video
  > - 00600000    Viral Video
  > - 00070000    Xbox Download
  > - 00005000    Xbox Original Game
  > - 00060000    Xbox Saved Game
  > - 00001000    Xbox 360 Title
  > - 00005000    Xbox Title
  > - 000E0000    XNA

### HddX

HddX is the original Xbox backwards compatibility partition. It is  used when playing original Xbox games on the Xbox 360. If partition is  not visible [it might not be installed](https://www.reddit.com/r/360hacks/wiki/original_xbox).

### SysExt

The SystemExtended partition introduced in the 2.0.12611.0  (Kinect-Dashboard) update was created to hold Kinect and Avatar related  system files. Most likely the reason for this partition to exist is that Microsoft needed place for new system files and there was not enough  space in the NAND chip to hold everything. **SysExt contains  important system files and it is dangerous to change anything if you  don't know what you're doing. Broken SysExt can lead to a bricked  console!**

### System

The System partition contains the contents of your Xbox 360 NAND chip. **The NAND contains important system files and it is dangerous to change anything if you don't know what you're doing. Broken NAND can lead to a bricked console!**

# Extracting/Injecting Game Saves

------

This guide will walk you through managing your Xbox / Xbox 360 game  saves. Saves are stored on a per-profile per-game basis, and require  resigning to work on other profiles. 

------

## Xbox 360 Saves

1. Connect your Xbox 360 hard drive to your PC with a transfer cable or plug in a flash drive that you've moved saves onto using the  Microsoft dashboard memory manager. 
2. Navigate into Partition 3 > Content. This folder contains a folder for each profile on the system, and a public directory `0000000000000000` ([example structure here](https://www.reddit.com/r/360hacks/wiki/files#wiki_example_structure)). Open your profile, and a folder for each game will be inside. Right  click the desired game, and select "Extract..." if you wish to copy the  save to your PC, or right click the blank field and select "Insert  Folder" and insert your game save folder. It should be something like `373407DB`. 

## Injecting Original Xbox Saves (Transfer Cable)

Keep in mind that Burnout 3: Takedown, Dead or Alive Ultimate (1 and  2), Dead or Alive Xtreme Beach Volleyball, Forza Motorsport, Half-Life  2, Ninja Gaiden, Ninja Gaiden Black and Tron 2.0: Killer App saves are  EEPROM locked and therefore you cannot use them on an Xbox 360.

1. Connect your Xbox 360 hard drive to your PC with a transfer cable. 
2. Open Xplorer360, select Drive > "Open hard drive or  memcard...", and expand Partition 3 > Compatability > Xbox 1 >  UDATA. 
3. Right click the empty field and select "Insert Folder" and choose your original Xbox game save folder. It should be something like `5655002A`. 