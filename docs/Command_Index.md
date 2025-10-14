# FlexRadio Command Reference

This documentation provides comprehensive reference for all FlexRadio API commands discovered from the FlexLib C# API.

## Command Categories

### Core Radio Control
- [**Slice Commands**](slice_commands.md) - Receiver slice control, tuning, and configuration
- [**Radio Commands**](radio_commands.md) - Global radio settings and configuration
- [**Transmit Commands**](transmit_commands.md) - RF power, audio processing, and transmission parameters

### Client and Connectivity
- [**Client Commands**](client_commands.md) - Client connection and session management
- [**WAN Commands**](spot_wan_commands.md) - Wide Area Network remote access

### Audio and CW
- [**CW Commands**](cw_commands.md) - Morse code keying and CWX text buffer operations
- [**Audio and Profile Commands**](audio_profile_commands.md) - Microphone, mixer, and profile management

### Display and Data
- [**Display Commands**](display_commands.md) - Panadapter and waterfall display control
- [**File and Stream Commands**](file_stream_commands.md) - File operations and audio/data streams
- [**Spot Commands**](spot_wan_commands.md) - DX cluster spot management

### System and Utilities
- [**Miscellaneous Commands**](miscellaneous_commands.md) - ATU, meters, TNF, antennas, and other utilities

## Command Format

All commands follow the FlexRadio API format:

```
C[D]<seq_number>|<command> [sub-command] [parameters]
```

Where:
- `C` = Command prefix
- `D` = Optional debug flag
- `<seq_number>` = Sequence number for command tracking
- `<command>` = Primary command word
- `[sub-command]` = Optional sub-command
- `[parameters]` = Command-specific parameters

## Response Format

Responses follow the format:
```
R<seq_number>|<result_code>|<data>|[debug_info]
```

Where:
- `R` = Response prefix
- `<seq_number>` = Matching sequence number from command
- `<result_code>` = Result code (`0` = success, non-zero = error)
- `<data>` = Command-specific response data
- `[debug_info]` = Optional debug information

## Response Examples

**Successful Commands:**
```
R21|0|2|slice created on 14.230000 MHz        (slice create)
R25|0|14.230000|                              (slice tune)
R33|0|192.168.1.100|                          (client ip)
R26|0||                                       (simple set commands)
```

**Error Responses:**
```
R21|50000001||Unable to create slice
R25|50000004||Invalid frequency parameter
R26|50000016||Malformed command
```

## Common Response Codes

| Code | Meaning |
|------|---------|
| 0 | Success |
| 50000001 | Unable to get foundation receiver assignment |
| 50000003 | License check failed |
| 50000004 | Parameter error |
| 50000005 | Incorrect number or type of parameters |
| 50000016 | Malformed command |
| 5000002C | Incorrect number of parameters |
| 50000032 | Bad mode |

## Usage Notes

1. **Sequence Numbers**: Each command should use a unique sequence number to track responses
2. **Parameter Format**: Most numeric parameters accept ranges as specified in each command
3. **String Parameters**: String parameters should be quoted when they contain spaces
4. **Stream IDs**: Display stream IDs are typically in hexadecimal format (e.g., 0x40000000)
5. **Frequency Format**: Frequencies are specified in MHz with up to 6 decimal places

## Command Discovery Source

These commands were extracted from the FlexRadio FlexLib C# API by analyzing:
- `SendCommand()` method calls for immediate commands
- `SendReplyCommand()` method calls for commands requiring responses
- Complete analysis of Radio.cs, Slice.cs, and related source files

The documentation represents the complete command set available in the FlexRadio protocol as implemented in the official FlexLib API.
