# Dragon 32 Rev 2 Build Instructions #

## Introduction ##

This is a rough guide on how to assemble the 
Dragon 32 Rev 2 reproduction board. It assumes 
you have collected together all the parts you 
will need using the bill of materials in the 
project repository.

## Preparation ##

Clean the mainboard to remove contaminants, soapy
water first, dry and then a wipe down with 
isopropy alcohol.

Make sure you have a good supply of solder, a
temperature controlled soldering iron. If you
are using lead based solder set the temperature
to between 360C and 370C. The board can tolerate
higher for lead-free solder.

A ready supply of solder flux can be really
helpful if you find yourself having to remove a
component from the board.

You will need short tipped, angled wire cutters
for trimming the component leads after soldering.
Don't cut the leads right down to the board or deep
into the solder.

It is also a good idea to have a multimeter on hand
to check component values and test for any shorts
after soldering.

The project repository on GitHub includes an
interactive Bill Of Materials that allows you to
cross-reference components against position on
the board (and mark off all the parts that you've
fitted). To use this download the ibom.html file
to your computer and open it from the local file
system (this should open up a web browser).

If you can't or don't want to use the iBOM it is
a good idea to print off the Dragon32__Assembly 
PDF on to large form paper and mark the positions 
off from there as they are fitted to help avoid
getting lost.

## Build Order ##

Work with the components with the lowest profile
first - resistors, then diodes, then capacitors,
transistors, etc.

Leaving the chip sockets until last helps as they 
tend to get in the way when fitting other items.

### PAL/NTSC configuration ###

If you are setting the board up to use NTSC you
need to start by modifying JP15/16 and JP17/18.
By default these are pre-bridged for PAL use.
You need to cut the trace joining pads 1 and 2
on both jumpers. Pad 1 is marked with a triangle.

Once the trace is cut, use a blob of solder to
join pads 2 and 3.

To use NTSC you need to provide an adapter to the
VDG that includes an MC1372 NTSC modulator chip.
This replaces most of the discrete logic on the
board.

The output of the adapter board is wired to PL8.
Ground on the left, composite NTSC video on the
right.

The rest of this build assumes you are assembling
for a PAL machine.

### Resistors ###

Fit resistors first making sure the solder is
forming on both sides of the board, not just
the bottom.

Regardless of board configuration all of the
resistors should be fitted.

Save the two potentiometer resistors RV1 and RV2
for later.

### Diodes ###

Fit all 9 diodes in much the same way as the
resistors but making sure the polarity marking
matches the board.

### Inductors ###

If you want to have the option of two button
joysticks (non-standard but used in some
CoCo games) then you'll need to fit all 4
inductors (L1-L4).

If you only want single button joysticks you
only need to fit L1 and L2.

Soldering is the same as for resistors.

### Capacitors ###

If you are using 4164 DRAM chips you need to
miss some components out. C12 and C50-C57
must not be fitted - failing to do this will
result in corrupted memory read and write.

Other than this fit all capacitors making 
sure that the tantalum and electrolytic
capacitors are fitted the right way around.

Tantalum capacitors have a + symbol next to
the positive side. Electrolytic capacitors
have an arrow pointing to the negative side.

The board is marked to show a + next to the
positive side and a filled semicircle on the
negative side.

It is worth saving two of the long legs
after trimming the legs back. You can use
these for securing the crystals.

Save the trim pot capacitor C7 for later.

### Transistors ###

TR1 is an NPN transistor driving the coil of
the cassette remote relay. It uses a wide
TO-92 footprint.

TR2 and TR3 are NPN transistors in the
video amplification circuit.

TR4 is a PNP transistor acting as the
final amplifier in the video circuit.

TR2-TR4 all use a narrow TO-92 footprint.

It may require some leg bending to form
your transistors to the right spacing. 
This is best done with a pair of tweezers
to reshape the legs as needed. Trying to
do this by hand is likely to result in
snapped legs.

Make sure the transistors are fitted the
right way around according to the outline
printed on the board.

### Jumper Posts ###

The board has 7 configuration jumpers. All
of these are 3 posts. Soldering them can
be tricky when trying to get them aligned
vertically. A simple approach is to only
tack a single pin and then adjust the angle
until happy.

If you know the configuration you are going
for and do not wish to change it later you
can safely use a piece of wire to bridge 
the desired contacts.

This is fine for jumpers JP1/2 through to 
JP9/10 but it is recommended to fit the 
three post headers for JP11/12 and JP13/14.

### Connectors ###

The keyboard connector can be vertical or
a horizontal as desired. Original boards
used a vertical orientation but later boards
and the D64 moved to horizontal to avoid 
clashing with the keyboard itself. I
recommend using the horizontal option as
it leaves more space for connectors.

