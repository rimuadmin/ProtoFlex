# Miscellaneous Commands

## Antenna Commands

### LIST

Get list of available antenna ports.

```
C[D]<seq_number>|ant list
```

**Example:**
```
C150|ant list
```

**Response:**
```
R150|0|ANT1 ANT2 RX_A RX_B XVTR|               (success - returns antenna list)
```

## ATU Commands

Antenna Tuning Unit commands for automatic antenna matching.

### BYPASS

Set ATU to bypass mode.

```
C[D]<seq_number>|atu bypass
```

**Example:**
```
C151|atu bypass
```

**Response:**
```
R151|0||                                         (success - ATU bypassed)
```

### CLEAR

Clear ATU memories.

```
C[D]<seq_number>|atu clear
```

**Example:**
```
C152|atu clear
```

**Response:**
```
R152|0||                                         (success - ATU memories cleared)
```

### SET

Configure ATU parameters.

```
C[D]<seq_number>|atu set memories_enabled=<0|1>
```

**Parameters:**
- `<0|1>` = disable/enable ATU memories

**Example:**
```
C153|atu set memories_enabled=1
```

### START

Start ATU tuning process.

```
C[D]<seq_number>|atu start
```

**Example:**
```
C154|atu start
```

## Equalizer Commands

### GET INFO

Get equalizer information.

```
C[D]<seq_number>|eq <eq_select> sc info
```

**Parameters:**
- `<eq_select>` = equalizer selection

**Example:**
```
C160|eq 0 sc info
```

### APF GAIN

Set Auto Peak Filter gain.

```
C[D]<seq_number>|eq apf gain <0-100>
```

**Parameters:**
- `<0-100>` = gain level

**Example:**
```
C161|eq apf gain 50
```

### APF MODE

Set Auto Peak Filter mode.

```
C[D]<seq_number>|eq apf mode <0|1>
```

**Parameters:**
- `<0|1>` = mode setting

**Example:**
```
C162|eq apf mode 1
```

### APF QFACTOR

Set Auto Peak Filter Q factor.

```
C[D]<seq_number>|eq apf qfactor <0-33>
```

**Parameters:**
- `<0-33>` = Q factor value

**Example:**
```
C163|eq apf qfactor 10
```

## Filter Commands

### SET BANDWIDTH

Set slice filter bandwidth.

```
C[D]<seq_number>|filt <slice_index> <low> <high>
```

**Parameters:**
- `<slice_index>` = slice number
- `<low>` = low cut frequency in Hz
- `<high>` = high cut frequency in Hz

**Example:**
```
C170|filt 0 100 3000
```

## Information Commands

### INFO

Get radio information.

```
C[D]<seq_number>|info
```

**Example:**
```
C180|info
```

**Response:**
```
R180|0|model=FLEX-6700 version=3.4.15 serial=1234-5678-9012-3456|  (success - returns radio info)
```

### VERSION

Get radio version information.

```
C[D]<seq_number>|version
```

**Example:**
```
C181|version
```

**Response:**
```
R181|0|3.4.15.987|                              (success - returns firmware version)
```

## Interlock Commands

Configure transmit interlock parameters.

```
C[D]<seq_number>|interlock <parameter>=<value>
```

**Available Parameters:**

| Parameter | Value Range | Description |
|-----------|-------------|-------------|
| `acc_tx_delay` | `ms` | Set ACC TX delay in milliseconds |
| `acc_tx_enabled` | `0\|1` | Enable/disable ACC TX |
| `acc_txreq_enable` | `0\|1` | Enable/disable ACC TX request |
| `acc_txreq_polarity` | `0\|1` | Set ACC TX request polarity |
| `rca_txreq_enable` | `0\|1` | Enable/disable RCA TX request |
| `rca_txreq_polarity` | `0\|1` | Set RCA TX request polarity |
| `timeout` | `ms` | Set interlock timeout in milliseconds |
| `tx_delay` | `ms` | Set general TX delay in milliseconds |
| `tx1_delay` | `ms` | Set TX1 delay in milliseconds |
| `tx1_enabled` | `0\|1` | Enable/disable TX1 |
| `tx2_delay` | `ms` | Set TX2 delay in milliseconds |
| `tx2_enabled` | `0\|1` | Enable/disable TX2 |
| `tx3_delay` | `ms` | Set TX3 delay in milliseconds |
| `tx3_enabled` | `0\|1` | Enable/disable TX3 |

