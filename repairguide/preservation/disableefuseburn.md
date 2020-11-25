##### You can disable the circuit responsible for burning eFuses, making it  impossible for eFuses to be burned. This also prevents official updates  from being installed, since they cannot successfully burn your eFuses, so it errors out.

## Disabling the eFuse Burning Circuit

Two methods exist to disable the eFuse burning circuit. Both methods involve this area on the bottom side of the motherboard:

![Bottom of Motherboard](../media/WV1xg0UeHv2-WvRavLKp7pfhYxET_fqMMc6ODyrn5uI.png)

### Method 1

#### UT61 Present

If UT61 is present, as shown in the diagram below, bridge the solder  of the two pads in the red box. This process can be reversed in the  future by unbridging the two points.

![UT61 Present](../media/p5xfjvxdLVt3HZTJIPCowHxX6SGWQ-Bm29YkOKlvMKE.png)

#### UT62 Present

If UT62 is present, as shown in the diagram below, bridge the solder  of the two pads in the red box. This process can be reversed in the  future by unbridging the two points.

![UT62 Present](../media/q4ZUi-wIE6nKOOScOQj0xtZ2pVqWjVOJulmeax1747g.png)

### Method 2

The second method to disable the eFuse burning circuit is to remove  the R6T3 resistor on the bottom side of the 360 motherboard as shown  below, ensuring that you don't bridge the two R6T3 pads together. This  process is not as easily reversible as Method 1, as you would have to  buy and solder on another 10k Ohm resistor in order to restore  functionality to the fuse burning circuit.

- Note that if you are on an unmodded console running dashboard 12611, you will receive an E80 error if this resistor is missing. 

![R6T3](../media/yUByZ-14nvQnP_WBVZV1fz8BUo4igOSyLzDU8Z4bP6g.png)