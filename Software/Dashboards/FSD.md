# Freestyle Dash (FSD)

------

[Freestyle Dash](http://www.mediafire.com/file/wnpyc98qahytf3q/TeamFSD.Freestyle3.0.775.7z/file) (known as FSD or F3), created by Team FSD, is a highly customizable  replacement dashboard. Features include the ability to scan, categorize, and download cover art for your Xbox 360, XBLA, and original Xbox  games; the ability to launch homebrew apps and tools; a full skinning  suite to make your dashboard look and feel how you want; and the ability to set fan settings.   

A video demonstration of how to install FSD can be found on [MrMario2011's channel](https://youtu.be/tu7PR7ehhuo?list=PL1CadovfabPskGb2Ur4kBGzD5s7DzQw5I).

The current version is [FSD3 Rev 755](http://www.mediafire.com/file/wnpyc98qahytf3q/TeamFSD.Freestyle3.0.775.7z/file).

- The default username/password for FTP is "xbox" and "xbox".

------

## Controls

- **A**: Enter/Confirm/Launch
- **B**: Back (in file manager)
- **X**: Open tray / Sign out
- **Start**: Launch game
- **Back**: Shows the weather (no longer working)
- **LB/RB**: Move left/right one tile. Shows favorites in game category
- **LT/RT**: Move up/down one row.
- **DPAD**: Move left/right one tile or up and down a row

## Default Menu

### Library

#### Open Tray

Opens or closes the disc tray, or launches the inserted game. Press X to open it if a game is inserted.

#### Profile

You can sign in to a profile by clicking here. The active avatar will be displayed. If the avatar is completely faded white, you may need to [reinstall the avatar data](https://www.reddit.com/r/360hacks/wiki/update_dash#wiki_installing_the_avatar_data). Press X to sign out if already signed in..

#### Xbox 360 Games

Opening this will list any Xbox 360 games in the specified scan  directory, which can be launched by pressing Start. Hold LB or RB to  show favorites list.

#### Xbox Live Arcade Games

Opening this will list any Xbox Live Arcade games in the specified  scan directory, which can be launched by pressing Start. Hold LB or RB  to show favorites list.

#### Homebrew

Opening this will list any homebrew apps in the specified scan  directory, which can be launched by pressing Start. Hold LB or RB to  show favorites list.

#### Xbox Classic

Opening this will list any original Xbox games in the specified scan  directory, which can be launched by pressing Start. Hold LB or RB to  show favorites list.

#### Emulators

Opening this will list any emulators (not ROMs) in the specified scan directory, which can be launched by pressing Start. Hold LB or RB to  show favorites list.

### Setup

#### Settings

##### General Settings

###### General Settings

- **Enable Kinect controls in F3**: Allows you to use your body as a controller in the dashboard.
- **Display Temperature in Celsius**: Toggle between Celsius and Fahrenheit for system temperatures
- **Sync Clock on Startup (Internet Required)**: Reaches out to an NTP server for the current time when the dashboard starts up.
- **Receive Update Notices at Startup**: No longer working. Reaches out to check for FSD updates.
- **Enable Beta Updates**: No longer working. Reaches out to check for beta FSD updates.
- **Show StatusBar at Startup**: Shows the network, status, date, and time at the bottom of the screen.
- **Show Weather on Startup**: No longer working. Displays the weather on startup. Same as pressing the Back button.
- **File Manager Advanced Mode (flash, sysext, hddx)**: Un-hides these directories in the file manager. Descriptions of the directories can be found [here](https://www.reddit.com/r/360hacks/wiki/files).
- **Enable smb: File Manager**: Allows you to manage a remote share from the file manager. 
- **Enable Samba Server**: Allows you to input the Workgroup name and Hostname of the device with the remote share for game and music streaming. 

###### JQE60.com

- Allows you to log in to JQE360 for playing on [LiNK](https://www.reddit.com/r/360hacks/wiki/link).

###### Profile

- **Avatar**: Toggle whether to show your Avatar on under the Library row.
- **Auto Sign In**: Set or unset your profile to automatically sign in when the console is powered on.

###### Updates

- No longer working. Used to update FSD, avatar data, and plugins.

###### Weather Settings

- No longer working. You can input an API key from World Weather to  pull down the weather for the entered zip code, viewable by pressing  Back on the dashboard.

###### Reset Settings

- **Clear Data**: Deletes all downloaded covers, game information, and file paths.
- **Default Settings**: Restores default FSD settings.
- **Reset Skin Settings**: Resets to default skin settings. 

##### Content Settings

###### Game List Settings

- **Show Game Background Images**: Shows image behind currently selected game.
- **Show Game Screenshot Images**: Shows screenshots of game. Number of screenshots dependent on setting in Marketplace Options.
- **Game List Style Options**: Change how games are displayed.
- **Game List Transition Options**: Change how the transition to the game list looks.

###### Marketplace Options

- Allows you to choose the marketplace locale and downloaded assets.

###### Cover Downloading

- Allows you to enable custom cover downloading, and at what resolution.

###### Scan Settings

- Allows you to disable automatic content scanning at startup. 

###### Manage Game Paths

- Press A to open the game path manager if you do not have any paths  listed. If you already have a path added, you will need to press Y to  open the game path manager. From here, you can choose a path to scan by  clicking "Change Path" and choosing the desired folder and pressing Y.  You can also choose how many folders deep you want the scan to go. Press X to save settings.

##### System Settings

###### Date/Time Format

- Allows you to set the date and time manually. Overridden if you have it set to automatically look up the time at startup.

###### Security

- Allows you to enable and set usernames and passwords for FTP  (default "xbox" for both fields) and HTTP (default "f3http" for both  fields) servers. The HTTP server allows you to enter the Xbox 360's IP  address into a web browser to view Xbox 360 related information.

###### Overscan

- Allows you to correct horizontal and vertical overscan settings to better fit your TV.

###### Fan Settings

- Allows you to set the fan speed to a percentage. It's recommended to leave it on "Auto" and adjust the target temperatures with DashLaunch  to best prevent overheating and increase fan longevity. You must launch  games/apps through FSD in order for the fan settings to be applied.

##### Plugin Settings

###### Status

- Lists the status of FSD Plugin and ConnectX. ConnectX is a plugin used to stream games from a PC on your network.

###### F3Plugin

- Lists settings for LiNK and allows you to set a button combo for taking sceenshots. Screenshots are saved to `.../FSD/PLUGINS/userdata/<game>/`

###### Connectx

- Lists settings for ConnectX, a plugin used to stream games from a PC on your network.

#### Skins

- Any skins located in `.../FSD/Skins/` will be listed here. Press A to select a skin, or X to customize it.

##### Customize Skin

- **Current Skin Settings**: Allows you to enable or disable background animations. Press X to save changes.
- **Choose Background**: Allows you to choose from backgrounds from your skin. Press X to save changes.
- **Choose Stage**: Allows you to choose from images from your skin that covers the bottom half of the screen. Press X to save changes.
- **Edit Mode (Y)**: Press Y to access edit mode. From here, you can change the theme of the background or icon of any tile on your dashboard. Press X to apply it to all tiles in the row, press Y to apply to all tiles on the dashboard. Press RS to randomize the tile.

#### Credits

- Lists credits and plays music.

### Utilities

#### File Manager

- Controls shown on screen. In order to execute a copy/move from one  side to another, you will have to hold LB or RB as a modifier for the  direction to copy/move and press the desired command. Directories and  their descriptions are listed [on this page](https://www.reddit.com/r/360hacks/wiki/files).

#### DVD Extract

- Creates a folder of the content's name and rips the currently inserted DVD or original Xbox / Xbox 360 game. 

#### Weather

- No longer works. Displays the weather.

------

## Downloading Covers [1](https://www.se7ensins.com/forums/threads/superior-method-to-adding-game-covers-banners-icons-and-backgrounds-to-fsd-v3-webui.1230170/) [2](https://mega.nz/#!ycUVjSrR!QsM9Eb5U_VQsCHTunaz8LnfaVo0VJepvosejioZgbCw)

## Troubleshooting

- FSD won't boot after changing skin
  - Likely, you applied a skin made for FSD1 or FSD3, or the skin was corrupt. Boot into XEXMenu and delete the skin from `.../FSD/Skins/` to be able to boot into FSD again.