# Dumping NAND and Obtaining your CPU Key

------

This guide will walk you through dumping your console's NAND and  obtaining it's CPU Key. These come in handy when updating your system  software and can also help you recover you from a possible brick.

------

## Using XeLL

By default, if you boot XeLL with an ethernet cable is plugged in, it will either pull an IP from your router via DHCP or it will use the  default IP of `192.168.1.99` if you are not connected to a  router. You must unplug any wireless USB adapters if you have them  plugged in, as it will halt the boot process. By entering the IP address shown toward the bottom of XeLL on a web browser, it should pull up a  XeLL Reloaded web page. The following are displayed:

- CPU Key
- DVD Key
- Raw Flash (download): This will download a dump of your flash chip straight to the device you are using. 
- Key Vault: This will download a decrypted keyvault file straight to the device you are using. 
- Fuses: This will download a file listing the status of your CPU fuses straight to the device you are using. 
- Startup Log: This will display a text file of all the events that  have been printed to the screen since boot, some of which you can't  normally see.
- Shutdown
- Reboot

A video demonstration of using XeLL to dump and flash a NAND can be found on [MrMario2011's channel](https://youtu.be/4iKCG6N1FzA?list=PL1CadovfabPskGb2Ur4kBGzD5s7DzQw5I).

## Using Simple 360 NAND Flasher 1.2

### Dumping the NAND

1. Download and launch [Simple 360 NAND Flasher 1.2](http://www.homebrew-connection.org/files/xbox/nand_flasher/dl_Simple_360_NAND_Flasher_v1.2.rar) on your console.
2. Press X to dump NAND. If everything went fine, you should get message saying "NAND Dumped!". Press any button to exit.
3. There should now be a file called "flashdmp.bin" in the Simple 360 NAND Flasher directory. Copy this file to your PC.
4. Download and run [X360 NAND Dump Checker](http://www.homebrew-connection.org/files/xbox/Nand_Tools/dl_x360_NAND_Dump_Checker_GUI v1.0.rar). Press "check NAND" and select the flashdmp.bin file. If the NAND is  fine, then you should see a message saying "NAND Verified as OK!". As  long as the verification is OK, then bad blocks do not matter. If bad  blocks are causing verification to fail, you should go back to step 1  and try to dump NAND again.
5. Store flashdmp.bin to a safe location, preferably outside of your PC (to a cloud, external media, etc). Keep a copy on hand if you wish to  obtain your CPU key with the steps below.

### Obtaining the CPU Key

1. Download and launch the latest [xeBuild GUI](http://www.homebrew-connection.org/files/xbox/nand_builder/xeBuild_GUI/) (currently v2.098) on your PC.
2. Click "Open" and for the "Source File", select your NAND backup (flashdmp.bin).
3. If you know your Xbox 360's IP address type it into "IP to Xell" box and click "Get CPUKey/CFLDV from Network". The CPU Key should be  displayed in its text box.
   - If you do not know your Xbox 360's IP, you can boot your Xbox 360  into XeLL (by pressing the eject button to start the console by default) and go to Tools → "Scan for Xell" and press "Start scanning for Xell".  If your Xbox 360 is in same network, it will be detected and the CPU Key will be displayed in main window.
4. Check "Keyvault Information" in bottom-right corner and verify that  information given is OK. If something seems weird, you could always try  again.
5. xeBuild should have generated a "FUSE.txt" file to same directory  containing your flashdmp.bin file. Store this file to a safe location,  preferably outside of your PC (to a cloud, external media, etc).