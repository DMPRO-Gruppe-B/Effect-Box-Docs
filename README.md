# Effect-Box-Docs

## Introduction
The Effect Box IV: Gruppe B Edition is a sound effect device that takes a sound input signal, modifies it by applying effects and passes it to sound output.
The sound input and sound ouput signals is provided by two 3.5 mm jacks.
The effects are created using an Xilinx Artix 7 FPGA and programmed using the modern hardware design language Chisel. 
To control the application of the effects and the settings of each effect, an EFM32GG MCU is used.
Each effect with their respective settings is displayed on the SPI display, and can be configured using the buttons below the display.

## LCD menu
The LCD menu displays the available effects applicable to the input sound signal. Every effect has one or more settings that can be configured. The settings will be different for each effect, but every effect has a "bypass" setting. This setting enables/disables the chosen effect. Several effects can be enabled simultaneously.

The button group on the bottom left side of the display is the navigation buttons. The group consist of four buttons. These buttons can be used to navigate through the effects and their respective settings.

The button group on the bottom right side of the display handles incrementing and decrementing setting values. The group consists of two buttons. When a setting is selected with the navigation buttons, using these buttons will change the value displayed next to each setting.
