# RGH1 - Phat Non-Xenon Consoles

------

RGH1 is for Phat consoles with dashboard 14699 and lower. It uses CPU_PLL_BYPASS to slow down the CPU.

## Equipment Needed

- Coolrunner Rev A/B/C/D
- A PC running Windows Vista or later
- A soldering iron, solder, and flux (MG 835 recommended)
- Isopropyl alcohol (91% or higher recommended) and cotton swabs
- NAND-X or JR-Programmer
- [J-Runner with Extras](https://cdn.octalsconsoleshop.com/J-Runner with Extras.zip)

## NAND Setup

1. Follow the [NAND-X and JR-Programmer page] to Read the NAND as instructed.
2. In the upper right of J-Runner, select the "Glitch" radio button.
3. Click "Create ECC" and select your motherboard type if prompted.
4. Click "Write ECC".

## Soldering to the Motherboard

1. Affix the Coolrunner on the A/V port with the  solderpoints facing towards the fan cutout.
2. Solder the GND wire to the A/V port
3. Solder 3v3: [Diagram](https://i.imgur.com/Y5p0dxP.jpg)
4. Solder A: [Diagram](https://i.imgur.com/lmVSZZi.jpg)
5. Solder B: [Diagram](https://i.imgur.com/pMlJpmS.jpg) There are 2 points boxed, either can be used.
6. Solder C: [Diagram](https://i.imgur.com/WEFEjMr.jpg)
7. Solder D: There are 2 options for D.
   - R8C2: Performs better [Diagram](https://i.imgur.com/vXi9LgC.jpg)
   - J8C1: Easier to solder [Diagram](https://i.imgur.com/Cp2OBF3.jpeg)

## Programming the Glitch Chip

1. Plug the cable from your programmer into the Coolrunner.
2. Set the switch on the front edge of the Coolrunner to "PRG".
3. Open J-Runner with Extras
4. Click "Program Glitch Chip" in the upper left
5. On the Phat RGH1/RGH1.2 Tab, select the [radio button for your board](https://i.imgur.com/Y8x7XsZ.png).
6. Click "Program".
7. When complete, unplug the cable from the Coolrunner and set the switch back to "NOR".

## Decrypting the NAND

1. Connect Ethernet and power on the console.
2. The Coolrunner should blink once or more times, and then the console should start into XeLL RELOADED.
3. Once XeLL finishes, it will display your CPU key and some other info. There is also an IP address.
4. Put the IP address into the box on the lower right of J-Runner and click "Get CPU Key".
5. J-Runner will pull the info from the box, and decrypt the NANDs automatically.

## Generating and Writing Hacked Image

1. Power down the console, and connect your programmer to the motherboard.
2. In the upper right of J-Runner, ensure the "Glitch" radio button is still selected.
3. Click "Create XeBuild Image". This will take a few moments.
4. Click "Write NAND".
5. Disconnect your programmer when the process completes.

## Finishing Touches

1. Boot the console several times and ensure it boots consistently. If  not, make sure your wiring is clean and neat and avoids noisy area. Run  the wires near the X-Clamps for best results.
2. Remove your NAND programmer wires and clean the points.
3. Clean all flux off the board.