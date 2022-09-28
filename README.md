# DRAGON 32 CPU Issue 2 #

This project is a recreation of the SA2120 CPU Mainboard 
for the 1982 Dragon Data **Dragon 32**

Everything (excluding modifications) is taken from the SA2120
schematics. Component positioning is as close to the original
too *but* the memory ICs (1-8) are rotated 180 degrees and may 
not be the same spacing. IC16s position is unchecked. Using an
original expansion board for memory will result in the, already
delicate, chips being fried. Use 4164s instead and set the
memory configuration jumpers appropriately

The two ROMS will need to be sourced from original boards or an
adapter used to allow the use of modern, available EPROM or EEPROM
components

The variable resistor (RV1), motor relay (RL1) and trim capacitor
(C7) are adjusted for modern, available components

## Experimental Revision ##

This update attempts to convert as many components as possible to
modern SMD while rearranging the board to try and minimise routing.
This has not been completely successful but has freed up a large
chunk of real estate on the board. Further refinement may follow
to convert the RAM section to modern SRAM

This update also converts the two roms to a single EEPROM with
switchable banks (effectively 4 different ROMS can be selected
from the EEPROM)

## Caveat ##

The scans on the original SA2120 schematics are not always clear
and it has taken a fair amount of careful study to get everything
correct but there is no guarantee at this time that the board 
design is as intended

All unpolarised capacitor positions are using a simple bead type
footprint which should suffice for modern components

Revision 1 of this board is effectively untested and unproven

## Modifications ##
### Joysticks ###

The two joystick ports provide a second fire button capability
wired to consecutive keyboard rows, as per the Tandy CoCo. 
Unless a two button joystick is used this make no difference to
the operation of the computer. It also requires the use of 6-pin 
DIN sockets, these are pin compatible with the 5-pin originals
so a regular single button joystick can still be used.

The two extra buttons can also be disabled by omitting L3 and L4

### Parallel Port ###

An extra jumper has been introduced to bypass the logic inverter
on the STROBE line. When bypassed the parallel port should 
operate as a communication port for DRIVEWIRE

### Memory Addressing ###

The board is configurable between 32k and 64k ram addressing
using jumper 13/14. Position 13 is for original 32k ram
configuration, position 14 is for an upgraded 64k ram. Note
that this then requires removal of some additional passive 
components and assumes that suitable 64k x 1 ram chips are 
fitted in IC1 to IC8.

Jumper 9/10 has been added for consistency with some of the
other early designs and for compatibility with the 64k
upgrade.

See [World of Dragon: Dragon 32 - 64k Upgrade]
(http://archive.worldofdragon.org/index.php?title=Dragon_32_-_64K_Upgrade)