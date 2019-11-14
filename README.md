# Effect-Box-Docs

## Introduction
The Effect Box IV: Gruppe B Edition is a sound effect device that takes a sound input signal, modifies it by applying effects and passes it to sound output.
The sound input and sound ouput signals is provided by two 3.5 mm jacks.
The effects are created using an Xilinx Artix 7 FPGA and programmed using the modern hardware design language Chisel. 
To control the application of the effects and the settings of each effect, an EFM32GG MCU is used.
Each effect with their respective settings is displayed on the SPI display, and can be configured using the buttons below the display.
