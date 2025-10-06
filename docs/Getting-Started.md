## Requirements
- At this time ProtoFlex only runs on Windows.

## Running ProtoFlex on Windows
1. Create a folder on your PC.
2. Download the following files from the repository 'dist' folder and store them in the local folder:
   - protoflex.bat
   - protoflex.exe
   - radio_config.json
3. Double click on the file `protoflex.bat` to run ProtoFlex.
   - The ProtoFlex server will start running.
   - It will log to the console and also to a file.
4. Start SmartSDR and the Protoflex will be listed. If you have a FlexRadio on the same subnet you will see two choices:

![SmartSDR Selection](https://github.com/rimuadmin/ProtoFlex/blob/main/images/smart_sdr_radio_selection.png)
   
5. Using a browser, go to http://localhost:5000 to display the browser interface.

![Browser Main Page](https://github.com/rimuadmin/ProtoFlex/blob/main/images/protoflex_main_2.png)

## Access the ProtoFlex web app from another device
- If you have started ProtoFlex on a computer, you can access the web app from another device on the network.
- Determine the IP address of the computer running ProtoFlex, say 192.168.1.100
- On the remote device, use a browser to go to http://192.168.1.100:5000

## Command Line Options

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
