# Xbox 360 Neighborhood

------

Xbox 360 Neighborhood (or Xbox Neighborhood for short) is an official Windows extension tool that is meant to be used with development kits,  but also can be used on RGH/JTAG exploited consoles. The tool allows  basic FTP features as well as live peek/poking of values and running  executable XEX files remotely. Xbox Neighborhood is often used for  modding as it provides a simple interface into your console.

A video demonstration of how to install Xbox 360 Neighborhood can be found on [Modded Warfare's channel](https://youtu.be/aqmO-T7LlTc?list=PLn7ji3VsPy3FCoZ5E3zWz5tS5iWbysPZX).

**Note: Since Xbox Neighborhood is an official Microsoft tool, it can not be distributed. Do not ask for download links.**

------

## Adding a Console

1. Place xbdm.xex on the root of `HDD1:`. If the file `xbdm.ini` is present, delete it.
2. Reboot your console, and launch Xbox 360 Neighborhood on your PC.
3. If not automatically prompted, select "Add Xbox 360".
4. Enter the console name (default "Jtag") or the IP address. It will add the console into your Xbox 360 Neighborhood window.
   - You can change the icon and name by editing the "xbdm.ini" file that is generated in the root of HDD1. Valid names are `black gray blue white nosidecar`.

## Taking a Screenshot

To take a screenshot, simply right-click your console and select "Screen capture".

## Executing an XEX

Double-click on your console to browse its files. Locate the XEX you want to launch and double click it.

## Troubleshooting

- Hang/Crash
  - Crashes are inevitable in Xbox Neighborhood. When they happen, they  will also crash explorer.exe, the interface of Windows. To restore  explorer.exe, press Win+R and type "explorer.exe" and press Enter. You  can prevent it from crashing explorer.exe on Windows 7, by opening File  Explorer, pressing Alt > Tools > Folder Options > View, and  ensuring "Launch folder windows in a separate process" is checked. If  not, change it and press Apply. By default, Windows 10 has this option  checked.