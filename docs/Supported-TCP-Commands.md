## Supported Commands

### Client and Connection Management
- `C<n>|client gui`
- `C<n>|client program`
- `C<n>|client disconnect`
- `C<n>|client ip`
- `C<n>|client udpport <port>`
- `C<n>|client station`
- `C<n>|client bind client_id=<client_id>`
- `C<n>|client nickname <nickname>`
- `C<n>|client set <property>=<value>`

### CW (Morse Code) Control
- `C<n>|cw key <state>`
- `C<n>|cw <subcommand> <parameters>`

### Display Control
- `C<n>|display panafall create [<parameters>]`
- `C<n>|display panafall remove <stream_id>`
- `C<n>|display pan remove <stream_id>`
- `C<n>|display pan set <stream_id> <property>=<value>`
- `C<n>|display pan rfgain_info`
- `C<n>|display panf rfgain_info`
- `C<n>|display waterfall <stream_id> create [<parameters>]`
- `C<n>|display waterfall <stream_id> remove`

### Filter Control
- `C<n>|filt <slice_id> <low_freq> <high_freq>`

### System Information
- `C<n>|info`
- `C<n>|version`

### Keep-Alive and Ping
- `C<n>|keepalive`
- `C<n>|ping`

### Meter Management
- `C<n>|meter list`

### Profile Management
- `C<n>|profile global info`

### Radio Configuration
- `C<n>|radio name <radio_name>`
- `C<n>|radio callsign <callsign>`
- `C<n>|radio backlight <level>`
- `C<n>|radio filter_sharpness <level>`
- `C<n>|radio reboot`
- `C<n>|radio set <property>=<value>`
- `C<n>|radio static_net_params`
- `C<n>|radio uptime`
- `C<n>|radio gps <command>`
- `C<n>|radio fan <command>`

### Slice Management
- `C<n>|slice create [pan=<stream_id>] [freq=<frequency>] [<parameters>]`
- `C<n>|slice set <slice_id> <property>=<value>`
- `C<n>|slice tune <slice_id> <frequency>`
- `C<n>|slice t <slice_id> <frequency>` (tune shorthand)
- `C<n>|slice remove <slice_id>`
- `C<n>|slice r <slice_id>` (remove shorthand)
- `C<n>|slice list`

### Spot Management
- `C<n>|spot add <parameters>`
- `C<n>|spot remove <spot_id>`

### Subscription Management
- `C<n>|sub pan all`
- `C<n>|sub slice all`
- `C<n>|sub radio all`
- `C<n>|sub meter all`
- `C<n>|sub atu all`
- `C<n>|sub tx all`

### Transmit Control
- `C<n>|transmit set <property>=<value>`
- `C<n>|transmit tune <parameters>`
- `C<n>|xmit <command>`


## Unsupported Features
There are a number of unsupported features, but the following are unlikely to ever be supported:
- Slice Audio Streams
- DAX and DAX IQ Streams
- CAT
