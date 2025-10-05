# Introduction

**ProtoFlex** is a protocol-level emulator that replicates the behavior of a FlexRadio including Maestro-style interactions over TCP and UDP. It simulates how FlexRadio devices respond to network commands, enabling developers, integrators, and testers to validate control workflows, debug protocol exchanges, and build custom SDR interfaces without requiring physical hardware.

Originally developed to support [TeensyMaestro hardware](https://github.com/rimuadmin/TeensyMaestro-Hardware) testing in the absence of a FlexRadio, ProtoFlex provides a minimal yet functional simulation of FlexRadio behavior. It mimics expected responses and state transitions, making it ideal for environments with limited hardware access or where automated testing is essential.

Beyond its initial scope, ProtoFlex supports scenarios such as simulating multiple FlexRadios on a network. ProtoFlex also emulates multiple panadapters and receive slices. Each panadapter includes an independent Spectrum Generator that approximates RF signals and noise, offering a realistic backdrop for client-side signal visualization and interaction.

# SmartSDR connected to ProtoFlex
ProtoFlex simulates panadapter, waterfall and meter streams:

![SmartSDR Connected](https://github.com/rimuadmin/ProtoFlex/blob/main/images/smart_sdr.png)

# Server Logging
- ProtoFlex logs all the incoming TCP client commands, responses and status responses. 
- The UDP Discovery payload is logged when a change to one of the attributes occurs.

![ProtoFlex Log](https://github.com/rimuadmin/ProtoFlex/blob/main/images/protoflex_log.png "ProtoFlex Log")

# Browser Interface
ProtoFlex has a browser interface to show the state of the emulated radio. Some attributes, like meter values, can be changed using this interface.

![ProtoFlex Main Page](https://github.com/rimuadmin/ProtoFlex/blob/main/images/protoflex_main.png "ProtoFlex Main Page")


