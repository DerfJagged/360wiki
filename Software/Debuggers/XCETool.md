# XCE Tools

------

XCE Tools is a debugger similar to Cheat Engine on a PC. With it, you can scan memory ranges to find offsets of specific values within the  game so you can use a peek/poker tool to change them. Finding these  offsets are useful for making cheat tools such as mod menus or Real Time Edit (RTE) tools.

------

## Setup

1. Copy the following files to the root of your Xbox 360 hard drive or a USB storage device:
   - JRPC.xex (or XRPC.xex)
   - RPC.xex
   - xbdm.xex
2. Open DashLaunch and expand the Plugins section. Highlight  plugin1, press A, and navigate to and select xbdm.xex. Repeat the same  process to add RPC.xex as plugin2 and JRPC.xex as plugin3. Press RB,  highlight Flash, and press X to save.
3. Reboot your Xbox 360 and verify that you can successfully connect to your console with [Xbox 360 Neighborhood](https://360.consolemods.org/software/networking/xboxneighborhood.html).

## Usage Example

This example is a hypothetical example using the game Doom 3. In this example, we will set the health counter to 900%.

1. Verify Xbox 360 Neighborhood is connected, then launch  XCE_Tools2.exe. Launch your game of choice and progress through the game until you reach a point in which you can visually see your value, for  instance a health counter. If possible, try and make this value a number that is not `0` or `1` as these are extremely common values and may take longer to find. For this example, we will say the health counter is at 57%.
2. In XCE Tools, change the value of the second Range field to `D0000000`. This will reduce the number of RAM addresses that it will search to a  range that your target value (in this example, our health counter) is  more likely to be in.
3. If your number can only be an integer with no decimal points,  select the "4 bytes" checkbox at the top and the "4 bytes" radio button  on the right side. Otherwise, select "float" or "double". It is  partially guess work as to which type your value is, and it will help  you to look up what the maximum value each type can represent. For this  example, we know that our number goes up to 200 normally, so it is  likely a 2 byte or 4 byte number. We will choose 4 bytes as it is more  common.
4. If possible, pause your game so that less things are being processed and less values are changing in RAM.
5. Click the Init button. The program will begin dumping the RAM of  your console and show a progress bar in the bottom left. The process  will take quite a while. Do not use your console while this is dumping,  as you may inadvertently change the value you are trying to find.
6. In the field next to the "Exact" button, enter the target value  that you are trying to find an address for (in this example, 57) and  press the Exact button. This will remove all values from the RAM dump  that don't match your target value and list the address offsets that  match your value.
7. Do something in-game that will cause your target value to change. Repeat step 6 using the new target value. In this example, we will take damage and the health counter will end up at 62%, so we will input 62.  This will take the list of addresses that had previously had the value `57` and will remove the ones that did not change to `62`. Repeat this process until you are only left with a very small amount (1 to 5) values. In this example, lets assume we are left with:
   - 001: ABCD1234: 57>>62
   - 002: AAAA1234: 57>>62 
   - 003: DAAD0000: 57>>62
8. The offset we want is one of these. Often times multiple offsets  follow the same path of changes as it might be separate variables for  displaying graphics or just a copy of the variable. The only way to  really know for sure which value is the one we want is to manually  change (poke) the value and see if it changes in-game. For this, we can  use [Peek Poker](https://360.consolemods.org/software/debuggers/peekpoker.html).