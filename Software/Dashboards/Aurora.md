# Aurora



# Aurora Dashboard

------

[Aurora](http://phoenix.xboxunity.net/#/news) is a custom dashboard focused around the coverflow design of its game  launcher. Features include customizable skins, automatic download of  game updates and cover art, the ability to organize games into  categories, FTP support, integrated XLink Kai, and a plugin system. 

It is the most recently updated dashboard, with an official website at [XboxUnity.net](http://phoenix.xboxunity.net/#/news) and an official support forum at [RealModScene.com](https://www.realmodscene.com/). An FAQ can be found [here](https://www.realmodscene.com/index.php?/topic/5851-useful-qa-for-new-people-faq/).

A video demonstration of how to install Aurora can be found on [MrMario2011](https://youtu.be/FNYVGkFJV2s) or [Modded Warfare's](https://youtu.be/Kqvruf8q3J0?list=PLn7ji3VsPy3FCoZ5E3zWz5tS5iWbysPZX) channel.

- The default username/password for FTP is "xboxftp" and "xboxftp".

------

## Installation

Download the latest Aurora build from [XboxUnity.net](http://phoenix.xboxunity.net/#/news) and extract the files into a new folder named `Aurora`. Copy this folder to your Xbox 360's hard drive. Launch the Aurora.xex  to start the dashboard, or set it as your default dashboard using [DashLaunch](https://360.consolemods.org/software/utilities/dashlaunch.html).  

## Controls

- **A**: Enter / Confirm / Launch
- **B**: View Settings / Back
- **X**: Browse/Search games / Select multiple files or folders in file manager
- **Y**: Game details / Sync windows' working directories in file manager
- **Start**: Settings
- **Back**: System info / tools
- **LB/RB**: Change content category
- **LT/RT**: Scroll through content (fast)
- **Left Thumbstick**: Scroll through content (slow)
- **Right Thumbstick**: Peek left/right
- **DPAD**: Move left/right

## Game Launcher (CoverFlow)

The game launcher is a horizontal list of games that you can scroll through. In order to see covers, you have to set the path setting to point to the folder(s) that contains your games/homebrew.

## View Settings (B)

### Filters & Sort

This section allows you to filter the content that appears in the  game launcher by type or favorites. You can also set how the titles are  sorted. Clear All will reset all filters.

### Quick View

This section allows you to construct filtered categories that you can quickly switch to in the game launcher. Select Add to create a filter  and sort view. You can disable categories here as well.

### Theme

This section allows you to modify the current theme's settings. By  default, you can change the colors and speed of the aurora in the  background by selecting "Override Defaults" and "Configure". You can  also change the background image by placing a JPG/PNG/DDS into  .../Aurora/User/Backgrounds and pressing X to refresh. The Cover Layout  allows you to choose how the game covers are displayed and animated in  the game launcher.

### Skin

Allows you to change the skin you are using. A skin is essentially a  bundle that includes backgrounds, animations, and cover layouts.

### Display

Allows you to change the horizontal/vertical overscan, toggle  letterboxing on 4:3 displays, toggle whether your profile picture/avatar are shown, or turn on an RSS feed of the newest forum posts in a ticker at the bottom of the screen.

## Browse (X)

This section allows you to view all of your game titles in a text list, mark games as favorites, and search your game titles.

## Details (Y)

This section, when hovering over a game, shows the details about the  game such as a synopsis of the game, the rating on the Xbox Live  marketplace, and when you last played the game. From this menu, you can  choose an option on the left hand side or press left on the DPAD to  change the button to different options indicated next to the A button  icon. The alternate options are also listed below:

- **Favorite**: Marks the game as a favorite.

- Launch

  : Launch the game.

  - **Trainer**: Prompts to select a trainer before launching.
  - **Settings**: After enabling Settings Override, you can set patches for the game, as well as "activator" and "trigger" buttons  which act as a button combo to take in-game screenshots. 

- Title Updates

  : Allows you to view installed game updates and download more from the Unity Marketplace.

  - **DLC**: Shows installed DLC.
  - **File Manager**: Opens the file manager to the game's directory.

- Achievements

  : Shows the game's acheivements

  - **Saved Games**: Lists all of your game saves.

- Preview

  : Shows game preview images (if it has any).

  - **Screen Captures**: Shows any screenshots you took.
  - **Refresh**: Redownloads all metadata for your game. This will override the game cover.
  - **Download Cover**: Shows a list of community uploaded game covers to apply.

- Rename

  : Renames the displayed name in the game launcher.

  - **Hide**: Hides the game from the main screen. Useful for hiding backups of games if you plan on modding.
  - **Delete**: Deletes the game and everything in the game directory.

## System (Back)

This section shows various tools and metadata about your temperatures and IP address. 

- **File Manager**: Opens the file manager (more information below)..
- **Scripts**: Allows you to run Lua scripts which you've placed in .../Aurora/User/Scripts/Utility. 
- **Restart**: Restarts Aurora.
- **Reboot**: Power cycles your console.
- **Shutdown**: Shuts down your console. 

## Settings (Start)

### Assets

This section allows you to download metadata from the Xbox Live  marketplace for all games, even from different regions. The Download  button will download them from the selected locale, while the Import  button will import metadata that you place on your local hard drive in the import format below.

### Profile

This section allows you to set an auto sign in profile and add your  username and API Key to connect to XboxUnity. You can get an API key by  registering at [XboxUnity.net](http://xboxunity.net/), then entering your username and pressing the Request button. After  entering your password, it will automatically populate the field below  it.

### Content

#### Title Updates

This section allows you to mass install.delete game updates or set it to automatically scan for updates always. You will need to make an XboxUnity account and request an API key before it allows you to download them.

#### Manage Paths

This section allows you to add folders which will be scanned for  games or homebrew, what type of content is in the folder, and how many  sub-folders deep it should look.

#### Modules

This section shows plugins and the options for each. 

#### Language

This section allows you to change Aurora's language. You can add more languages by placing the language files in ../Aurora/Media/Locales.

#### Security

This section allows you to password protect different areas of  Aurora. Upon choosing Apply, it will allow you to set the passcode if  you do not have one set. To remove the passcode, uncheck all options and choose Apply.

#### About

This section displays the credits and allows you to update Aurora.  The version information shows what version of each component that you  have and what the latest version is.

## File Manager

The file manager uses a classic commander-style interface, but with  each window being in a different tab switchable by pressing LB/RB. The  icons on the left choose standard file management options as indicated  next to the A button icon at the bottom. To exit, browse back to the  root and press B.

## Troubleshooting

- **No Synopsis / Marketplace Rating**
  - Likely your router firewall is blocking the Xbox Live ports for pulling this data. You must forward the ports on your router.
- **Can't play local system link** 
  - You must unload the FreeStyle plugin any time you wish to play local system link.

# Import Format

------

All items are optional.

------

**Metadata**:

> Aurora\User\Import<TitleID>\titlename.txt
>
> Aurora\User\Import<TitleID>\description.txt
>
> Aurora\User\Import<TitleID>\publisher.txt
>
> Aurora\User\Import<TitleID>\developer.txt
>
> Aurora\User\Import<TitleID>\releasedate.txt
>
> Aurora\User\Import<TitleID>\genre.txt 

**Banner**:

> (one of the following)
>
> Aurora\User\Import<TitleID>\banner.jpg
>
> Aurora\User\Import<TitleID>\banner.png
>
> Aurora\User\Import<TitleID>\banner.dds

**Cover**:

> (one of the following)
>
> Aurora\User\Import<TitleID>\cover.jpg
>
> Aurora\User\Import<TitleID>\cover.png
>
> Aurora\User\Import<TitleID>\cover.dds

**Background**:

> (one of the following)
>
> Aurora\User\Import<TitleID>\background.jpg
>
> Aurora\User\Import<TitleID>\background.png
>
> Aurora\User\Import<TitleID>\background.dds

**Screenshots**:

> (one of the following, number up to 20)
>
> Aurora\User\Import<TitleID>\screenshot1.jpg
>
> Aurora\User\Import<TitleID>\screenshot1.png
>
> Aurora\User\Import<TitleID>\screenshot1.dds
>
> OR
>
> (one of the following, number up to 20)
>
> Aurora\User\Import<TitleID>\screenshot01.jpg
>
> Aurora\User\Import<TitleID>\screenshot01.png
>
> Aurora\User\Import<TitleID>\screenshot01.dds> 