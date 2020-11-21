# Boxzii / X360DOCK

------

Description here. Boxzii was eventually renamed to X360DOCK.

https://www.youtube.com/watch?v=i3BnAD-elmI

------

## Troubleshooting

- Your model 2 will not turn on
  1. Check that it is powered properly. There are two methods of supplying power:
     - Plugging the module 1 dongle's jumper will power module 2 using XBOX360 energy 
     - Using an external 5V adapter to power (4.5V is acceptable) 2.Your MicroSD is not plugged in correctly or the kernel image isn't  present. Use USBBIT and "RESTORE", choosing the correct ISO for the  latest kernel image.
- Your hard drive doesn't boot 
  1. Use an externally powered hard drive. If it is not externally  powered, it may be drawing more power than the USB port can provide.
  2. Use NTFS format to store ISO images.
- You can't see any cover images on your model 2
  1. Use NTFS format. Make sure that the covers are in the same folder and have the same name as their corresponding ISO (i.e. `Hello_Kitty.iso` and `Hello_Kitty.jpg`). The images must be 180x200 JPGs.
- Your model 2 boots but the console displays an E64 error. 
  1. Store your key.bin/inquiry.bin in the `DATAS` partition of the kernel's MicroSD.
  2. Check your key.bin/inquiry.bin if you're getting "PLAY DVD" on the dashboard.