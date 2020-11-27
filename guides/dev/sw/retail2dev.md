# Convert Retail Console to Devkit Console

Converting a retail console to a development console will help you work on developing homebrew software for the Xbox 360 by providing a test environment which streamlines the development process by allowing access to SDK[LINK NEEDED] features unavailable via Freeboot[LINK NEEDED] or stock NAND. This is done using RGLoader[LINK NEEDED], which is a tool that can build a devkit NAND from a retail NAND dump. The devkit NAND enables debug features not otherwise available on a modified console capable of running unsigned code. This process also installs xshell[LINK NEEDED], the official development dashboard[CITATION NEEDED].



## WARNINGS

- Doing this should increase performance with Xbox 360 Neighborhood[LINK NEEDED].[CITATION NEEDED]
- This may also allow NAND dumps to perform quicker.
- This is **NOT** for people who aren't looking to get into development for the Xbox 360.
- The latest kernel available for this is **NOT** the latest kernel. It is currently on `17150`[CITATION NEEDED]. This means you *will not* be able to go on Xbox Live with RGLoader[CITATION NEEDED]. You will also be unable to play system link[LINK NEEDED] with anyone who does not have either a devkit[LINK NEEDED] or the devkit patch enabled in DashLaunch[LINK NEEDED].
- You will be able to do everything you could with a Freeboot[LINK NEEDED] NAND.
- This can go wrong and brick your console. JTAGs[LINK NEEDED] are especially common to brick.[CITATION NEEDED]
- RGLoader[LINK NEEDED] overwrites XeLL[LINK NEEDED], therefore the only way to revert this is to reflash the NAND[LINK NEEDED] with the XeLL[LINK NEEDED] or stock image[LINK NEEDED].

- Dashlaunch does not work with a devkit NAND.[CITATION NEEDED]
- Fakeanim does not work with a devkit NAND. You will have to remove the `;` and edit the path to your fakeanim in rgloader.ini if you wish to use it.
- By default it will boot into the xshell[LINK NEEDED] dashboard. You can change this by changing the path to a different dashboard's XEX in rgloader.ini

## You will need:

A modified retail console capable of running unsigned code[LINK NEEDED]



## RGLoader.ini settings



## Credits

[Modded Warfare for their tutorial on turning a JTAG/RGH into a DevKit with RGLoader.](https://www.youtube.com/watch?v=YeFZd6R3K90)