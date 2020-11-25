# Cooling System Improvements

------

Early fat models have issues with cooling that contributed to the Red Ring of Death issue. By default, the Xbox 360 has a poor fan profile,  poor thermal paste, and – in older models – inferior heat sink designs.  If you're console is still under warranty from the seller, it is  recommended that you contact them for a replacement before attempting to fix it yourself. While there are no established "normal" temperatures,  anything under 65°C on idle is considered good, and anything over 80°C  when playing a game is considered dangerous.

- **Some guides recommend "delidding" the console for better  temperatures. While this may lower temperatures, it's extremely easy to  mess up the process and permanently damage your console. It is  considered a last resort method and will not be covered here.**

------

## Replacing Thermal Paste

This process involves opening your Xbox 360, removing the heatsinks,  removing the old thermal paste with isopropyl alcohol, and applying a  new pea-sized blob of thermal paste. It's often easiest to get the old  thermal paste off by heating it with a hair dryer, and swiping it off  with a coffee filter or Q-tips. Keep in mind that, unless your thermal  paste is conductive, too much is better than too little paste. 

## Fan Voltage Mods

On stock consoles, you don't have the option to adjust fan speeds.  However, you can do the 12V fan mod to run the fan always at 100%, which will help cool older model Xbox 360s. This is recommended for early fat consoles, especially for Xenon consoles, as they are the most likely to experience overheating issues and RROD. There also exist tutorials for  9V fan mods using the DVD drive power (like how GameStop refurbished  consoles come), but if the system needs to go over 75% fan speed, it  won't ramp the fan up. These mods are not recommended for RGH/JTAG  exploited consoles since you can achieve the same results through  changing the fan settings. 

To do the 12V fan mod, solder a wire from the "Fan (CPU)" point to  the ground point next to it, and soldering a second wire from the "GPU  Fan" point to the ground point using [this diagram](https://i.imgur.com/XTp3PXW.jpg). 

## Heatsink Improvement

A significant airflow efficiency improvement can be made to the CPU  heatsink by covering the top of it with aluminum foil and keeping it  anchored on by folding slightly over the edges or using electric tape to anchor the foil on the shroud. Do not block the open end of the heat  sink. The same can be done for the GPU, however, due to it being shorter and having less air intake than the CPU heatsink, you should only cover about half of the top of the heatsink so that it can pull in more air.

You can replace the GPU heatsink with a CPU heatsink and cut a hole  in the fan shroud so that you can use foil as part of the shroud to pull air from the entire height of the heat sink. With a second CPU  heatsink, there will not be any room for a DVD drive, so this would be  best on a RGH/JTAG console or on a system with an ODE. You may also want to see [this page](removeodd.md) for your options to stop the power LED from flashing indefinitely. 

## Adding Extra Fan(s)

Often times, people will add extra fans to their console. Popular spots are:

- A single one on top of the CPU heat sink, blowing out of holes cut in the side of the case
- A fan in front of both the GPU and CPU heat sinks to blow air  through the heatsinks into the white sheathing and out of the regular  fan vent
- A external fans mounted directly outside the fan vent - **note that most of these products usually draw power from the console power plug and are known to damage hardware**

## Adding RAM Heatsinks

Occasionally, RROD is caused by RAM or HANA chip failures due to  overheating. You can lower RAM temperatures by over 10C by adding [copper RAM heatsinks](https://www.ebay.com/itm/3Pcs-Heatsinks-Copper-Heat-Sink-Cooling-Cooler-Kit-for-Raspberry-Pi-3-Model-B/222644651898?epid=607890447&hash=item33d6a7c77a:g:BEgAAOSwRFdZum91:rk:1:pf:0) to each RAM chip. The heatsinks generally come with a thermal adhesive on them and do not need thermal paste.

- On the top side of the motherboard, there are two accessible  Samsung/Qimonda/Winbond RAM chips that can use regular RAM heatsinks.
- On the top side of the motherboard, two more RAM chips are under the GPU heatsink that can have thermal paste applied to them, but not RAM  heatsinks. 
- On the top side of the motherboard, there is the HANA chip that can use a regular RAM heatsink.
- On the top side of the motherboard, there is the SouthBridge chip,  which has the Xbox 360 logo and "PSB", "KSB", or "XSB" on it, that can  use a regular RAM heatsink.
- (Phats) On the bottom side of the board, there are four Samsung RAM  chips which can have flat heatsinks applied on them to clear the height  limit. 

## Adjusting Fan Speeds (JTAG/RGH)

While custom dashboards usually have their own fan options, it's best to set your desired fan settings in DashLaunch because it keeps them  applied no matter what dashboard or app/game you are in. Open DashLaunch and navigate to Miscellaneous > System Info > SMC Config  Settings, and set a target temperature for your CPU, GPU, and EDRAM. The optimal value is different per system, but it's generally recommended  to choose target temperatures below 60°C that don't run the fan too  loudly. You can also set the fan at a certain percent instead with the  fan override settings, but this is not recommended.

## Setting Fan Thresholds (JTAG/RGH)

By default, the Xbox 360 will automatically shut off when any  temperature hits 100°C. This value can be changed by making an image  with XeBuild in JRunner and installing it via USB and [XeLL](../ultimate-mod-guide/xell.md). 