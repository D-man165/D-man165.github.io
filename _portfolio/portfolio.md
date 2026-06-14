# Frequently asked questions

## How do sensors work?
A silicon sensor is essentially a p-n junction under external potential difference. The strip sensor consists of many n-type strips implanted on a p-type substrate creating many p-n junctions. When an ionizing particle hits the sensor, it ionizes the electron-hole pairs which create current due to the potential difference. This current is measured by the read-out ABCStars (ATLAS Binary Chips).

## What is an IV scan
An IV scan measures the leakage current (I) of the sensor under varying voltage (V). The voltage is varied from 0V to -550V (for glued sensors), and -700V (unglued). Descrepancies can help identify breakdowns in the sensors.

## What is a strobe delay test?
The purpose of this test is to find the delay between when the ABCStar receives the clock signal from HCCStar and when the ABCStar monitors the channels for signal. For a given channel threshold and input charge, occupancy of each channel is measured for different calibration pulse delays. A sample plot is attached below:

<p align="center">
  <img src="/Images/NORMAL_STROBE-DELAY_EXAMPLE.jpeg" width="100%">
</p>

## What is a three point gain?
Gain is the threshold voltage (where 50% of hits are detected) of an ABCStar for an input charge. Threshold scans are measured for 3 charges (0.5, 1 and 1.5 fC). The slope of the threshold voltage with respect to the input charge is the 3PT gain. 

The input noise (at the amplifier) is calculated as the output noise (threshold voltage) divided by the gain and measured in Coulombs as the ENC (Effective Noise Charge). ENC can help us identify defective channels. 

For example, this is a normal ENC plot:

<p align="center">
  <img src="/Images/NORMAL_ENC_EXAMPLE.jpeg" width="100%">
</p>

This is a high noise plot:

<p align="center">
  <img src="/Images/HIGH_ENC_EXAMPLE.jpeg" width="100%">
</p>

## What is a pedestal trim?
Each channel has slightly different offset (noise floor). For this reason, every ABCStar has a 5 bit trim DAC (Digital-to-Analog Converter). So every channel has 32 adjustable steps for offset. This is essential for a uniform response within a chip.

What does "change the shunt" mean?

Why do we need to restart ITSDAQ after the initial initialization of the AMAC? Can that be placed into a function without having to restart?

What are all of the PPB phases and subphases? How many staves per phase / subphase?

If the BurstData and ScanData windows close while ITSDAQ is running, do you need to restart ITSDAQ?

From are above list are we missing anything that is included in the FullTest

In examples RC curves, what is the quantity in the top plot? And how does it affect the bottom plot?

Does the ITk production database contain both pixel and strips information?

Which two components does the HV tab connect?
