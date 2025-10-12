### Overview
The behavior of ProtoFlex is a best attempt at mimicking the behavior of a FlexRadio, mostly based on the (now quite old) published API specifications and using WireShark to observe the network protocol behavior of a FLEX-6400 and SmartSDR version 3.10.10. There may be differences when compared to other Flex models or SmartSDR versions.

### Spectrum Generator
- ProtoFlex's signal generation doesn't mimic FlexRadio's Spectral Capture Units (SCUs) exactly. 
- In a FlexRadio each SCU processes signals for a 30kHz to 54MHz frequency range - a lot of data. If two panadapters are opened for the same band, the same data is displayed.
- Because it's just an emulator, ProtoFlex simplifies this. It assigns a Spectrum Generator to each panadapter which generates random signals for 1.5x the frequency range selected for the panadapter. 
- This significantly reduces the amount of data to process. The downside is that two panadapters on the same band and frequency range show entirely different signals. For an emulator this isn't an important difference.

### Supported Commands
- See the 'Supported Commands' page which shows the current list of commands that ProtoFlex will honor. While the response message for these commands should exactly match a FlexRadio, the status messages are less accurate (see the Status Messages section).
- Not every TCP command has been implemented yet and there are some commands that are unlikely to ever be implemented (i.e. the Audio commands).

### Status Messages
- FlexRadios send status messages to connected clients when a command is issued or some radio event occurs. 
- Many status messages are only sent when a client subscribes to a topic (Radio, Panadapters, Slices, etc...). Determining exactly which status messages get sent under what conditions is a time-consuming exercise, and so ProtoFlex does not do this perfectly. 
- Additionally, FlexRadios sometimes send duplicate status messages when there is seemingly no need to send duplicates. 
- There is definitely room for ProtoFlex to more accurately match FlexRadio's behavior.

### Meters
FlexRadio streams some data like slice signal strengths, temperature and voltage as meter data. Meter data is sent to the client much more frequently than panadapter or waterfall data.

Only the most important meters are currently implemented. 
- The radio initially creates 11 basic meters items like temperature, voltage, current draw and fan speed (at least on a FLEX-6400, it might be different on other models). ProtoFlex also does this, and allows those values to be changed using the web app interface.
- When a new slice is created, a FlexRadio adds approximately 10 new meters. ProtoFlex adds only three today: LEVEL, AGC+, 24kHz. Most significant of these is the signal level meter. ProtoFlex derives the signal level from the peak signal strength of all signals in the slice's bandpass filter. This is not how it's normally calculated, but sufficient for an emulator.
- When a slice is removed, ProtoFlex removes the corresponding meters - identical behavior to the FlexRadio.