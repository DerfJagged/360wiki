# XLink Kai

------

[XLink Kai](https://www.teamxlink.co.uk/)  is a system link tunneling application for consoles that allows you to  play with other users on the Internet as if you were on the same LAN.  Any System Link enabled game can be played online through the XLink  orbital servers. For original Xbox games, Xbox 360 Xlink Kai users can  play with original Xbox users on XBSlink if the game host has both  applications running. Official instructions for setup can be found in  the [XLink Kai Quick Start Guide](http://web.archive.org/web/20160802134730/http://www.teamxlink.co.uk/quickstart.php).

- You can find a list of games that support System Link [here](https://en.wikipedia.org/wiki/List_of_Xbox_360_System_Link_games).

------

## Patching Ping Limits

You must launch [DashLaunch](https://www.reddit.com/r/360hacks/wiki/dashlaunch) and enable the Network > pingpatch setting in order to play Xbox 360 games with people over the internet who have 30ms ping from your  location. Original Xbox games do not have this limitation.

## Register an XTag

Your XTag (similar to the Xbox Live Gamertag) is your username while  using the XLink services and is your way of telling the world who you  are. To get yourself registered, visit [the signup page](https://www.teamxlink.co.uk/?go=register).

## Download and Install XLink

The XLink Kai application can be found [here](https://www.teamxlink.co.uk/?go=download). 

## Console Setup

Unless you have a wireless card capable of entering promiscuous mode, it is required that the PC you are running XLink on will need to be  connected to your router with an ethernet cable. Even in the case where  you can use wireless, it is best to use a pure ethernet connection to  reduce latency. A full list of ways to set up your network can be found  in the official [Quick Start Guide](http://web.archive.org/web/20160802134730/http://www.teamxlink.co.uk/quickstart.php).

## Port Forwarding

Before you can use XLink, you will need to either enable uPnP in your router configuration page if it is supported, and set the XLink  settings to use port 0 OR you can forward the required port by assigning a static IP address in your Xbox settings and by forwarding port 30000  (UDP). A guide to port forwarding on your router can be found on [PortForward.com](http://portforward.com/).

## Using XLink Kai

The XLink online service is broken up into region, consoles,  categories (such as "First Person Shooters" or "Racing"), and individual game arenas. You must be in the same game arena as another person for  them to show up in your System Link match list on your Xbox. You can  also create private passworded arenas to prevent random people from  joining in by clicking the pencil icon in the Web UI. 

## Troubleshooting

##### Firewall and Antivirus Issues

Certain software firewalls or antiviruses (specifically Zone Alarm)  may block XLink from running properly, or disconnect you when you  attempt to join a game. You can fix this by adding XLink as an exception in your firewall or antivirus, or by disabling them while playing.

##### Can't See Other Players

Assuming port 30000 (UDP) was successfully forwarded, this may happen due to being on a different orbital server as the other players. You  can change your orbital server by right clicking the XLink icon on the  system tray and choosing the other orbital. Also check that your network is set up properly and that PAT is turned off in XLink's configuration  menu. Sometimes changing orbital and then changing back will help.

##### XLink Crashes

An incorrectly forwarded port can cause this. Double check your port  settings, or if you are using uPnP, try setting it manually.

##### XLink Can't Detect your Xbox

Try entering your Xbox's MAC address into XLink's properties. You can also try restarting your router if you had changed your network layout.

##### It is stuck on "Querying Orbital Mesh"

Try to connect to a different orbital. If it will not connect to  either orbital, it is likely a firewall or antivirus blocking you.