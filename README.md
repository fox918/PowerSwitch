# PowerSwitch Project

## Idea
Having a simple and extensible way to switch 12V power with a microcontroller

## Concept
The idea is to use a Infineon SmartFET as powerswitch.
This reduces complexity because a lot of things are already taken care of and we can
further use the diagnostic outputs to measure the current.

Using an i2c GPIO expander and an i2c ADC allows for measuring supply voltage, current delivered to the output and temperature of the heatsink.

With a dip switch, we can change the address of both i2c devices simultaneously, therefore allowing 4 devices on the same i2c bus.

Look at [PowerSwitch Idea](./PowerSwitch_Idea.pdf) for a Block Schema.


## License
MIT, 2017 Oliver Wisler
