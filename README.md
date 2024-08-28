# esphome-yaml
ESPHome Yaml Configuration Files

To use these templates, you must have these values in your secrets file:

```
# Your Wi-Fi SSID and password
wifi_ssid: "<replace-me>"
wifi_password: "<replace-me>"
api_encryption_key: "<replace-me>"
web_server_auth_user: "<replace-me>"
web_server_auth_password: "<replace-me>"
fallback_hotspot_password: "<replace-me>"
ota_password: "<replace-me>"
```

Upload these template files using `File Editor` into the `esphome` directory. The `.` prefix is important to prevent ESPHome from recognizing the file as a device.

Then update your device files with the appropriate substituions and includes:

```
substitutions:
  device_name: dining-room
  friendly_name: Dining Room
  min_brightness_pct: "15"
  max_brightness_pct: "100"
  min_brightness: "150"
  max_brightness: "1000"

<<: !include .common.yaml
<<: !include .treatlife-ds02s-single-pole-dimmer.yaml
```

If you have any suggestions or improvements feel free to open a PR with additional files or changes and I'm happy to pull them in.