The joystick and cassette port connectors
have an overlapping design, if you want
to get them nicely lined up start with the
5-pin cassette socket and tack it in
place on a single pin.

You can then do the same with the two
joystick ports (6-pin or 270deg 5-pin)
and align them to the edge of the board.
This can be a tricky task so don't rush
it.

The power board connector needs to be 
fitted with the vertical guide towards
the bottom of the board (assuming you
don't have a plain pin header).

The cartridge port connector can be very
entertaining to fit. The pins like to
bend in transit so you'll likely find
yours do not line up on the first attempt.
It is very easy to bend the pins on the
cheaper connectors resulting in the pin
not fitting properly. Double check that
all pins have fitted through the mounting
holes on the board before soldering.

### Variable Components ###

C7 should fit easily but some varistors
have legs that can split into multiple
layers. Make sure that all of the leg
makes it through the mounting holes.

RV1 needs to be fitted at an angle so
that the adjustment side is facing more
upwards. The long, flexible legs of the
part make this relatively easy to 
achieve. If you fit it flush and then
trim the legs before realising you can't
easily adjust it, you will need to
obtain a replacement or work with it
as-is.

RV2 has a top adjustment and can be 
fitted flush to the board but the legs
of the component need to be checked.
Some versions of the part have the legs
in-line while the board expects the
middle leg to be offset. As with RV1
the legs are flexible and be easily
formed to the right configuration.

The orientation of RV1 and RV2 is not
critical, it just changes which way
you turn the adjustment.

### Crystals ###

Assuming you have the larger housed
crystals you will need to bend the legs
so the crystal lies flush with the board.
This is not essential but it is 
recommended. Two additional solder points
are provided for each crystal to allow a
wire to be formed over the body and 
prevent the crystal being moved. A
convenient source for the wire to do this
is the long legged capacitors you 
hopefully saved earlier.

### Sockets ###

When fitting the sockets make sure the
orientation is correct and the notch of
the socket matches the outline on the
board.

Most of the chips are aligned with the 
notch to the top of the board but RAM, ROM
and SAM chips have the notch towards
the bottom of the board.

As with the header pins it can be a 
little tricky to get the sockets to fit
flush and aligned. Tacking one pin at 
each end of the socket to hold it in
place and then heating one pin while
adjusting the position gives a good
result.

Be very careful to avoid bridging the
pins on the socket while soldering.
It is worth checking with a multimeter
to double check as the pins can 
bridge on the top of the board, hidden
underneath the socket.

If you are using original ROMs for U17 and 
U18 it is worth fitting regular double
wipe leaf sockets. If you are using EPROMS
in adapters you can either fit the adapters
straight to the board (definitely recommended
for square pins) or fit turned pin sockets 
(only for round pins on the adapter).

### Before Fitting Chips ###

As a precaution, before fitting the
chips to the board it is worth making
sure none of the voltage pins of the
power board connector are shorted to
ground (that would be bad).

The power connector has the voltages
as +12v, +5v, -5v, Gnd going from
right to left. You don't need to connect
to the power supply to test, you just
need to check continuity between the
power pins and the different power pins
on the various sockets.

If you fit your configuration jumpers
next to the power connector (JP1/2 to
JP9/10) you can make sure the right
voltages are available on the board
by checking for continuity from the 
respective power pins.

The +5v pin is connected to almost
every single chip on the board as Vcc.
On the 74LS logic chips this is the 
upper right pin. The lower left pin
is connected to ground.

The RAM chips take a little more attention. 
For 4164 chips there are  only two power 
pins, +5v and ground. +5V should be the top 
right pin. Gnd should be the lower left pin.

The LM1889 modulator IC9 needs different
voltages, -5V to pin 5 (5th pin down on
the left side) and +5V to pin 14 (5th pin
down on the right side).

The amplifier at IC25 needs +12V on the top
right pin.

The amplifier at IC10 needs -5V on the lower
left pin and +5V on pin 7 (2nd pin down on
the right).

You should also have +5V on the left pin of
R67. You should have -5V on the left pin of
R69. These are the top and bottom resistors
just to the left of the ram bank.

### Bonus Jumpers ###

JP11/12 is used to disable the inverter
driving the strobe pin of the printer port. 
While this is "on" (11) the strobe pin will not 
work for input. If you want to use the
printer port for bit banging a serial port
you will need to disable the inverter by
setting the jumper to the 12 position.

JP13/14 defines whether the board is working
in "half-good" 4164 mode or full 64k mode.
If you only want your board to work as a D32
then set this to 13, if you want to be able
to access the full 64k memory mode (which
will break your ROM access) then set the
jumper to 14.

In effect JP13/14 is the part of the 
memory upgrade mod that requires bodging
and cutting traces between chips.

### Fitting Chips ###

Make sure you have a grounding strap on your
wrist (or ankle) and it is actually connected
to a proven ground point (radiators are a 
good source). The LM1889 and DRAM chips are
very susceptible to static discharge! Leave
these until last.

Fit all your chips paying very careful attention
to orientation, notches must match with the
board. Fitting chips the wrong way round will 
likely destroy them when the power is switched
on.

### ROM Chips ###

If you have original ROMs you fit these directly
to sockets. EPROMs require an adapter board which
probably has a socket on top so the adapter can
be directly soldered to the board, unless you want 
to keep changing them. If you are going to chop
and change between original and EPROMs I recommend
fitting turned pin sockets and creating a sandwich
of regular leaf pin and turned pin sockets for the
ROMs to fit in. This will avoid damaging your
valuable ROMs and maintain good contact to the 
board.

### First Power Up ###

Before turning the power on for the first time it
is worth removing the LM1889 modulator, it provides
the colour signal but the video will work in 
monochrome without it.

When powering on for the first time always be
prepared to turn the power off in a hurry. If it
doesn't show a picture on your monitor it does not
mean it isn't working, you may need to adjust RV1
to bring the output into an acceptable voltage range

If anything smokes or looks to be getting hot, turn
the power off immediately. You most likely have a 
short (you did check for shorts?) or a polarised
capacitor in backwards.

Assuming nothing goes pop you should be able to
adjust the video output to get a stable picture.
If all goes well, turn the power off and reinsert
the LM1889 modulator.

Try the video again and you should be welcomed by
the regular green screen. You can adjust the 
video timing by turning the head on C7. This is
best done with a plastic screwdriver, not a metal
one. When set correctly you should be able to just
about freeze horizontal dot crawl but won't be able
to remove horizontal artifacts.

### Troubleshooting ###

#### No Colour ####
In most cases this will be a failed LM1889. Test
the clock signal on PIN 17 of the modulator. If you
can see a good 4.3MHz signal you should be seeing 
colour. Check RV1 is set appropriately and that the 
colour signal is arriving at R7 (lower leg, not the
top one) and again at R10 (left leg, not the right).

If the signal is getting that far then you likely have
a bad TR2 (or the wrong component, or a short between
pins on TR2 - easily done).

If the signal is not getting to the test points, check
for continuity.

If you are only getting clear colour on alternating
lines the problem will sit with the amplifier at IC10.
This mixes the signal for alternating lines. The chip
is pretty robust but I've seen failures during testing
that left me scratching my head...

#### Garbage Picture ####
There are many, many ways that this can happen. The 
most common cause is a stuck data line, either due
to bad RAM/ROM or a short between data lines or
address lines.

Test your RAM - either in a known good device or
with a dedicated RAM tester (beware that some testers
can show a failure for good chips due to differences
between TTL and CMOS). The ROMs on the Dragon are
generally robust but the same chip type is a common
source of failure on other computers (cough Commodore).
It is worth checking the legs are making good contact
with no sign of corrosion (blackening).

#### No Response At All ####
If the relay doesn't click on powering up (assuming
you fitted one) and there is no picture at all, the
chances are the CPU is not cycling. Either it hasn't
come out of reset or is being locked up by another
line.

