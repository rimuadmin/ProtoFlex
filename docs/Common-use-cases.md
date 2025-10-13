Here are some use cases where ProtoFlex is an ideal diagnostic tool.

## 1. Test Commands Sent from a Custom Client

By connecting SmartSDR to ProtoFlex, the log will list all the commands that SmartSDR uses. While this can be done with WireShark, it takes more effort to parse out the command and response strings. However, if a custom hardware device is connecting to a FlexRadio, it's very difficult to use WireShark. With firmware changes, the hardware device might be able to log the commands and responses, but this much easier with ProtoFlex.

## 2. Test Multiple FlexRadios on the Same Subnet
If your client application needs to test the use case where there is more than one FlexRadio on the same subnet, ProtoFlex is ideal. Instead of buying or borrowing a second FlexRadio, start one (or more) ProtoFlex instances on the same subnet. Change the JSON configuration file to give each ProtoFlex instance a different name. Each ProtoFlex instance will broadcast VITA-49 UDP Discovery packets. You can then test how your application handles selecting one of the FlexRadios.

## 3. Test Client Application Handling of Meter Data
If you have a client application that consumes meter data to provide warnings on high temperatures or low power, use ProtoFlex and change the meter values while it's running using the Web Application. You could check to see if your application warns the user when over a certain temperature or under a specific voltage.

## 4. Log Client Commands for Bug Report
If you suspect a FlexRadio bug and want to record the commands that are being used by your custom hardware, to then test using a simple client (i.e. Putty) then ProtoFlex will log the commands your device is sending.
