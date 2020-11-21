# eFuses

------

Electronic fuses, or eFuses, are tiny circuits embedded in the CPU.  Like a fuse in a house circuit, an eFuse is a metallic bridge that, when exposed to too much power, physically burns out and is permanent. Every official dashboard update burns some eFuses, making a permanent record  of what dashboard version you are currently on, and it will check this  record to make sure that you aren't installing a dashboard older than  the one you're currently on, making it impossible to downgrade.

Fortunately, with RGH/JTAG exploited consoles, NAND images made with XeBuild will skip the eFuse check and will not burn eFuses.