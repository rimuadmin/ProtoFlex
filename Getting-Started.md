### Running ProtoFlex on Windows

1. Create a folder on your PC.
2. Download the executable (protoflex.exe) from the repository 'dist' folder and store it in the local folder.
3. Copy the radio_config.json file from the repository to the same local folder.
4. Open a command line window.
5. Change directory to the local folder.
6. Run the command: `protoflex.exe --config-file radio_config.json`

The ProtoFlex server will start running. At this point you can connect SmartSDR to ProtoFlex.

Using a browser, go to http://localhost:5000 to display the browser interface.

Start SmartSDR and the Protoflex Radio Emulator will be listed.

### Access ProtoFlex Webapp Another Device
- If you have started ProtoFlex on a Windows computer, you can access the web app from another device on the network.
- Determine the IP address of the computer running ProtoFlex, say 192.168.1.100
- On the remote device, use a browser to go to http://192.168.1.100:5000

### Command Line Options

```bash
# With console logging only
protoflex.exe --config-file radio_config.json 

# With file logging and console logging
protoflex.exe --config-file radio_config.json --log-file protoflex.log

# With file logging and console logging with a custom log level
protoflex.exe --config-file radio_config.json --log-file protoflex.log --log-level INFO

# With file logging and custom log level and no console logging
protoflex.exe --config-file radio_config.json --log-file protoflex.log --log-level INFO --no-console

# Short form
protoflex.exe -c radio_config.json -l protoflex.log
```
