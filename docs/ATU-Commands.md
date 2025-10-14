# ATU Commands

Antenna Tuning Unit commands for automatic antenna matching.

## BYPASS

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

## CLEAR

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

## SET

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

## START

Start ATU tuning process.

```
C[D]<seq_number>|atu start
```

**Example:**
```
C154|atu start
```