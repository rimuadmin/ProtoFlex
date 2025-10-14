# Spot and WAN Commands

## Spot Commands

Spot commands manage DX cluster spots and spotting functionality.

### ADD

Add a new spot to the display.

```
C[D]<seq_number>|spot add callsign=<call> rx_freq=<MHz> [tx_freq=<MHz>] [mode=<mode>] [color=<color>] [etc.]
```

**Parameters:**
- `<call>` = callsign of spotted station
- `<MHz>` = receive frequency in MHz
- `tx_freq=<MHz>` = optional transmit frequency
- `mode=<mode>` = optional mode (USB, LSB, CW, etc.)
- `color=<color>` = optional spot color
- Additional optional parameters may be available

**Example:**
```
C340|spot add callsign=W1AW rx_freq=14.230 mode=CW color=red
```

**Response:**
```
R340|0|spot_id=12345|                           (success - returns spot ID)
```

### CLEAR

Clear all spots from the display.

```
C[D]<seq_number>|spot clear
```

**Example:**
```
C341|spot clear
```

**Response:**
```
R341|0||                                         (success - all spots cleared)
```

## WAN Commands

WAN (Wide Area Network) commands manage remote radio access and connectivity.

### REGISTER

Register radio with WAN service using owner token.

```
C[D]<seq_number>|wan register owner_token=<token>
```

**Parameters:**
- `<token>` = owner authentication token

**Example:**
```
C350|wan register owner_token=abc123def456
```

**Response:**
```
R350|0||                                         (success - registered with WAN)
R350|50000008||Invalid token                     (error - bad owner token)
```

### SET

Configure WAN parameters.

#### PUBLIC PORTS

Set public TLS and UDP ports for WAN access.

```
C[D]<seq_number>|wan set public_tls_port=<port> public_udp_port=<port>
```

**Parameters:**
- `public_tls_port=<port>` = TLS port number
- `public_udp_port=<port>` = UDP port number

**Example:**
```
C351|wan set public_tls_port=4993 public_udp_port=4991
```

### UNREGISTER

Unregister radio from WAN service.

```
C[D]<seq_number>|wan unregister owner_token=<token>
```

**Parameters:**
- `<token>` = owner authentication token

**Example:**
```
C352|wan unregister owner_token=abc123def456
```

### VALIDATE

Validate WAN connection.

```
C[D]<seq_number>|wan validate handle=<handle>
```

**Parameters:**
- `<handle>` = connection handle

**Example:**
```
C353|wan validate handle=0x12345678
```