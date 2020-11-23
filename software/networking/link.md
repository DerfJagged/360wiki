# LiNK

------

LiNK is a system link tunneling application created by Team FSD for  consoles that allows you to play with other users on the Internet as if  you were on the same LAN. It is similar to [XLink Kai](kai.md), except that it does not require another device on the network to be  running a server. Any System Link enabled game can be played online  through the Xbox Unity servers. You will need to visit [XboxUnity.net](http://xboxunity.net) and create an account in order to use LiNK.

A video demonstration of setting up LiNK can be found on [MrMario2011's channel](https://youtu.be/KHr02kthz18).

- You can find a list of games that support System Link [here](https://en.wikipedia.org/wiki/List_of_Xbox_360_System_Link_games).

------

## DashLaunch Settings

Open DashLaunch and under the Network section, set `pingpatch` to Enabled and `devlink` to Disabled. Also disable any Stealth services you may have active  under the Plugins section. Press RB, scroll down to Flash, and press X  to save your settings.

## Dashboard Configuration

### Aurora Installation

1. Under the Unity tab, enter your username and press the Request  button. Enter your Xbox Unity password and it will fill the API Key  field. 
2. Press Start and select the Plugins tab. Ensure the LiNK settings are set as follows: 
   - Enabled: Enabled
   - RSS Feed: Enabled
   - UPNP: Enabled
   - Data Port: 3072
   - Broadcast Port: 3071
3. Press the Verify button on the LiNK settings page. It will report Passed or Failed for each item. If it says Passed for all items, you  are set. If it says Failed for the "UPNP Capable Router" line, you will  need to disable the UPNP setting in the LiNK settings and manually port  forward the ports 3071 and 3072 (both UDP and TCP) on your router. Once  all items show as Passed **except** the "UPNP Capable Router" line, you are finished. 
   - Since port forwarding is different for every router, it will not be covered here. Guides for port forwarding can be found on [PortForward.com](https://portforward.com/).

### Freestyle Dash

1. Navigate to Setup > General Settings > JQE360.com, and  enter your XboxUnity username and password and select "Link Console to  JQE360". 
2. Navigate to Setup > Plugin Settings > F3 Plugin, and set  "Enable LiNK" to "Always On" and ensure there is a checkmark inside of  the box for "Enable UPNP for port mapping".
3. Press the Test button on the F3Plugin settings page. It will  report Passed or Failed for each item. If it says Passed for all items,  you are set. If it says Failed for the "UPNP Status" line, you will need to disable the UPNP setting in the F3Plugin settings and manually port  forward the ports 3071 and 3072 (both UDP and TCP) on your router. Once  all items show as Passed **except** the "UPNP Status" line, you are finished. 
   - Since port forwarding is different for every router, it will not be covered here. Guides for port forwarding can be found on [PortForward.com](https://portforward.com/).

## Usage

Launch your game of choice. Press the Guide button and select "System Link". From here, you will see a list of rooms that you can join and  play with other players. You can also press Y to create a room,  selecting the region and options for your game. A password can be set so that only your friends can join. From there, you should be able to  enter the System Link option within the game and you will see other  users' matches appear.

## Troubleshooting:

- **System Link is grayed out in the Xbox Guide**
  - Try setting up your Unity account again
- **Port forwarding isn't working**
  - Try enabling UPNP on your router (if it supports it) or put your  Xbox 360 in the DMZ making sure that your FTP password has been changed  so that people outside of your network can't FTP into your console.
- **You can't play with others**
  - Make sure you are on the same title update (TU) as the people you  are trying to join. Generally, everybody plays on the latest title  update.