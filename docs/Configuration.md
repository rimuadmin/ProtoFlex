### ProtoFlex is configured with a JSON file

- The max_slices and max_panadapters values can be increased to simulate other models of Flex Radios.

- It can even be used to simulate models that don't yet exist.

[![SmartSDR Connected](https://raw.githubusercontent.com/rimuadmin/ProtoFlex/main/images/protoflex_8x16.png)](https://raw.githubusercontent.com/rimuadmin/ProtoFlex/main/images/protoflex_8x16.png)



## Default JSON file
```JSON
{
  "max_slices": 2,
  "max_panadapters": 2,
  "lineout_gain": 100,
  "lineout_mute": 0,
  "headphone_gain": 100,
  "headphone_mute": 0,
  "remote_on_enabled": 1,
  "pll_done": 0,
  "freq_error_ppb": -4,
  "cal_freq": 2.500000,
  "tnf_enabled": 1,
  "nickname": "ProtoFlex",
  "callsign": "PR0TO",
  "binaural_rx": 0,
  "full_duplex_enabled": 0,
  "band_persistence_enabled": 1,
  "rtty_mark_default": 2125,
  "enforce_private_ip_connections": 0,
  "backlight": 3,
  "mute_local_audio_when_remote": 1,
  "daxiq_capacity": 16,
  "daxiq_available": 14,
  "alpha": 0,
  "low_latency_digital_modes": 0,
  "mf_enable": 1,
  "auto_save": 1,
  "discovery_protocol_version": "3.0.0.3",
  "api_version": "V1.4.0.0",
  "model": "FLEX-6400",
  "serial": "0111-2222-3333-4444",
  "version": "3.10.10.38187",
  "radio_license_id": "00-01-02-03-04-05",
  "requires_additional_license": 0,
  "licensed_clients": 2, 
  "max_licensed_version": "v3",
  "min_software_version": "2.1.20.0",
  "external_port_link": 1,

  "filter_sharpness_voice": {
    "level": 0,
    "auto_level": 1
  },
  "filter_sharpness_cw": {
    "level": 2,
    "auto_level": 1
  },
  "filter_sharpness_digital": {
    "level": 0,
    "auto_level": 1
  },
  "eq": {
    "rx": {
      "mode": 0,
      "freq_63Hz": -10,
      "freq_125Hz": -10,
      "freq_250Hz": 0,
      "freq_500Hz": 0,
      "freq_1000Hz": 5,
      "freq_2000Hz": 5,
      "freq_4000Hz": 0,
      "freq_8000Hz": 0
    },
    "rxsc": {
      "mode": 0,
      "freq_63Hz": 0,
      "freq_125Hz": 0,
      "freq_250Hz": 0,
      "freq_500Hz": 0,
      "freq_1000Hz": 0,
      "freq_2000Hz": 0,
      "freq_4000Hz": 0,
      "freq_8000Hz": 0
    }
  },
  "filter_ranges": {
    "USB": {
      "low": 100,
      "high": 2800
    },
    "DIGU": {
      "low": 0,
      "high": 3000
    },
    "LSB": {
      "low": -2800,
      "high": -100
    },
    "DIGL": {
      "low": -3000,
      "high": 0
    },
    "CW": {
      "low": 0,
      "high": 100
    },
    "AM": {
      "low": -3000,
      "high": 3000
    }
  },
  "network": {
    "static_net_params": {
      "ip": "",
      "gateway": "",
      "netmask": ""
    },
    "radio_tcp_port": 4992,
    "udp_port": 4992
  },
  "bands": {
    "6": {
      "default_mode": "USB",
      "default_frequency": 50.200000,
      "sub_bands": [
        { "name": "6m CW", "start_freq": 50.000, "end_freq": 50.100, "signal_width": 50, "emission_type": "CW" },
        { "name": "6m SSB", "start_freq": 50.100, "end_freq": 50.313, "signal_width": 2800, "emission_type": "SSB" },
        { "name": "6m FT8", "start_freq": 50.313, "end_freq": 50.318, "signal_width": 50, "emission_type": "FT8" },
        { "name": "6m SSB", "start_freq": 50.318, "end_freq": 54.000, "signal_width": 2800, "emission_type": "SSB" }
      ]
    },
    "10": {
      "default_mode": "USB",
      "default_frequency": 28.200000,
      "sub_bands": [
        { "name": "10m CW", "start_freq": 28.000, "end_freq": 28.070, "signal_width": 150, "emission_type": "CW" },
        { "name": "10m Digital (part 1)", "start_freq": 28.070, "end_freq": 28.074, "signal_width": 2800, "emission_type": "DIGI" },
        { "name": "10m FT8", "start_freq": 28.074, "end_freq": 28.077, "signal_width": 50, "emission_type": "FT8" },
        { "name": "10m Digital (part 2)", "start_freq": 28.077, "end_freq": 28.300, "signal_width": 2800, "emission_type": "DIGI" },
        { "name": "10m SSB", "start_freq": 28.300, "end_freq": 29.000, "signal_width": 2800, "emission_type": "SSB" }
      ]
    },
    "12": {
      "default_mode": "USB",
      "default_frequency": 24.930000,
      "sub_bands": [
        { "name": "12m CW", "start_freq": 24.890, "end_freq": 24.915, "signal_width": 150, "emission_type": "CW" },
        { "name": "12m FT8", "start_freq": 24.915, "end_freq": 24.918, "signal_width": 50, "emission_type": "FT8" },
        { "name": "12m Digital (part 1)", "start_freq": 24.918, "end_freq": 24.930, "signal_width": 2800, "emission_type": "DIGI" },
        { "name": "12m Digital (part 2)", "start_freq": 24.930, "end_freq": 24.950, "signal_width": 2800, "emission_type": "DIGI" },
        { "name": "12m SSB", "start_freq": 24.950, "end_freq": 24.990, "signal_width": 2800, "emission_type": "SSB" }
      ]
    },
    "15": {
      "default_mode": "USB",
      "default_frequency": 21.200000,
      "sub_bands": [
        { "name": "15m CW", "start_freq": 21.000, "end_freq": 21.070, "signal_width": 150, "emission_type": "CW" },
        { "name": "15m Digital (part 1)", "start_freq": 21.070, "end_freq": 21.074, "signal_width": 2800, "emission_type": "DIGI" },
        { "name": "15m FT8", "start_freq": 21.074, "end_freq": 21.077, "signal_width": 50, "emission_type": "FT8" },
        { "name": "15m Digital (part 2)", "start_freq": 21.077, "end_freq": 21.200, "signal_width": 2800, "emission_type": "DIGI" },
        { "name": "15m SSB", "start_freq": 21.200, "end_freq": 21.450, "signal_width": 2800, "emission_type": "SSB" }
      ]
    },
    "17": {
      "default_mode": "USB",
      "default_frequency": 18.100000,
      "sub_bands": [
        { "name": "17m CW", "start_freq": 18.068, "end_freq": 18.100, "signal_width": 150, "emission_type": "CW" },
        { "name": "17m FT8", "start_freq": 18.100, "end_freq": 18.103, "signal_width": 50, "emission_type": "FT8" },
        { "name": "17m Digital", "start_freq": 18.103, "end_freq": 18.110, "signal_width": 2800, "emission_type": "DIGI" },
        { "name": "17m SSB", "start_freq": 18.110, "end_freq": 18.168, "signal_width": 2800, "emission_type": "SSB" }
      ]
    },
    "20": {
      "default_mode": "USB",
      "default_frequency": 14.100000,
      "sub_bands": [
        { "name": "20m CW", "start_freq": 14.000, "end_freq": 14.070, "signal_width": 150, "emission_type": "CW" },
        { "name": "20m Digital (part 1)", "start_freq": 14.070, "end_freq": 14.074, "signal_width": 50, "emission_type": "DIGI" },
        { "name": "20m FT8", "start_freq": 14.074, "end_freq": 14.077, "signal_width": 50, "emission_type": "FT8" },
        { "name": "20m Digital (part 2)", "start_freq": 14.077, "end_freq": 14.150, "signal_width": 100, "emission_type": "DIGI" },
        { "name": "20m SSB", "start_freq": 14.150, "end_freq": 14.350, "signal_width": 2800, "emission_type": "SSB" }
      ]
    },
    "30": {
      "default_mode": "DIGU",
      "default_frequency": 10.100000,
      "sub_bands": [
        { "name": "30m CW", "start_freq": 10.100, "end_freq": 10.130, "signal_width": 150, "emission_type": "CW" },
        { "name": "30m Digital (part 1)", "start_freq": 10.130, "end_freq": 10.136, "signal_width": 2800, "emission_type": "DIGI" },
        { "name": "30m FT8", "start_freq": 10.136, "end_freq": 10.139, "signal_width": 50, "emission_type": "FT8" },
        { "name": "30m Digital (part 2)", "start_freq": 10.139, "end_freq": 10.150, "signal_width": 2800, "emission_type": "DIGI" }
      ]
    },
    "40": {
      "default_mode": "LSB",
      "default_frequency": 7.200000,
      "sub_bands": [
        { "name": "40m CW", "start_freq": 7.000, "end_freq": 7.070, "signal_width": 150, "emission_type": "CW" },
        { "name": "40m Digital (part 1)", "start_freq": 7.070, "end_freq": 7.071, "signal_width": 2800, "emission_type": "DIGI" },
        { "name": "40m FT8", "start_freq": 7.071, "end_freq": 7.074, "signal_width": 50, "emission_type": "FT8" },
        { "name": "40m Digital (part 2)", "start_freq": 7.074, "end_freq": 7.100, "signal_width": 2800, "emission_type": "DIGI" },
        { "name": "40m SSB (part 1)", "start_freq": 7.100, "end_freq": 7.175, "signal_width": 2800, "emission_type": "SSB" },
        { "name": "40m SSB (part 2)", "start_freq": 7.175, "end_freq": 7.300, "signal_width": 2800, "emission_type": "SSB" }
      ]
    },
    "60": {
      "default_mode": "USB",
      "default_frequency": 5.357000,
      "sub_bands": []
    },
    "80": {
      "default_mode": "LSB",
      "default_frequency": 3.600000,
      "sub_bands": [
        { "name": "80m CW", "start_freq": 3.500, "end_freq": 3.570, "signal_width": 150, "emission_type": "CW" },
        { "name": "80m FT8", "start_freq": 3.570, "end_freq": 3.573, "signal_width": 50, "emission_type": "FT8" },
        { "name": "80m Digital", "start_freq": 3.573, "end_freq": 3.600, "signal_width": 2800, "emission_type": "DIGI" },
        { "name": "80m SSB (part 1)", "start_freq": 3.600, "end_freq": 3.800, "signal_width": 2800, "emission_type": "SSB" },
        { "name": "80m SSB (part 2)", "start_freq": 3.800, "end_freq": 4.000, "signal_width": 2800, "emission_type": "SSB" }
      ]
    },
    "160": {
      "default_mode": "LSB",
      "default_frequency": 1.810000,
      "sub_bands": [
        { "name": "160m CW", "start_freq": 1.800, "end_freq": 1.830, "signal_width": 150, "emission_type": "CW" },
        { "name": "160m Digital (part 1)", "start_freq": 1.830, "end_freq": 1.837, "signal_width": 2800, "emission_type": "DIGI" },
        { "name": "160m FT8", "start_freq": 1.837, "end_freq": 1.840, "signal_width": 50, "emission_type": "FT8" },
        { "name": "160m Digital (part 2)", "start_freq": 1.840, "end_freq": 1.850, "signal_width": 2800, "emission_type": "DIGI" },
        { "name": "160m SSB", "start_freq": 1.850, "end_freq": 2.000, "signal_width": 2800, "emission_type": "SSB" }
      ]
    }
  }
}
```