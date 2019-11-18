# Effect-Box

## Introduction
Effect-Box is an audio effect device that takes an audio input, modifies it by applying effects and plays the modified audio on a DAC.
The audio input and output is provided by two 3.5 mm jacks.
To select the desired audio effects and configure these the PCB is equipped with an LCD screen and buttons.

## Quickstart guide
TODO image, description of physical connections (power, audio, ..)

## Effects
Several effects can be enabled simultaneously.
They are chained after each other, meaning the original audio signal is the input to the first effect, and each effects output is the input to the next effect in the chain.
The order of effects is fixed and not configurable.

### Bit crusher
TODO

### Tremolo
TODO

### Delay
TODO

TODO briefly describe the audio properties (not implementation) of each effect

## How it works
The audio effects are implemented in Chisel and run on a Xilinx Artix 7 FPGA.
The buttons and LCD are connected to an EFM32GG MCU which in turn sends control signals to the FPGA to enable and configure the effects as the user specifies in the interface.
Communication with the LCD happens over SPI using Silicon Labs libraries.
MCU-FPGA communication is also over SPI, using a custom protocol.

### LCD menu
The LCD menu displays the available audio effects and their configurable settings.
The settings will be different for each effect, but every effect has an enable setting.

The button group to the left is for navigation, and the buttons to the right increment and decrement the selected setting value.
When a setting value is changed the MCU sends a corresponding SPI command to the FPGA and the display is updated.

## Audio connection
The Effect Box is a mono balanced input, stereo unbalanced output device, although the outputs are currently mirrored and not true stereo. However, this allows you to connect the output directly to a typical 3.5 mm unbalanced stereo input on a computer sound card or active speaker. When outputting to a balanced mono input (typically a 6.35 mm jack or XLR), a split cable should be used to separate one channel (if not, the balanced input will treat the identical channels as a differential pair).

The input is capable of receiving either balanced or unbalanced mono signals. These should be somewhere between consumer and professional line level (maximum 1 V peak or 0 dBV). The input impedance is around 1 MΩ, so the device is also capable of receiving instrument level signals like guitars, although this is not optimal and they will need to be turned up to the maximum possible level.

To connect a sound source to the Effect Box, you probably need to use a 6.35 to 3.5 mm jack adapter, for example if you want to hook up a synthesizer or a line level output from a mixer or sound card (these typically have 6.35 mm jack outputs). You could also use a split cable to connect only one channel of a phone or laptop if you want to send music through the Effect Box.
