# Halo 3 Mods (RGH/JTAG)

------

This page offers options for modding Halo 3. Generally, the most  popular program for modding Halo games is Assembly, which is a direct  replacement for Ascension and Alteration. The program Adjutant is used  to view map geometry in 3D.

**All tutorials on this page require you to have the Halo 3  installed on your Xbox 360's hard drive, the Xbox 360 XDK installed on  your PC, xbdm.xex on your hard drive and added as a plugin in  DashLaunch, and `contpatch` disabled in DashLaunch. This XDK cannot be legally distributed.**

------

## Applying XEX Patches

1. Download the [XEX PPF patches archive](http://www.xboxchaos.com/files/file/113-halo-3-ultimate-xex-ppf-patches/) and extract it on your desktop.
2. Copy `default.xex`, `waveShell-Xbox.dll`, `wavesLibDLL.dll`, and a folder named "waves" from the Halo 3 folder on your Xbox 360 to  the extracted folder on your desktop. Right click each file (including  the ones in the waves folder), select Properties, and uncheck the  "read-only" checkbox if it is checked and press OK. 
3. Run start.bat, press a key to start it, ensuring that you read  everything that pops up on the screen. It will have a single error about a missing `default.xexp` file. 
4. (Optional) If you wish to apply a title update to the XEX, note the Media ID line and plug it into [Xbox Unity](http://xboxunity.net/) to download the latest title update. Use Modio/Horizon or download [Velocity](https://www.mediafire.com/?mbr944kv9dp8c) and select File > Open > Package, and choose the update. Extract the update to the TUfiles folder.
5. Run start.bat again, and check that the two Media IDs match.  Ensure that no errors occured, and press a button to start. It should  indicate success by saying "Successfully wrote altered xex to  topatch.xex". This means that it successfully patched your default.xex,  and a backup of the original default.xex was made, named  default.xex.bak. 
6. Press any key to continue. You should see another message  indicating "Patching... Successful" and "Successfully wrote altered xex  to..." with the game's name or ID. Verify that there are no errors, and  press any key to close the window.
7. Copy the generated XEX file, `waveShell-Xbox.dll`, `wavesLibDLL.dll`, the "waves" folder to your Halo 3 installation directory on your Xbox  360. It will prompt you to overwrite the existing files, select Yes each time.

## Assembly

Assembly is a program that modifies Halo cache files (.map).  Essentially, while any map is running on a console, it is using a cache  file which contains all of the variables ("tags") for the currently  running map including references to sound effects, models, visual  effects, objects and their properties, map geometry (BSPs), and more.  You can use Assembly to explore and change these variables and save an  "offline" copy of the .map to use in place of the original .map file on  the Xbox 360, or you can modify a .map and "poke" it to the console,  meaning that the variables in the running map on the console will be  updated live. 

The tutorials here are an expansion of [Lord Zedd's tutorial](https://www.xboxchaos.com/topic/4518-map-modding-getting-started/).

### Installation

Download Assembly from the [Assembly GitHub](https://github.com/XboxChaos/Assembly/). It is *highly* recommended to compile the latest build, as the pre-made release  version (found under Releases on the page) is from 2016 and many things  have been added.

Afterwards, create a folder called "Maps" in your Assembly  installation directory, and another called "Backup". Copy all of the  .map files from your Halo 3 installation directory (under the "maps"  folder) into Maps on your desktop and a second copy into Backup. The  Maps folder will be the sandbox in which you will make modifications to  the map files, while the Backup folder will be a clean backup of each  map in case you want to revert changes by copying the backup .map into  the Maps folder.

### Applying Map Patches

Note that applying patch files will require that you have patched the game's XEX file and (unless otherwise specified by the mod creator) the latest title update.

1. Double-click the downloaded patch to open it in Assembly, or open Assembly and select Tools > Map Patcher > Apply Patch.
2. Select "..." next to the Patch File field and choose the patch. The patch's file extension should be `.asmp`, `.ascpatch`, or `.patchdat`. Information about the map patch will populate. 
3. Select "..." next to the Unmodified Map field and choose the  corresponding map for the patch. If you aren't sure what map you're  supposed to use, it should say it at the bottom of the screen next to  Patch Target Map.
4. Select "..." next to the Output Map field and name it what you would like. The maps *do not always* have to have the same name as the originals, so consult the patch  release post to see if you can just add it to your maps list without  replacing one. 
5. Some patches will have an extra checkbox asking if you want to  use the extra data folder. Go ahead and check it, as without it, the  patch will likely not work. 
6. Select the Apply Patch button at the bottom of the window. It  will generate a new map file. Place this in the ".../maps" folder on  your Xbox by copying it over with FTP or a USB storage device.

### Troubleshooting

- **Modifications on Forge item tags are not applying when poked**
  - Some tags require that you re-spawn the object you have modified or restart the round / match. 
- **"Players Failed To Load Content" in lobby**
  - If the error pops up near instantly, the .map could not be found. If you applied a patch, open the .mapinfo file that came with it in  Assembly (if it exists) and check that the file name matches the name  found in the "Map Filename" field. Change it to match and restart Halo 3 and see if it works. Alternatively, if it's a campaign patch, try going to the Campaign lobby first to allow your system to load campaign.map,  then change to a Custom Game / Forge lobby. 
  - If the error does not pop up near instantly, or loads partially /  restarts loading a few times, you either are running an unmodified XEX  or have contpatch enabled in DashLaunch. If the map had a custom  .mapinfo and you were able to see and select it, then your XEX is fine  and it's likely that contpatch enabled.
- **Black Screen/Frozen Loading Animation**
  - It is likely a bad patch, botched application of the patch, or a  corrupt download. Re-download and re-patch the map. It could also be a  bad shader if you modified shaders on the map.
- **Dirty Disk Error**
  - Either something is wrong involving the map's raw data or the Map ID in the .mapinfo and .map does not match. Open the .mapinfo in Assembly  and get the Map ID value, then open the .map and check the top of the `scnr` tag, replacing the Map ID value if it is different. 
- **Kicked Back To The Main Menu After Load Screen**
  - The build string of the .map does not match any of the ones listed  internally in the XEX. Update to the latest title update and it should  work, or manually edit the build string with a hex editor.
- **Others Can't Join Your Game**
  - Make sure everyone has the same .map as you do. Some mods, such as  .map mods (excluding live variable poking), will only work if everyone  has a RGH/JTAG exploited console and the same assets.

### Glossary

 

| Term        | Definition                                                   |
| ----------- | ------------------------------------------------------------ |
| Plugins     | Add-ons for Assembly that define the layout and content of tags. Updated plugins can define more unknown values, thus allowing  you to do more in Assembly. |
| Tags        | Variables in a map. Every object is a tag, and has tags in them that define the model, sound effects, their behavior, etc. |
| Tag Classes | Each tag belongs to a class. For instance, every weapon is in the `weap` tag class. Each item in a class have the same tags and layout as every  other item in a class, whether it uses the values or not. |
| Tag Blocks  | Tags in an item are generally grouped into collapsible tag blocks so that relevant information is grouped together. |
| TagRef      | Tag Reference. Found in tags, they are used to  reference another tag. For example, a weapon tag contains a tag  reference to its projectile, which is another tag. |
| Locales     | Refers to the text in a map. Locales can be modified in the "Strings" tab in Assembly, split up by language, and then further  split up via UNIC tags by application. Each locale is also paired with a StringID so they can be referenced in tags. A StringID can be attached  to more than one string, granted the strings are in different UNIC tags. You are limited to the contents of the UNIC as far as replacing, but  you are free to add to it with the String Editor. Changed strings can  only be applied to an offline .map file, and cannot be poked to a  running session. |
| StringID    | A label of sorts found in tags. Comes in 2 flavors, and are made up of a 32 bit index value. Global StringIDs are always the  same value between each map and used by the XEX for various reasons.  Standard StringIDs that are made up of things unique to tags, like  object names or object variants. |

 

| Tag Class | Definition                                                   |
| --------- | ------------------------------------------------------------ |
| SCNR      | Scenario. The backbone tag of an individual map,  defines all the basic information for the map like object spawns, AI  spawns, death barriers, forge palettes, scripts, and more. SCNR  references more crucial tags like the maps SBSPs and Lightmaps. You  typically can't poke anything here without restarting the mission with  the start menu or poking a checkpoint reload byte in multiplayer. |
| MATG      | Global variables. Defines common values that are the same in each map, such as which biped you play as and your movement speed. |
| MULG      | Multiplayer Global Variables. Defines common  multiplayer values that are the same in each map, such as the forge  biped and team colors. |
| WEZR      | Game Engine Settings. Defines the default gametypes,  allowing you to modify typically more settings than what is displayed  ingame. Starting with Reach, only Forge and Firefight remain, where the  standard gametypes got moved to external files in VTGL. Regardless, you  want to edit the WEZR found in the main menu, as that is the only place  it matters. |
| HLMT      | The name is deceiving, it is not actual object models,  but rather the base of all objects. HLMT defines things like variants  and health. It also contains the references for the rest of an object,  specifically the MODE, JMAD, PHMO, and COLL. |
| MODE      | Object models. This tag references the shaders, applies the model raw data, and defines the regions, nodes, and markers. |
| JMAD      | Model Animation Graph. This tag defines all the  animations of a model. A lot of animation data is raw data so there  isn't too much you can edit here besides swapping or inheriting. |
| PHMO      | Havok engine physics models. Powered by Havok this tag  makes models solid to the world. It also defines constraints for limbs  as well as controls gravity lifts and man cannons. [More information can be found here](http://www.xboxchaos.com/topic/4389-about-physics-models-info-forge-20-making-things-solid/#entry34436). |
| COLL      | Collision Model. This tag makes models solid to things like bullets. |
| SBSP      | Scenario Structure BSP. This tag, alongside sLdT (and  Lbsp starting in ODST onward) apply the rawdata for the world itself,  meaning its model. Not much to edit here for most people besides  shaders. |