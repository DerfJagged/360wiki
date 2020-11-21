# Custom Boot Animations (Fakeanim)

------

With a RGH/JTAG console, you are able to apply a custom boot  animation in place of the standard boot animation, whether it be your  own or a pre-made one. It is recommended to keep a backup of your  original boot animation in case something were to go wrong. Note that in order to revert back in an extreme case, you would need to flash your  NAND through Xell.

A video demonstration of how to install FakeAnim can be found on [MrMario2011's channel](https://youtu.be/v6odqtntV1o?list=PL1CadovfabPskGb2Ur4kBGzD5s7DzQw5I).

- Any video can be used for a custom boot animation so long as it is a `.wmv` file of 1080p resolution or lower.

------

## Installing a Custom Boot Animation

1. Download [fakeanim](https://www.mediafire.com/file/dxlzj5m2hj6zsvz/FakeAnim_v0.60b.rar/file). In the jukebox folder, you will see a few boot animations you can use.  The one called "Bootanim Fall 2010.wmv" is the latest stock boot  animation.
2. Choose a boot animation from the ones provided or add your own and delete the ones you don't want. 
3. Move the entire fakeanim folder onto the root of your hard drive on your Xbox 360 using FTP or a flash drive.
4. Launch DashLaunch and navigate to Paths > fakeanim. Press A  and browse to your fakeanim folder and continue through the folder until you get to fakeanim.xex and select it. Save your config by pressing X, and reboot. The original Xbox 360 boot animation will  play, followed by a red screen, and finally your own animation. If your  animation does not play, retry starting at step 2.
5. To optimize the fakeanim, open the fakeanim.ini file in the  fakeanim folder. The "delay" value is how long the Xbox will wait before playing the animation. The red screen indicates waiting, so you should  change the "delay" value to a lower value to have your Xbox boot up  quicker but not so quick that your TV isn't ready for it. Phat consoles  likely will be around a value of 5, and slim consoles around 10. Use FTP or a flash drive to move this to the fakeanim folder on your Xbox 360  hard drive, replacing the old one and reboot to see the result.
6. When you've found a good balance where there's very little red  screen, change the "calibration" value in the fakeanim.ini file from 1  to 0 to turn off the red screen, and use FTP or a flash drive to move  this to the fakeanim folder on your Xbox 360 hard drive, replacing the  old one.
7. Using either FTP or a file manager, open your Flash (also known  as SFC in some dashboards) and make a backup of bootanim.xex onto your  PC or flash drive, and then delete the original. Now, only your boot  animation will play.

- On Freestyle Dash, you will need to enable File Manager Advanced  Mode under Setup > General Settings in order to see the Flash.