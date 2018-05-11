# Arria-V-ADC-Ethernet-scripts

## Description

   This repository contains scripts for reading data from the [Arria-V-ADC-Ethernet](https://github.com/samdejong86/Arria-V-ADC-Ethernet) project. They will work on both the verilog and VHDL versions of the code.

## Requirements

   1. Matplotlib
   2. Numpy
   3. telnetlib

## Contents

### Amplitude_Phase.py

#### Description

     Generates a real time plot showing the amplitude and phase of a sinusoidal waveform

#### Usage

     usage: Amplitude_Phase.py [-h] [-a ADDRESS] [-p PORT] [-m] [-f FILENAME]
                               [-r FREQ] [-d]

     Find amplitude and phase of sinewave from FPGA

     optional arguments:
       -h, --help            show this help message and exit
       -a ADDRESS, --address ADDRESS
                             IP address of FPGA
       -p PORT, --port PORT  The port to listen to
       -m, --movie           Save a video
       -f FILENAME, --filename FILENAME
                             Video filename
       -r FREQ, --freq FREQ  Sampling frequency in Megahertz (default: 40)
       -d, --delay           Send delay signal before starting, resend after

### fastScope.py

#### Description

     Creates a live readout of the waveforms from the FPGA

#### Usage

     usage: fastScope.py [-h] [-a ADDRESS] [-p PORT] [-m] [-f FILENAME] [-l LENGTH]
                         [-r FREQ] [-t {self,ext}] [-s {pos,neg}] [-d {on,off}]
                         [-k]

     View waveforms coming from ethernet

     optional arguments:
       -h, --help            show this help message and exit
       -a ADDRESS, --address ADDRESS
                             IP address of FPGA
       -p PORT, --port PORT  The port to listen to
       -m, --movie           Save a 200 frame video
       -f FILENAME, --filename FILENAME
                             Video filename
       -l LENGTH, --length LENGTH
                             length if video (in seconds)
       -r FREQ, --freq FREQ  Sampling frequency in Megahertz (default: 40)
       -t {self,ext}, --trigSource {self,ext}
                             Set trigger source (self or ext)
       -s {pos,neg}, --trigSlope {pos,neg}
                             Set trigger slope (pos or neg)
       -d {on,off}, --delay {on,off}
                             Set delay (on or off)
       -k, --keep            Keep current settings

### getData.py

#### Description

     Gets a the most recent waveform from the FPGA

#### Usage

     usage: getData.py [-h] [-a ADDRESS] [-p PORT] [-sv] [-f FILENAME] [-n]
                       [-r FREQ] [-t {self,ext}] [-s {pos,neg}] [-d {on,off}] [-k]

     View a single waveform coming from ethernet

     optional arguments:
       -h, --help            show this help message and exit
       -a ADDRESS, --address ADDRESS
                             IP address of FPGA
       -p PORT, --port PORT  The port to listen to
       -sv, --save           Save data to a file
       -f FILENAME, --filename FILENAME
                             Name of data file
       -n, --noGraph         Suppress graphical output
       -r FREQ, --freq FREQ  Sampling frequency in Megahertz (default: 40)
       -t {self,ext}, --trigSource {self,ext}
                             Set trigger source (self or ext)
       -s {pos,neg}, --trigSlope {pos,neg}
                             Set trigger slope (pos or neg)
       -d {on,off}, --delay {on,off}
                             Set delay (on or off)
       -k, --keep            Keep current settings
