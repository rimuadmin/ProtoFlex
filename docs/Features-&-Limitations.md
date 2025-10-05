## Features

- **FlexRadio Compatible TCP Interface**: Command protocol support for client applications
- **Realistic Spectrum Generation**: Dynamic HF band simulation with SSB, CW, and digital signals
- **UDP Streaming**: Panadapter FFT data, waterfall tiles, and meter streaming
- **VITA-49 Discovery Protocol**: Automatic radio discovery for SmartSDR clients
- **Multi-Client Support**: Handle multiple simultaneous client connections
- **Session Management**: Track client sessions with GUI/non-GUI client detection
- **Flexible Configuration**: Configure the ProtoFlex using a JSON file
- **Browser Interface**: View internal state of ProtoFlex
- **Comprehensive Logging**: Configurable logging with file output support

## Limitations
ProtoFlex's signal generation doesn't mimic FlexRadio's Spectral Capture Units (SCUs) exactly. In a FlexRadio each SCU processes signals for a 30kHz to 54MHz frequency range - a lot of data. Instead ProtoFlex assigns a Spectrum Generator to each panadapter which generates random signals for 1.5x the frequency range selected for the panadapter. This significantly reduces the amount of data to process. The downside is that two panadapters on the same band and frequency range show entirely different signals. For an emulator this isn't an important difference.

Not every TCP command has been implemented. There are some commands that are unlikely to ever be implemented (i.e. the Audio commands). 

Only the most important meters are currently implemented. 
- There are 11 basic meters created initially for items like temperature, voltage, current draw and fan speed. These values can be set using the web app interface.
- When a new slice is created, a FlexRadio adds approximately 10 meters. ProtoFlex adds only three today: LEVEL, AGC+, 24kHz. Most significant of these is the signal level meter. ProtoFlex derives the signal level from the peak signal strength of all signals in the slice's bandpass filter. This is not how it's normally calculated, but sufficient for an emulator.
- When a slice is removed, ProtoFlex removes the corresponding meters - identical behavior to the FlexRadio.

The behavior ProtoFlex is a best attempt at mimicking the behavior of a FlexRadio, mostly based on observed behavior of a FLEX-6400 for SmartSDR version 3.10.10. There may be differences when compared to other Flex models or SmartSDR versions. There is definitely room for improvement here.

