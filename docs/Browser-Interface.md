ProtoFlex has a browser interface to show the state of the emulated radio. Some attributes, like meter values, can be changed while ProtoFlex is running using this interface.

You can connect to the browser interface using http://localhost:5000 if ProtoFlex is running on the same PC as the browser. Otherwise substitute 'localhost' with the IP address of the PC running ProtoFlex.

# Main Page
The main page shows the radio model and version numbers, the maximum limits of the radio and the internal state values.
[![ProtoFlex Main Page](https://raw.githubusercontent.com/rimuadmin/ProtoFlex/main/images/protoflex_main.png)](https://raw.githubusercontent.com/rimuadmin/ProtoFlex/main/images/protoflex_main.png)

# Slices Page

[![ProtoFlex Slices Page](https://raw.githubusercontent.com/rimuadmin/ProtoFlex/main/images/protoflex_slices.png)](https://raw.githubusercontent.com/rimuadmin/ProtoFlex/main/images/protoflex_slices.png)

# Panadapters Page
This page shows panadapters. Note that when a panadapter is closed, the inUse value is set to False and not visible to client, but the internal panadapter object is not removed. I'm unsure the best practice for handling this as it's possible the FlexRadios also retain panadapter objects internally for some purpose.

[![ProtoFlex Panadapters Page](https://raw.githubusercontent.com/rimuadmin/ProtoFlex/main/images/protoflex_pans.png)](https://raw.githubusercontent.com/rimuadmin/ProtoFlex/main/images/protoflex_pans.png)

# Waterfalls Page

[![ProtoFlex Waterfalls Page](https://raw.githubusercontent.com/rimuadmin/ProtoFlex/main/images/protoflex_waterfalls.png)](https://raw.githubusercontent.com/rimuadmin/ProtoFlex/main/images/protoflex_waterfalls.png)

# Meters Page
This page shows the meters that ProtoFlex creates. The values for meters can be changed, but more work need to be done here to make it useful for testing meter values.

[![ProtoFlex Meters Page](https://raw.githubusercontent.com/rimuadmin/ProtoFlex/main/images/protoflex_meters.png)](https://raw.githubusercontent.com/rimuadmin/ProtoFlex/main/images/protoflex_meters.png)

# Sessions Page
This page shows the current sessions that ProtoFlex is maintaining. Sessions contain the connection information and the subscriptions.

[![ProtoFlex Sessions Page](https://raw.githubusercontent.com/rimuadmin/ProtoFlex/main/images/protoflex_sessions.png)](https://raw.githubusercontent.com/rimuadmin/ProtoFlex/main/images/protoflex_sessions.png)

# Spots Page

[![ProtoFlex Spots Page](https://raw.githubusercontent.com/rimuadmin/ProtoFlex/main/images/protoflex_spots.png)](https://raw.githubusercontent.com/rimuadmin/ProtoFlex/main/images/protoflex_spots.png)

# Streams Page
This page shows some of the internal streaming metrics for ProtoFlex. This is more of a diagnostic page for ProtoFlex than it is representative of what you would see inside a FlexRadio.

[![ProtoFlex Streams Page](https://raw.githubusercontent.com/rimuadmin/ProtoFlex/main/images/protoflex_streams.png)](https://raw.githubusercontent.com/rimuadmin/ProtoFlex/main/images/protoflex_steams.png)

# Trigger Page
This page allows you to manually trigger some of the basic status messages.

[![ProtoFlex Trigger Page](https://raw.githubusercontent.com/rimuadmin/ProtoFlex/main/images/protoflex_trigger.png)](https://raw.githubusercontent.com/rimuadmin/ProtoFlex/main/images/protoflex_trigger.png)
