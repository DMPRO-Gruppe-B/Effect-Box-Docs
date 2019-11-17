# Effect-Box

## Introduction
Effect-Box is an audio effect device that takes an audio input, modifies it by applying effects and plays the modified audio on a DAC.
The audio input and output is provided by two 3.5 mm jacks.
The audio effects are implemented in Chisel and run on a Xilinx Artix 7 FPGA.
To select the desired audio effects and configure these the PCB is equipped with an LCD screen and buttons.
These are connected to an EFM32GG MCU which in turn sends control signals to the FPGA to enable and configure the effects as the user specifies in the interface.

## Effects
TODO write about chaining

TODO briefly describe the audio properties (not implementation) of each effect

## LCD menu
The LCD menu displays the available audio effects and their configurable settings.
The settings will be different for each effect, but every effect has a bypass setting for disabling the effect.
Several effects can be enabled simultaneously.

The button group to the left is for navigation, and the buttons to the right increment and decrement the selected setting value.
When a setting value is changed the MCU with send a corresponding control signal to the FPGA and the display will be updated.
