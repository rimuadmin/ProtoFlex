ProtoFlex is a versatile tool for testing and debugging FlexRadio client applications. Below are several scenarios where it excels:

## 1. Test Commands Sent from a Custom Client
When SmartSDR connects to ProtoFlex, all exchanged commands are logged in plain text—making it easy to analyze protocol behavior. While WireShark can capture similar traffic, parsing command and response strings is far more tedious. For custom hardware clients, WireShark becomes impractical due to limited visibility and decoding complexity. Although firmware modifications might enable internal logging, ProtoFlex offers a much simpler and more reliable alternative.

## 2. Test Multiple FlexRadios on the Same Subnet
If you need to test how your client handles multiple FlexRadios on the same subnet, ProtoFlex makes this easy. Instead of sourcing additional hardware, launch multiple ProtoFlex instances with unique names via their JSON config files. Each instance will broadcast VITA-49 UDP Discovery packets, allowing you to validate how your application detects and selects among available radios.

## 3. Test Client Application Handling of Meter Data
If your application monitors meter data — such as temperature, voltage, or fan levels — ProtoFlex lets you simulate dynamic changes in real time. Use the built-in Web UI to adjust meter values and verify that your client responds appropriately, such as triggering alerts for overheating or low voltage conditions.

## 4. Log Client Commands for Bug Reports
If you suspect a bug in FlexRadio's firmware or API behavior, use ProtoFlex to log every command sent by your custom hardware. These logs can then be replayed or tested using simple clients like PuTTY, helping you isolate issues and generate reproducible bug reports.

## 5. Try out SmartSDR before Buying a FlexRadio
If you're considering purchasing a FlexRadio but want to explore SmartSDR first, ProtoFlex offers a low-risk way to evaluate the software. By launching a ProtoFlex instance on your local network, SmartSDR will detect it just like a real FlexRadio. You can connect and interact with the interface—giving you a hands-on feel for the operation of the radio.
