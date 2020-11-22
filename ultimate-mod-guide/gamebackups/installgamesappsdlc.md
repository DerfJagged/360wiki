# Installing Apps, Games, and DLC

------

This guide will show you where to install different content so it can be run on a JTAG/RGH exploited console.

------

## Xbox 360 Disc Rips

Xbox 360 games ripped from a disc can be placed anywhere. Most  dashboards have to have a content path set in order to automatically  find them, which you can change in the dashboard settings.

## Xbox Live Arcade Games

Xbox Live Arcade (XBLA) games are usually available in package files that contain STFS. An example file name is: `26F32F9B748A8F60CDE75EB5A56185E470CA7C3858`. There are three ways to install arcade games.

##### Internal Installation

If you want games to show in original dashboard then the games should be installed to your hard drive under the Content directory inside of  the public download directory (0000000000000000) and inside the  directory with the Title ID. If you're not sure what the Title ID is,  you can look it up on the [Games Database](http://www.gamesdatabase.org/xbox_360_games_list_with_title_ids). Inside the Title ID directory should be a folder named 000D0000 which  contains your game file. The full path of a game should look something  like this: `0000000000000000/68C101BA/000D0000/26F32F9B748A8F60CDE75EB5A56185E470CA7C3858`.

##### External Installation

If you don't want to install game to the internal hard drive, then  you can install it to an external hard drive as is. Dashboards should be able to find the game automatically if the content paths were set to  search for games on your external hard drive.

##### Extracted

You can extract the game with a tool such as [wxPirs](http://gael360.free.fr/wxPirs.php) and launch it manually from Default.xex. Some of the dashboards may recognize the game even in this form.

## Games on Demand

There are two ways to install Game on Demand (GOD) games.

##### Internal Installation

If you want games to show in original dashboard then the games should be installed to your hard drive under the Content directory inside of  the public download directory (0000000000000000) and inside the  directory with the Title ID. If you're not sure what the Title ID is,  you can look it up on the [Games Database](http://www.gamesdatabase.org/xbox_360_games_list_with_title_ids). Inside the Title ID directory should be a folder named 00070000which  contains your game file. The full path of a game should look something  like this: `0000000000000000/68C101BA/00070000/26F32F9B748A8F60CDE75EB5A56185E470CA7C3858`.

##### Extracted

One option is to [extract the GOD package](https://www.reddit.com/r/360hacks/wiki/god2iso) and use the extracted files. Most dashboards will find files and treat it as game.

## Xbox Indie Games

To play Indie Games you should have [this title update](http://download.digiex.net/Consoles/Xbox360/TitleUpdates/IndyGameTitleUpdate.zip) installed by placing it in  "0000000000000000/58E07D2/000B0000/tu32000100_00000000". Indie games  usually come in packages containing STFS. These should go inside the  "0000000000000000/58E07D2/00000002" directory. The full path of an indie game should look something like this:`"0000000000000000/58E07D2/00000002/1DDF3646E2A20520C06D6FFF5F1B2979121879AC58`.

## Homebrew

Homebrew software can be installed anywhere. Most of the dashboards  will recognize homebrew content if you have set a specific path to be  scanned. Homebrew can also be executed directly from any file browser by launching Default.xex.

## LibXenon Homebrew

Homebrew compiled with libXenon are not usually recognized by any  dashboard and need to be executed manually from a file browser. The  executable of libXenon homebrew contains .elf extension. You can also  place the .elf file onto the root of a USB storage device and insert it  into the Xbox. When the Xbox is started by pressing the eject button, it will load directly into the application.

## DLC

DLC files should go inside the Content directory "00000002" of a  Title ID folder. The full path of a DLC should look something like this: `0000000000000000/58E07D2/00000002/D15B11B78B42EAD08103E25AA45D2946942B1BCC54`.

## Original Xbox Games

Ensure that your Xbox 360 is [able to run Xbox games](https://www.reddit.com/r/360hacks/wiki/original_xbox). Original Xbox games can be placed anywhere and most of the dashboards will recognize them if a content path is set correctly.

GTA5 disc 2 shouldn't be installed to hard drive as it causes pop in issues