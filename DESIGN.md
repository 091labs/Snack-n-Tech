091 Labs Vending Machine Project
================================

Cabinet
-------

**Can Dispenser**

Cans will be positioned to can size duct where they will be dispenced
by rotating arm one by one. Cans should not be dropped directly to
receiving bowl, but slide should be implemented to ensure minimal shake
during the dispense.

**Snack and Tech Dispenser**

Snack and Tech dispensing will be done with rotating screw conveyor.
Screw conveyor will be open with spring like screw instead of tube. 

**Refrigeration**

Refrigeration will not be implemented at least on initial phase.

**Payment**

Payment will be handled either by coin acceptor or by RFID attached
to the credit account. RFID payments should be protected by PIN to
avoid possible misuses.

Payment verification will be made before product is dispensed. No
change will be provided at initial implementation, but members account
can be credited with any extra paid via coin acceptor.

**User Interface**

User input will be done via coin acceptor, RFID reader and keypad.

Output to user will be done with receiving bowl, indication leds and
lcd display (16-20 char, 2-4 rows).

User interface could be integrate with our door lock to enable door
being left unlocked during open events.

Controller
----------

**Controller communication**

Controller units will communicate over ethernet with each other.

The main controller unit (Raspberry Pi) will communicate with member
database over lab/public network on encrypted manner.

**Sofware on Arduino**

Mqtt client to communicate with main controller.

Various functions to handle I/O. TBD

**Software on Raspberry Pi**

mosquitto for mqtt broker.

Various software components to deal with I/O, security, sync, etc. TBD