A bad PIA can cause the CPU to run very, very slowly
by generating interrupt requests at high frequency.
Try removing the PIAs and try running without them.

Check the reset line is going high (about 5V) and the
same again for halt, mrdy, extal, xtal, bs and ba pins.
If any of these are low it can stop the CPU operating.

Check the Q and E pins are oscillating at (about) 
0.9MHz, no clock means no CPU. You can also check
the SAM is receiving the full 14MHz clock from the
crystal.

If all is well with those pins, test the address and
data lines with an oscilloscope or logic probe. You
should see activity with the lines moving from high
to low.

If the CPU is doing nothing it may be faulty, either
test the CPU in a known good machine or try a different
CPU.

If the CPU is proven good you can turn your attention
to the SAM, this governs the CPU activity and memory
addressing. I've yet to see one fail but if it does
you have no hope of getting the computer to work until
it is replaced. More likely the SAM is not getting 
the input signals it needs to operate.

Check the clock input and the Q/E output of the SAM.
If the clock is present and correct, check the SAM 
is generating RAM addressing signals on the Z lines 
and RAS/CAS lines.

The SAM also decides what device is being addressed
it does this though a multiplexer at IC33. Check the
operation of this chip carefully. Also make sure you
have a jumper clip on JP13/14 as a missing signal here
will disable the multiplexer!