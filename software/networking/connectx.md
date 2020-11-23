# Streaming Games over your Network with ConnectX

------

One useful feature of Aurora and FreeStyle Dash is the ability to  stream games over the network using a plugin called ConnectX. This means that you can make backups of your games and store them on a PC, NAS, or any other Samba-capable device and play them without having them stored on your console or external hard drive. ConnectX is an official  development kit tool, so it can not be distributed here.

ConnectX only supports folder format games, not ISOs. You will need  to extract ISOs into folder format by using a tool such as Xbox 360 XISO Extract.

A video demonstration of how to use ConnectX can be found on [Modded Warfare's channel](https://youtu.be/quiuNJG-5lk?list=PLn7ji3VsPy3G08cHNCHyT4Yj-WWYhw8D7).

------

## Computer Setup

Keep in mind that this process **requires** that you have a password set on your Windows account.

1. Press the Start button and search for "Network and Sharing  Center". After selecting it, ensure that your network is set as a "Home" or "Private" network instead of Public. This can be changed by clicking the blue "Public Network" link next to the park bench icon If this is  not correctly set, it will likely block the program from connecting to  your Xbox 360.
2. Create a folder in a location of your choosing to store your Xbox 360 games. Do not include any spaces in the folder name. Right-click  this folder and select “Properties” > Sharing > Share. If your  Windows account isn't already listed here, enter your account name into  the box and select "Add". Once your account is in the list, select  "Share". 
3. Move your Xbox 360 games into this folder. Keep in mind that ISOs are not supported, so you must extract any ISO files into folder  format.

## Aurora Setup

1. Extract and copy the `connectx_patch.xexp` and `connectx.xex` files into your `aurora:\plugins` on your console.
2. Navigate to Settings > Content > Modules, and enable the plugin to start up at boot.
3. In the ConnectX plugin settings, fill out this information:
   - Remote PC Name (**must be all capital letters**)
   - PC Share Name (name of the folder holding your games)
   - User Name (name of your Windows account)
   - Password (password of your Windows account)
4. Reboot your Xbox 360.
5. Press the Back button and ensure that ConnectX is listed in the  plugin list, then select the File Manager button. You should see a  listing for `ConnectX:` in the file manager, from which you  can browse to see the games on your PC. Test to make sure that you can  launch a game by launching the game's XEX file.
6. (optional) If you'd like your games to show up in the main menu  of Aurora, navigate to Settings > Content > Manage Paths, and add a path to the `ConnectX:` folder. 

## FreeStyle Dash Setup

1. Extract and copy the `connectx_patch.xexp` and `connectx.xex` files into your FreeStyle Dash `plugins` folder on your console.
2. In FreeStyle Dash, navigate to Setup > Settings > System Settings > Plugins. Fill out this information:
   - Remote PC Name (**must be all capital letters**)
   - PC Share Name (name of the folder holding your games)
   - User Name (name of your Windows account)
   - Password (password of your Windows account)
3. Select the "Save Settings" button and reboot your Xbox 360.
4. Navigate to Utilities > File Manager. You should see a listing for `ConX:` in the file manager, from which you can browse to see the games on your PC. Test to make sure that you can launch a game by launching the  game's XEX file.
5. (optional) If you'd like your games to show up in the main menu  of FreeStyle Dash, navigate to Setup > Settings > Content Settings > Manage Game Paths, and add a path to the `ConX:` folder. You can do this by pressing Y to open the game path manager, pressing A on the `ConX:` folder, then pressing Y again to select it, and finally pressing X to save your settings.

## Troubleshooting

- Xbox 360 won't connect to the PC
- Check the following:
  - The computer's name should be all uppercase letters in FreeStyle Dash
  - The folder you shared on the PC should have spaces in it.
  - The user account used to share the folder must have a password
  - The account might need admin rights (the account i used did)
  - Disable any firewalls on your PC
  - Restart your Xbox 360 after altering and saving any settings related to streaming
  - Passwords may have been entered incorrectly (they are case sensitive)