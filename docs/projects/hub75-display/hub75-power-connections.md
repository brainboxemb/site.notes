# HUB75 Power Connections

This page contains references and notes about distributing power to HUB75 LED matrix panels.

## Standard Power Cable

- [Replacement 5V Power Cable for RGB LED Matrices](https://www.adafruit.com/product/4767)  
  A replacement power cable intended for HUB75-style RGB LED matrix panels.

- [Adafruit forum discussion about the cable](https://forums.adafruit.com/viewtopic.php?t=191378)  
  Discussion about the details of this type of cable.

## Problems

HUB75 panels are often supplied with standard power cables, frequently with a split for connecting multiple panels.

Alternative cables are not easy to find. In particular, it appears difficult to find a simple HUB75 power connector with loose wires, allowing a custom termination to be added.

## Approach

The most practical solution currently seems to be reusing the available standard HUB75 power cables and connecting their spade terminals to a barrier terminal block.

## Barrier Terminal Block

A barrier terminal block can be used as a central distribution point for the power connections.

The example below shows two terminal blocks used side by side. Multiple connections are linked together on one side of each block.

![Barrier terminal block example](./_images/terminal_block_example.jpg)

- [Amazon.nl — HUAZIZ five-position barrier terminal block](https://www.amazon.nl/HUAZIZ-schroefklemmenblokken-posities-barrièreband-voorgeïsoleerd/dp/B09964YNVT/)  
  Example of a double-row barrier terminal block supplied with jumper strips.

- [Busbars versus terminal blocks](https://www.youtube.com/watch?v=95ZCdMZOhQM)  
  General explanation of the difference between busbars and terminal blocks.

## Assumptions

- The spade terminals at the cable ends appear to be suitable for M3 screws.

## Notes

-