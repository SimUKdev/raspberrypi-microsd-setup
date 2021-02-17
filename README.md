Files I always add to a Raspberry Pi Raspbian Micro SD card before first boot (SSH and WiFi settings)

Both files should be placed in the root of the 'boot' partition after burning a new Raspbian image to a Micro SD card, before inserting it in to a Raspberry Pi for the first boot.

### SSH

* `ssh`

This 'ssh' file is a blank file, with no file extension. It enables SSH on the Raspberry Pi.

### WiFi (wpa_supplicant.conf)

* `wpa_supplicant.conf`

This is template for the wpa_supplicant.conf file.

You should edit the file to have your '`SSID`' (WiFi network name) and '`PSK`' (pre-shared key/password). `scan_ssid` allows it to find "hidden" wifi networks, ones which aren't actively broadcasting their SSID, despite being an active WiFi network. These settings do assume you are using a secured WiFi network with a password (eg: secured with WPA2 or may also be called WPA2-PSK in your router)

If you are not in the United Kingdom you should also change the country from `GB` to your relevant [country code](https://en.wikipedia.org/wiki/ISO_3166-1).

> Further detailed information about `wpa_supplicant.conf` can be found on the official [Raspberry Pi Documentation](https://www.raspberrypi.org/documentation/configuration/wireless/wireless-cli.md)
