# Troubleshooting

------

This page serves as a guide to help with troubleshooting issues with  your console. If you see flashing red lights on the front of your  console, please visit the [**Error Codes**](https://360.consolemods.org/repairguide/errorcodes/index.html) page to troubleshoot.

Many Xbox 360’s made before 2008 have a problem with overheating,  which can then lead to more problems and different errors. If you have  this problem and your console is still under reseller warranty, return  it to your reseller.

------

## Xbox 360 won't Power On

### USB Shorted Out

Check the USB ports in the front (2) and back (1) of the console. If  the prongs of the USB port are bent and touching the case of the port  the USB will short circuit and not allow the Xbox to power on. Try  removing all USB devices to ensure that the device(s) aren't creating a  short.

### Bad Power Supply

If your device is properly plugged in, but the power supply is hot,  unplug all connections and let the components cool for at least an hour. If the problem persists after cooling the power supply, you may need to replace the power supply. Check the Power Supply section below for more tips.

### Bad RF Module Board

If the power supply is fine, the problem may be the RF Module board. If it has been damaged, you will need to replace it.

### Bad Motherboard

If you still have the problems after checking the above, and you don't receive flashing lights on your console indicating an [error code](https://360.consolemods.org/repairguide/errorcodes/index.html), you may have a problem with your motherboard. It is a common problem  for soldered joints on the motherboard to crack. If this is the case, it may be possible to solder or re-flow the connections.

## Xbox 360 won't Read Discs

### Disc Drive won't Open/Close

If your disc drive tray is stuck and will not open, then you have to  manually eject the disc by removing the faceplate and manually ejecting  the drive using a paperclip to spin the gears of the disc drive. If it  also has issues closing, make sure to remove any obstructions if they  are visible, and plug the console back in. Often times, the motor of the disc drive becomes weak and the magnet that holds discs in place will  interfere with the opening of the disc drive. Therefore, it is  recommended to always have a disc inside the console, as this will  prevent the magnet from sealing the drive shut. If the eject button  still doesn't work, you may need to clean or retension the rubber band  covering the gears near the front of the drive by boiling it in water  for a few minutes. Otherwise, your disc drive motor assembly may need to be replaced, keeping in mind that the daughterboard can not be swapped  out without flashing the new drive with the old drive's key.

A video guide for fixing a sticking Xbox 360 drive can be found on [MrMario2011's channel](https://youtu.be/YbdHUFVjjzA?list=PL1CadovfabPskGb2Ur4kBGzD5s7DzQw5I).

### Scratched/Dirty Discs

Discs that are extremely scratched will not be read by the console.  Put a clean, unscratched disc in the the drive. If your Xbox 360 plays  the disc without issue, then the scratched disc was the issue, and may  be able to be repaired by a game shop or pawn shop's resurfacing  machine. Although popular online, it is not recommended to use  toothpaste or a banana to fix scratched discs, though rubbing car wax in small circles on the disc with a microfiber cloth may fill in scratches and help the game be read.

### Dirty Laser Lens

If the problem is not due to a scratched disc, then there might be  dust on the lens of the optical drive that is keeping it from reading  discs. Remove the optical drive from the console and gently cleaning it  using 90%+ isopropyl alcohol and a cotton swab.

### Bad Optical Drive (Open Tray error)

If the Xbox 360 will still not read discs after cleaning the optical  drive, then your optical drive is likely faulty. Adjusting the  potentiometer screw (also known as a "pot tweak") will strengthen the  laser of your disc drive and may help with reading discs, though this  process can be dangerous for your hardware and disc if over-tweaked,  which is common if done without a ohmmeter. Replacing a defective DVD  drive with a replacement DVD drive will not work without flashing the  new drive with the old drive's DVD drive key.

A video guide for how to fix optical drive errors can be found on [MrMario2011's channel](https://youtu.be/OpG08stn9e4?list=PL1CadovfabPskGb2Ur4kBGzD5s7DzQw5I). There is also a more advanced video for [replacing a laser on a phat console](https://youtu.be/c2X7Up-u_WU?list=PL1CadovfabPskGb2Ur4kBGzD5s7DzQw5I).

## Audio/Video Issues

### No Red Lights, but No Audio/Video

Try resetting video settings by holding Y and the right trigger while powering on the console. If you are using a component cable, check that the switch on the console-side plug is set correctly according to your  TV. It could be bad Audio/Video cables, try another set. With HDMI  cables particularly, if they do not have a ferrite core (cylinder tube  on the cable) they are prone to interference, so it is recommended to  try an HDMI cable with ferrite cores. Otherwise, it's likely a GPU or  HANA chip issue which may be fixed by reflowing or reballing the GPU and HANA Chips.

### Audio Cuts Out / Textures Issues

If your audio cuts out, especially during the boot animation, try  going into Settings > Audio Settings, and change it to use Stereo  sound. For some reason, if your destination audio device doesn't support the level it is set at, it may cause the audio to drop out and  texture/memory issues to happen. The hard drive (particularly the cache) are also likely sources of issues, so try clearing the Cache or  removing the hard drive and seeing if the console boots and runs  normally. 

## Power Supply Issues

### No Light

The power supply is not receiving power from your power source. Try reseating both ends of the AC power cable.

### Green Light

The power supply is receiving power and is operating correctly with the Xbox 360 powered on.

### Orange Light

Standby mode. The power supply is receiving power from the power source, with the Xbox 360 powered off.

### Red Light

Power supply fault. The power supply is receiving power from the wall outlet, but is not supplying power to the Xbox 360. Possible causes may be:

#### Incorrect Input Voltage

If the power supply is plugged into a power source that is rated at a different voltage to the voltage stated on the bottom side of the power supply, this will cause the power supply to not operate properly and  can cause damage to the power supply. This problem can also occur if  your power source is experiencing issues such as a brownout. Xbox 360  power supplies are generally rated for 220-240 VAC in NTSC regions or  110-127 VAC in PAL regions. 

#### Overheating

This is most commonly caused by a lack of ventilation. This can be  diagnosed by feeling how warm/hot the power supply is. Ensure that there is a lot of open space around the power supply, that the temperature in the room is cool (not excessively high), and that the ventilation holes on the power supply are free from dust and debris. If the power supply  is in a well ventilated space and the vents are free of dust and debris, check that the fan in the power supply is still functioning properly.

#### Too Much Current Draw

This means that the console is drawing too much power from the power  supply. This is most commonly found in physically modified Xbox 360s,  due to hardware additions (such as excessive LED's, fans, etc) and/or  modifications being incorrectly done. If the Xbox is not modified, this  most likely caused by short-circuit somewhere in the Xbox. The most  common short-circuit is the USB ports being damaged and the pins inside  the port are shorting out or a USB device that is plugged in is shorting the pins.

## Console Reset Codes

### Clear Console Cache

Miscellaneous issues with launching games may be fixed by clearing the console cache. 

1. Press the Guide button on your controller, go to Settings, and select System Settings > Storage or Memory.
2. Highlight any storage device, and then press Y on your controller.  Regardless of which device you select, it will clear the cache for all  storage devices.
3. Select Clear System Cache. When prompted to confirm storage device maintenance, select Yes.

### Clear Failed System Updates

1. With the console off, press and hold the small white Sync button.
2. While holding the Sync button, press the power button to turn on the console.
3. Continue to hold the sync button until the console has booted up completely.
4. During the boot process, the console should clear any failed updates, allowing you to use it normally.

## Miscellaneous

### "Christmas Lights" after Installing a New Keyvault

Xenon keyvaults have a Type 1 keyvault, while all other Xbox 360s  have a Type 2 keyvault. Either type can be used on a Xenon, but a Type 1 keyvault cannot be used on a newer console.

### Issues after Installing DashLaunch Plugin

Turn on your console by pressing the power button, then quickly hold  eject. This will power on your console without loading the plugins  you’ve set in DashLaunch, and will allow you to access your console  normally. You can now reset your DashLaunch plugins or remove the plugin you just set that caused the issues.

### Can't Save Game Data

If your Xbox 360 won't save your game data, your hard drive may be  full or damaged. Make sure the hard drive is connected properly, ensure  there is enough free space for the save, and then attempt to save again. If this does not work, you may need to replace the hard drive. You can  also try plugging in a USB storage device and saving to it instead of  the hard drive to make sure that the hard drive is indeed the problem.

## Sending in your Console for Repair

If none of the above suggestions work, you may need external help. If your console is still under warranty from a reseller or store, return  it. If it is not under warranty, contact Microsoft customer support and  they will fix it for a price. In the US, Customer Support can be reached at 1-800-4-MY-XBOX (1-800-469-9269). Additionally, there are a  multitude of people capable of fixing an Xbox 360, often for cheaper,  and can be found by simply looking for them on local classifieds  websites or by asking local game shops.