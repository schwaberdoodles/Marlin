
https://www.thingiverse.com/thing:2975949/comments


# Set the home offsets for the ender3 with the 3dfused yaxis upgrade
M206 X-2 Y-0 Z0.0
# Set the probe offsets based on the zesty extruder mount bltouch
M851 X35 Y10 Z-2.0
# Save everything 
M500
# Move to the center of the bed
G1 F5000 X150 Y150 Z1
# Set the Z Offset at the measured value so the print head is close enough to the bed
M851 Z-2.094


# Instructions for setting the Z Offset

M211 S0 Turn OFF the Software Endstops
M851 Z-0.58 Set the z-offset value
M211 S1 Turn ON the Software Endstops
M500 Store the settings to EEPROM
M501 Load the settings from EEPROM

M92 X80.00 Y80.00 Z400.00 E93.00