**Examples:**
```
C190|interlock acc_tx_delay=100
C191|interlock acc_tx_enabled=1
C192|interlock tx_delay=50
C193|interlock timeout=5000
```

## Keepalive Commands

### ENABLE

Enable keepalive mechanism.

```
C[D]<seq_number>|keepalive enable
```

**Example:**
```
C200|keepalive enable
```

## License Commands

### REFRESH

Refresh radio license.

```
C[D]<seq_number>|license refresh
```

**Example:**
```
C210|license refresh
```

## Memory Commands

### CREATE

Create memory channel.

```
C[D]<seq_number>|memory create
```

**Example:**
```
C220|memory create
```

## Meter Commands

### LIST

Get list of available meters.

```
C[D]<seq_number>|meter list
```

**Example:**
```
C230|meter list
```

**Response:**
```
R230|0|1.src=COD~ANT#1.unit=SWR.low=1.0.hi=10.0 2.src=COD~ANT#1.unit=FORW.low=0.0.hi=100.0|  (success - returns meter list)
```

## Ping Commands

### PING

Send ping to radio.

#### WITH TIMESTAMP

Send ping with timestamp.

```
C[D]<seq_number>|ping ms_timestamp=<timestamp>
```

**Parameters:**
- `<timestamp>` = millisecond timestamp

**Example:**
```
C240|ping ms_timestamp=1234567890
```

**Response:**
```
R240|0|pong ms_timestamp=1234567890|             (success - returns ping with timestamp)
```

#### WITHOUT TIMESTAMP

Send simple ping.

```
C[D]<seq_number>|ping
```

**Example:**
```
C241|ping
```

**Response:**
```
R241|0|pong|                                    (success - simple pong response)
```

## Subscription Commands

### SUB

Subscribe to status updates.

```
C[D]<seq_number>|sub <category> all
```

**Parameters:**
- `<category>` = client, tx, atu, amplifier, meter, pan, slice, gps, audio_stream, cwx, xvtr, memories, daxiq, dax, usb_cable, tnf, spot, rapidm, ale, log_manager, radio, codec, apd

**Example:**
```
C250|sub slice all
```

### UNSUB

Unsubscribe from status updates.

```
C[D]<seq_number>|unsub <category> all
```

**Parameters:**
- `<category>` = category to unsubscribe from

**Example:**
```
C251|unsub tnf all
```

## TNF Commands

Tracking Notch Filter commands.

### CREATE

Create TNF.

```
C[D]<seq_number>|tnf create freq=<MHz>
```

**Parameters:**
- `<MHz>` = frequency in MHz

**Example:**
```
C260|tnf create freq=14.230
```

## Waveform Commands

### UNINSTALL

Uninstall waveform.

```
C[D]<seq_number>|waveform uninstall <waveform_name>
```

**Parameters:**
- `<waveform_name>` = name of waveform to uninstall

**Example:**
```
C270|waveform uninstall custom_waveform
```

## MOX Commands

### XMIT

Enable/disable MOX (Manual On/Off).

```
C[D]<seq_number>|xmit <0|1>
```

**Parameters:**
- `<0|1>` = disable/enable MOX

**Example:**
```
C280|xmit 1
```

## Transverter Commands

### CREATE

Create transverter.

```
C[D]<seq_number>|xvtr create
```

**Example:**
```
C290|xvtr create
```