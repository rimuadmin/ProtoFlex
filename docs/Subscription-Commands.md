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