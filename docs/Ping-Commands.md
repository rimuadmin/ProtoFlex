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