# Micro USB to Cisco RJ45 and TTL RS232 adapter

Many devices connect through a UART for console access or programming.
Many embedded devices' UARTs are broken out through a header with
5V (Arduino) or 3.3V (Beaglebone, Raspberry Pi) signaling.  Other
devices have RS232 ports, usually either DB9 (PCs, enterprise-class
network hardware) or RJ45 (Cisco).  In order to be ready to connect a
laptop to any encountered device, one's commando kit must contain a
pile of cables, such as USB to DB9, DB9 to RJ45, USB to TTL (FTDI),
and null modem/rollover adapters.

The adapter circuit in this repo carries an inexpensive CPL2102 USB
breakout board, cheap and plentiful on eBay, and exposes configurable
ports for talking to the above devices with minimal additional
cabling.

For connecting to RS232 consoles on PCs, network hardware, console
servers, etc., an onboard MAX3232 chip converts the TTL signals to
RS232 via a Cisco-pinout RJ45 connector.  Cisco console ports are
attached with a simple ethernet cable.  DB9 ports may be connected
with the same ethernet cable and a small, inexpensive DB9 to Cisco
RJ45 adapter.  Switch 2 selects straight through or null modem to
eliminate the need for a separate rollover adapter.

For connecting to embedded consoles, switch 3 directs the signals to a
six-pin header.  Switch 2 selects between 3.3 and 5 volt signal
levels.  The header pinout matches the Arduino Mini Pro, and provides
DTR (for programming) and power.  A straight-through six-pin header
cable connects both the Arduino Mini Pro and Beaglebone Black; other
devices may be connected after determining appropriate pinouts.
