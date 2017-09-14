# SmartPowerSwitch Project

## Idea
Having a simple and extensible way to switch 12V power with up to 10A with a microcontroller.
The intended use for the device is to remotely switch things at amateur radio repeater sites. 

## Concept
The idea is to use a Infineon SmartFET as powerswitch.
This reduces complexity because a lot of things are already taken care of and we can
further use the diagnostic outputs to measure the current.

Using an i2c GPIO expander and an i2c ADC allows for measuring supply voltage, current delivered to the output and temperature of the heatsink.

With a dip switch, we can change the address of both i2c devices simultaneously, therefore allowing 4 devices on the same i2c bus.

Look at [PowerSwitch Idea](./PowerSwitch_Idea.pdf) for a Block Schema.

## Current State
An initial approach of the [Schema](./Circuit_Schema_v2.pdf) and the PCB is done, after review a prototype shall be built.

### Current PCB
- [PCB Front](./PCB_front_v2.pdf) 
- [PCB_Back](./PCB_back_v2.pdf) 

### Current Issues
- Almost no protection circuits on the internal voltage source
- Current paths on the pcb not optimal (especially ground path)
- Choose a suitable connector for the i2c backplane (suggestion: rj12, JST SH or some 2.54mm connector)


## Further development
- Design a board to mount the two colored button
- Choose a ethernet enabled microcontroller and design a i2c shield for it 
(and a nice GUI)
- adapt the boards to mount into 1U rackunits with XLR 4-Pin connectors

## License
[MIT, 2017 Oliver Wisler](./LICENSE)

