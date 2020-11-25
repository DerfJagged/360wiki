# Unbanning your Console

------

When a console is banned, your unique Xbox 360 keys (stored in a  "keyvault" file) are blacklisted from connecting to Xbox Live. With a  JTAG/RGH console, you have the ability to swap out your keyvault for  another one. A keyvault (KV) must come from a legitimate console in  order to be recognized and allowed on Xbox Live. 

------

## Changing Keyvaults

1. You will need to either buy a new keyvault from someone or obtain a NAND dump from another console ([instructions below](extractkeyvault.md)) to extract the keyvault from it. This keyvault should not be shared  with anyone, as two consoles logging in to Xbox Live with the same  keyvault can trigger a ban on the keyvault.
2. Your new keyvault should have a kv.bin and cpukey.txt file. Open  cpukey.txt and copy the numbers and letters next to "CPU key" into a  blank Notepad document. In Notepad, click File > Save As, select the  dropdown menu at the bottom of the window and select "All Files", and  save it with the name `cpukey.bin`.
3. Put both kv.bin and cpukey.bin on a flash drive and plug it into the console.
4. With a file manager or FTP, open USB0 and copy kv.bin and paste  it into the root of hdd1. Confirm the overwrite if prompted. Repeat for  cpukey.bin.
5. Turn the console off and unplug the flash drive. Power it back  on. The console may reboot itself once or twice to accept the keyvault.  Your console should eventually boot up as normal, and you should be  unbanned.