
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


# Recording perfect Nimbler3 settings from M503
Send: M503
Recv: echo:  G21    ; Units in mm (mm)
Recv: echo:  M149 C ; Units in Celsius
Recv: 
Recv: echo:Filament settings: Disabled
Recv: echo:  M200 D1.75
Recv: echo:  M200 D0
Recv: echo:Steps per unit:
Recv: echo: M92 X80.00 Y80.00 Z400.00 E2924.50
Recv: echo:Maximum feedrates (units/s):
Recv: echo:  M203 X500.00 Y500.00 Z12.00 E120.00
Recv: echo:Maximum Acceleration (units/s2):
Recv: echo:  M201 X9000.00 Y9000.00 Z500.00 E120.00
Recv: echo:Acceleration (units/s2): P<print_accel> R<retract_accel> T<travel_accel>
Recv: echo:  M204 P1500.00 R1500.00 T1500.00
Recv: echo:Advanced: B<min_segment_time_us> S<min_feedrate> T<min_travel_feedrate> J<junc_dev>
Recv: echo:  M205 B20000.00 S0.00 T0.00 J0.02
Recv: echo:Home offset:
Recv: echo:  M206 X0.00 Y0.00 Z0.00
Recv: echo:Auto Bed Leveling:
Recv: echo:  M420 S1 Z0.00
Recv: echo:  G29 W I0 J0 Z0.02249
Recv: echo:  G29 W I1 J0 Z-0.01501
Recv: echo:  G29 W I2 J0 Z0.00499
Recv: echo:  G29 W I0 J1 Z0.02999
Recv: echo:  G29 W I1 J1 Z0.00499
Recv: echo:  G29 W I2 J1 Z0.00499
Recv: echo:  G29 W I0 J2 Z0.00249
Recv: echo:  G29 W I1 J2 Z-0.03001
Recv: echo:  G29 W I2 J2 Z0.01499
Recv: echo:Material heatup parameters:
Recv: echo:  M145 S0 H200 B60 F0
Recv: echo:  M145 S1 H240 B100 F0
Recv: echo:PID settings:
Recv: echo:  M301 P21.13 I2.11 D52.92
Recv: echo:Z-Probe Offset (mm):
Recv: echo:  M851 X30.00 Y10.00 Z-2.31
Recv: echo:Stepper driver current:
Recv: echo:  M906 X800 Y800 Z800
Recv: echo:  M906 T0 E450
Recv: 
Recv: echo:Driver stepping mode:
Recv: echo:  M569 S1 X Y Z
Recv: echo:  M569 S1 T0 E
Recv: ok
Recv


// April 2nd M503
SENDING:M503
echo:  G21    ; Units in mm (mm)
echo:  M149 C ; Units in Celsius
echo:  M200 D1.75
echo:  M200 D0
echo: M92 X80.00 Y80.00 Z400.00 E2700.00
echo:  M203 X500.00 Y500.00 Z20.00 E1200.00
echo:  M201 X500.00 Y500.00 Z100.00 E120.00
echo:  M204 P1000.00 R500.00 T1000.00
echo:  M205 B20000.00 S0.00 T0.00 J0.08
echo:  M206 X0.00 Y0.00 Z0.00
echo:  M420 S1 Z20.00
echo:  G29 W I0 J0 Z0.03500
echo:  G29 W I1 J0 Z0.01000
echo:  G29 W I2 J0 Z0.03500
echo:  G29 W I0 J1 Z0.06750
echo:  G29 W I1 J1 Z0.05250
echo:  G29 W I2 J1 Z0.06250
echo:  G29 W I0 J2 Z0.01250
echo:  G29 W I1 J2 Z0.06000
echo:  G29 W I2 J2 Z0.08000
echo:  M145 S0 H200 B60 F0
echo:  M145 S1 H240 B100 F0
echo:  M301 P16.60 I1.44 D47.90
echo:  M851 X30.00 Y10.00 Z-2.44
echo:  M906 X800 Y800 Z800
echo:  M906 T0 E500
echo:  M569 S1 X Y Z
echo:  M569 S1 T0 E






CR-10S Setup

>>> M503
SENDING:M503
echo:  G21    ; Units in mm (mm)
echo:  M149 C ; Units in Celsius
echo:; Filament settings: Disabled
echo:  M200 S0 D1.75
echo:; Steps per unit:
echo: M92 X80.00 Y80.00 Z400.00 E99.84
echo:; Maximum feedrates (units/s):
echo:  M203 X500.00 Y500.00 Z10.00 E120.00
echo:; Maximum Acceleration (units/s2):
echo:  M201 X1000.00 Y1000.00 Z1000.00 E5000.00
echo:; Acceleration (units/s2): P<print_accel> R<retract_accel> T<travel_accel>
echo:  M204 P500.00 R250.00 T500.00
echo:; Advanced: B<min_segment_time_us> S<min_feedrate> T<min_travel_feedrate> X<max_x_jerk> Y<max_y_jerk> Z<max_z_jerk> E<max_e_jerk>
echo:  M205 B20000.00 S0.00 T0.00 X8.00 Y8.00 Z0.40 E1.50
echo:; Home offset:
echo:  M206 X0.00 Y0.00 Z0.00
echo:; Auto Bed Leveling:
echo:  M420 S0 Z0.00
echo:  G29 W I0 J0 Z0.01999
echo:  G29 W I1 J0 Z-0.02501
echo:  G29 W I2 J0 Z0.20749
echo:  G29 W I0 J1 Z0.04749
echo:  G29 W I1 J1 Z0.00499
echo:  G29 W I2 J1 Z0.17999
echo:  G29 W I0 J2 Z0.05999
echo:  G29 W I1 J2 Z-0.04751
echo:  G29 W I2 J2 Z0.11499
echo:; Material heatup parameters:
echo:  M145 S0 H210 B60 F0
echo:  M145 S1 H240 B100 F0
echo:; PID settings:
echo:  M301 P9.40 I0.78 D28.45
echo:; LCD Contrast:
echo:  M250 C220
echo:; Z-Probe Offset (mm):
echo:  M851 X-60.00 Y-13.00 Z-2.99
echo:; Stepper driver current:
echo:  M906 X500 Y500 Z500
echo:  M906 T0 E300
echo:; StallGuard threshold:
echo:  M914 X90 Y90
echo:; Driver stepping mode:
echo:  M569 S1 X Y Z
echo:; Filament load/unload lengths:
echo:  M603 L350.00 U400.00
echo:; Filament runout sensor:
echo:  M412 S0 D25.00
