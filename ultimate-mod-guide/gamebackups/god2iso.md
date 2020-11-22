# Converting a Game on Demand (GOD) to ISO

------

This guide will walk you through converting a Xbox 360 Game on Demand container to an ISO image. A Game on Demand are downloadable games  available on Xbox Live Marketplace. GOD games are convenient, as the  games are installed to the internal hard drive and will show up in  original dashboard, but due to their large file size, it is desirable to convert them to ISO format and store them on an external hard drive.

------

## Requirements

- A Windows PC
- A JTAG/RGH Xbox 360
- [GOD2ISO](http://www.mediafire.com/download.php?o7sf7f8687p7tux) (v1.0.4)
- A GOD game

## Converting to ISO

1. Verify that you have the complete GOD game. The GOD container can be found in /Hdd1/Content/0000000000000000/titleId/00007000 directory and  should contain a 44KB identification file and data folder with data  split into multiple files.
2. Download and launch GOD2ISO.
3. Press "Add..." and select GOD game identification file.
4. Press "Browse..." and select output path for ISO file.
5. Click "GO!" and ISO will be generated in output directory. You will  not get a notification when conversion has finished, but it is finished  when progress bar has reached the far right.

