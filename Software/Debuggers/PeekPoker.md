# Peek Poker

------

Peek Poker is a tool used to view and modify values in live RAM on  your Xbox 360. It is most commonly used for cheats and validating  offsets for use in mod menus or mod tools.

------

## Setup

1. Copy the following files to the root of your Xbox 360 hard drive or a USB storage device:
   - JRPC.xex (or XRPC.xex)
   - RPC.xex
   - xbdm.xex
2. Open DashLaunch and expand the Plugins section. Highlight  plugin1, press A, and navigate to and select xbdm.xex. Repeat the same  process to add RPC.xex as plugin2 and JRPC.xex as plugin3. Press RB,  highlight Flash, and press X to save.
3. Reboot your Xbox 360 and verify that you can successfully connect to your console with [Xbox 360 Neighborhood](https://360.consolemods.org/software/networking/xboxneighborhood.html). 
4. Verify that Peek Poker can connect to your Xbox 360 by entering  your Xbox 360's IP address into the bottom left field in Peek Poker and  clicking Connect. You can find your Xbox 360's IP address by opening  Xbox Neighborhood, right clicking the console, and clicking Properties.

## Usage Example

- This example assumes that you have used another tool, such as [XCE Tools](https://360.consolemods.org/software/debugger/xcetool.html) to find the offsets for a value you wish to change in-game. This  provided example continues the example found on the XCE Tools page which we are trying to change the target value to 900, and we had found the  potential offsets for the target value as:
  - 001: ABCD1234: 57>>62
  - 002: AAAA1234: 57>>62 
  - 003: DAAD0000: 57>>62

1. Enter your Xbox 360's IP address into Peek Poker and click Connect. 
2. Click the "Peek & Poke" button. Enter the address of the  first offset (in this example, ABCD1234) and press the Peek button. This will pull up the location in RAM that the value resides in. In this  example, it will still have the value of 62 represented in hexidecimal  (3E). 
3. Select the found value (in this example, 3E) and change it to  another hexidecimal value such as 63 (900 in decimal) and press the Poke button. If your game is paused, unpause it and see if the value in-game changed as expected. If not, try another potential offset (in this  example, AAAA1234 or DAAD0000). Sometimes, one of these offsets may  visually change the display, but not actually change the value in-game.  In this example, the first offset may change the displayed health  counter value, but in reality, you still have low health and will die  quickly if you take damage. Because of this, you should Poke an offset  and test to make sure it behaves as intended and not just rely on visual changes.

- Note that not all games use static offsets, and the offsets may  change every time you restart the game. If you plan on making a mod  tool, reboot your console and verify that you can still poke the same  offset and get the same results.