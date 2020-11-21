# Disabling Driver Signature Enforcement in Windows 10

------

By default, Windows 10 enforces a rule that only signed drivers can  be installed. Due to the nature of many community-made tools being  unsigned drivers, this may cause issues, notably with JRunner. With this guide, you can reboot into "Unsigned driver mode" which will allow you  to install unsigned drivers until the next reboot.

1. Click Start > Settings > Update and Security > Recovery > Restart now (under Advanced Startup).
2. Click Troubleshoot > Advanced Options > Startup Settings > Restart.
3. When the Startup Settings page is displayed, press 7 or F7 to disable driver signature enforcement. 

Your computer will restart and you will be able to install  non-digitally signed drivers. If you restart your computer again the  driver signature enforcement will be re-enabled.