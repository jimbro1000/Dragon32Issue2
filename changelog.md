# Revision 1.8 #
# Unpublished

* Fix rebase/merge errors from between 1.6 and 1.7
* +5v and -5v fixed (again)
* CL7 footprint design updated 
* RV3 moved for clearance
* Migrate to Kicad 7
* Chome subcarrier of IC9 used instead of chnB

# Revision 1.7 #
# Published 14/01/2023 

* Add missing lumcontrol trace
* Correct carry trace between block A and B of IC32
* Revise position and orientation of IC17 and IC18
* Rework traces for all RAM wiring including ground plane provision
* Use suitable footprint for C7
* Update README with notes on using 4164s instead of 4116s
* Correct +v on IC25 from +5 to +12
* Reverse DAC ladder output from IC35
* Revise resistor values for line pulse padding

# Revision 1.6 #
# Published 08/11/2022

* Fix RL1 footprint
* Redesign PL7 mounting points
* Fix PL6 connections
* Improve trace spacing to reduce crosstalk
* Add secondary video amp bypass circuit
* Reposition RV1 to improve access for adjustment
* Change C7 footprint to accomodate trimmer
* Change TR1 footprint to use wider pitch
* Improve silkscreen text for clarity

# Revision 1.5 #
# Published 15/10/2022

* Fix incorrect wiring on C10
* Fix connection between IC35 and IC20 CB2 <-> STy
* Fix connection between IC25 and IC26 PA7
* Fix GND bias on IC10 to use -5V instead of 0V
* Fix R4 to use -5V instead of 0V
* Fix schema error on IC15, reversed Q and E
* Updated C11, C13, C24, C28, C37 to use polarized footprint
* Updated footprint for cartridge port PL7
* Moved board mounting holes to ease fitting
* Moved C43, C58, C59, R66
* Review passive component values vs original board
* Added more detail to front and back silkscreen
* Changed RL1 to use footprint for available part
* Changed RV1 to use common bourns footprint
* Aligned DIN sockets to edge of board (slight overhang)
* Identify parts with DigiKey part numbers for verification
* Trimmed bottom of board

# Revision 1.4 #
# Published 30/09/2022

* Revise positions of IC1-8 and IC16 for compatibility with original riser board

Note: this is not a tested working board. For evaluation only