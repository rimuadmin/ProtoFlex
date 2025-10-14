# Audio and Profile Commands

## Microphone Commands

Microphone commands control microphone input settings and parameters.

### ACC

Set ACC (Accessory) input.

```
C[D]<seq_number>|mic acc <0|1>
```

**Parameters:**
- `<0|1>` = disable/enable ACC input

**Example:**
```
C300|mic acc 0
```

**Response:**
```
R300|0||                                         (success - ACC disabled)
```

### BIAS

Enable/disable microphone bias voltage.

```
C[D]<seq_number>|mic bias <0|1>
```

**Parameters:**
- `<0|1>` = disable/enable mic bias

**Example:**
```
C301|mic bias 1
```

**Response:**
```
R301|0||                                         (success - mic bias enabled)
```

### BOOST

Enable/disable microphone boost.

```
C[D]<seq_number>|mic boost <0|1>
```

**Parameters:**
- `<0|1>` = disable/enable mic boost

**Example:**
```
C302|mic boost 0
```

**Response:**
```
R302|0||                                         (success - mic boost disabled)
```

### INPUT

Set microphone input source.

```
C[D]<seq_number>|mic input <input_name>
```

**Parameters:**
- `<input_name>` = microphone input designation

**Example:**
```
C303|mic input MIC
```

### LIST

Get list of available microphone inputs.

```
C[D]<seq_number>|mic list
```

**Example:**
```
C304|mic list
```

**Response:**
```
R304|0|MIC ACC BAL LINE|                         (success - returns available mic inputs)
```

## Mixer Commands

Mixer commands control audio routing and levels.

### FRONT_SPEAKER

Control front speaker settings.

#### MUTE

Mute/unmute front speaker.

```
C[D]<seq_number>|mixer front_speaker mute <0|1>
```

**Parameters:**
- `<0|1>` = unmute/mute

**Example:**
```
C310|mixer front_speaker mute 0
```

### HEADPHONE

Control headphone settings.

#### GAIN

Set headphone gain level.

```
C[D]<seq_number>|mixer headphone gain <0-100>
```

**Parameters:**
- `<0-100>` = gain level percentage

**Example:**
```
C311|mixer headphone gain 75
```

#### MUTE

Mute/unmute headphones.

```
C[D]<seq_number>|mixer headphone mute <0|1>
```

**Parameters:**
- `<0|1>` = unmute/mute

**Example:**
```
C312|mixer headphone mute 0
```

### LINEOUT

Control line output settings.

#### GAIN

Set line output gain level.

```
C[D]<seq_number>|mixer lineout gain <0-100>
```

**Parameters:**
- `<0-100>` = gain level percentage

**Example:**
```
C313|mixer lineout gain 50
```

#### MUTE

Mute/unmute line output.

```
C[D]<seq_number>|mixer lineout mute <0|1>
```

**Parameters:**
- `<0|1>` = unmute/mute

**Example:**
```
C314|mixer lineout mute 0
```

## Profile Commands

Profile commands manage radio configuration profiles for different operating scenarios.

### AUTOSAVE

Control automatic profile saving.

```
C[D]<seq_number>|profile autosave <on|off>
```

**Parameters:**
- `on|off` = enable/disable auto-save

**Example:**
```
C320|profile autosave on
```

### DISPLAY

Manage display profiles.

#### LOAD

Load a display profile.

```
C[D]<seq_number>|profile display load "<name>"
```

**Parameters:**
- `<name>` = profile name

**Example:**
```
C321|profile display load "Contest Setup"
```

#### INFO

Get display profile information.

```
C[D]<seq_number>|profile display info "<name>"
```

**Parameters:**
- `<name>` = profile name

**Example:**
```
C322|profile display info "Contest Setup"
```

### GLOBAL

Manage global profiles.

#### SAVE

Save a global profile.

```
C[D]<seq_number>|profile global save "<name>"
```

**Parameters:**
- `<name>` = profile name

**Example:**
```
C323|profile global save "DX Configuration"
```

#### DELETE

Delete a global profile.

```
C[D]<seq_number>|profile global delete "<name>"
```

**Parameters:**
- `<name>` = profile name

**Example:**
```
C324|profile global delete "Old Configuration"
```

#### LOAD

Load a global profile.

```
C[D]<seq_number>|profile global load "<name>"
```

**Parameters:**
- `<name>` = profile name

**Example:**
```
C325|profile global load "DX Configuration"
```

#### INFO

Get global profile information.

```
C[D]<seq_number>|profile global info "<name>"
```

**Parameters:**
- `<name>` = profile name

**Example:**
```
C326|profile global info "DX Configuration"
```

### MIC

Manage microphone profiles.

#### SAVE

Save a microphone profile.

```
C[D]<seq_number>|profile mic save "<name>"
```

**Parameters:**
- `<name>` = profile name

**Example:**
```
C327|profile mic save "Contest Mic"
```

#### CREATE

Create a new microphone profile.

```
C[D]<seq_number>|profile mic create "<name>"
```

**Parameters:**
- `<name>` = profile name

**Example:**
```
C328|profile mic create "New Mic Setup"
```

#### RESET

Reset microphone profile to defaults.

```
C[D]<seq_number>|profile mic reset "<name>"
```

**Parameters:**
- `<name>` = profile name

**Example:**
```
C329|profile mic reset "Contest Mic"
```

#### DELETE

Delete a microphone profile.

```
C[D]<seq_number>|profile mic delete "<name>"
```

**Parameters:**
- `<name>` = profile name

**Example:**
```
C330|profile mic delete "Old Mic Setup"
```

#### LOAD

Load a microphone profile.

```
C[D]<seq_number>|profile mic load "<name>"
```

**Parameters:**
- `<name>` = profile name

**Example:**
```
C331|profile mic load "Contest Mic"
```

### TRANSMIT

Manage transmit profiles.

#### SAVE

Save a transmit profile.

```
C[D]<seq_number>|profile transmit save "<name>"
```

**Parameters:**
- `<name>` = profile name

**Example:**
```
C332|profile transmit save "High Power"
```

#### CREATE

Create a new transmit profile.

```
C[D]<seq_number>|profile transmit create "<name>"
```

**Parameters:**
- `<name>` = profile name

**Example:**
```
C333|profile transmit create "QRP Setup"
```

#### RESET

Reset transmit profile to defaults.

```
C[D]<seq_number>|profile transmit reset "<name>"
```

**Parameters:**
- `<name>` = profile name

**Example:**
```
C334|profile transmit reset "High Power"
```

#### DELETE

Delete a transmit profile.

```
C[D]<seq_number>|profile transmit delete "<name>"
```

**Parameters:**
- `<name>` = profile name

**Example:**
```
C335|profile transmit delete "Old Setup"
```

### TX

Additional transmit profile operations.

#### LOAD

Load a TX profile.

```
C[D]<seq_number>|profile tx load "<name>"
```

**Parameters:**
- `<name>` = profile name

**Example:**
```
C336|profile tx load "Contest TX"
```

#### INFO

Get TX profile information.

```
C[D]<seq_number>|profile tx info "<name>"
```

**Parameters:**
- `<name>` = profile name

**Example:**
```
C337|profile tx info "Contest TX"
```