## Resetting a Parental Lock

------

Often times when buying a console from a third party, it will come  with a parental control set. On an RGH/JTAG, you have the option to look up a code to reset it or modify your NAND to remove the code. On an  unmodified console, you have a few official options outside of just  trying to guess the code.

A video demonstration of bypassing the family settings can be found on [MrMario2011's channel](https://youtu.be/nOdtG7z38us?list=PL1CadovfabPskGb2Ur4kBGzD5s7DzQw5I).

------

## Unmodified Console

On unmodified consoles, your options to remove a parental lock are as follows:

### Official Reset

Open the [Devices page](https://account.microsoft.com/devices) for your Microsoft account, register your console, select the console,  then select More Actions > Reset Passcode. If this isn't possible,  you can call Microsoft's customer support and they will provide you with a reset code. 

### Guessing the Recovery Question

Navigate to Family Settings > Family > Content Controls, enter  the wrong code, and it will prompt you to reset the passcode. It will  ask you a password reset question. Try and guess the answer if you can.

### Guessing the Factory Reset Code

Navigate to System Settings > Console Settings > System Info. Press (don't hold) the following button combination: `LT+RT+X+Y+LB+RB` followed by four more buttons or D-Pad directions out of the list below:

- `Y+A+RT+Y`
- `Y+A+RT+ANY D-PAD DIRECTION`
- `A+A+LEFT+UP` 
- `X+X+UP+DOWN`
- `X+Y+LT+X`
- `ANY D PAD DIRECTION+RT+A+Y`
- `A+A+A+A` 

If the correct code is entered, you will be prompted to reset your  Xbox 360 settings. Select Yes. This will reset all settings but will not delete any of your saved games or other data. If you did not receive  this prompt, enter the entire button combination again from the  beginning with a different code ending.

## RGH/JTAG

### Looking up your Reset Code

1. Obtain a [dump of your NAND](../ultimate-mod-guide/nanddump/index.md) if you don't already have one. 
2. Open JRunner and select the "Load Source" button and choose your  NAND dump. Select Tools > SMC Config Editor. Note the four letters in the field to the left of "Reset Code". 
3. Navigate to System Settings > Console Settings > System Info. Press (don't hold) the following button combination: `LT+RT+X+Y+LB+RB` followed by the buttons corresponding to the four letters. Any instance of "L" or "R" are the left and right triggers. If the correct code is  entered, you will be prompted to reset your Xbox 360 settings. Select  Yes. This will reset all settings but will not delete any of your saved  games or other data. If you did not receive this prompt, enter the  entire button combination again from the beginning. 

### Removing the Parental Lock Feature

1. Obtain a [dump of your NAND](../ultimate-mod-guide/nanddump/index.md) if you don't already have one. 
2. Open JRunner and select the "Load Source" button and choose your NAND dump. Select "Advanced XeBuild Options" and check the `nomobile` box. Press OK to close the window.
3. Select "Create Image". Rename the file to `updflash.bin` and place it on a USB storage device and plug it into your console.  Boot into XeLL, it should automatically find the update and flash it.
4. Reboot the Xbox 360 and the new NAND image should be applied with parental controls disabled.



(how to remove parental controls)

## Default Codes

LT RT X Y LB RB DOWN DOWN DOWN X

LT RT X Y LB RB LEFT LEFT DOWN X

LT RT X Y LB RB RIGHT RIGHT DOWN X

LT T X Y LB RB X X DOWN A

LT RT X Y LB RB X DOWN A Y

LT RT X Y LB RB X X X RIGHT

LT RT X Y LB RB X X Y A

LT RT X Y LB RB DOWN UP UP X

LT RT X Y LB RB DOWN UP DOWN UP

LT RT X Y LB RB DOWN DOWN UP UP

LT RT X Y LB RB LEFT X Y A

LT RT X Y LB RB RIGHT LEFT X X

LT RT X Y LB RB RIGHT X X X

LT RT X Y LB RB RIGHT X X A

LT RT X Y LB RB RIGHT X Y A

LT RT X Y LB RB DOWN Y Y A

LT RT X Y LB RB A RIGHT X LEFT

LT RT X Y LB RB DOWN DOWN X DOWN

LT RT X Y LB RB DOWN DOWN X X

LT RT X Y LB RB DOWN X DOWN DOWN

LT RT X Y LB RB DOWN DOWN DOWN A

LT RT X Y LB RB DOWN UP LEFT X

LT RT X Y LB RB X X DOWN A

LT RT X Y LB RB RIGHT X DOWN X

LT RT X Y LB RB DOWN RIGHT Y X