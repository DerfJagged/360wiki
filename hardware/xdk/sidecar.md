## Troubleshooting

To fix a sidecar that had a bad FPGA flash (red ring), remove the sidecar. launch Xbox360 Command Prompt, turn the XDK on, set the XDK to default in Neighborhood, plug the DVDEMU port on the sidecar into your  PC via USB, enter `xkd /i:0`, followed by `y`. It will write all 46 blocks and reboot when completed.