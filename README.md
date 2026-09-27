# jqh-device-releases

Firmware releases for my DIY devices, published automatically by CI and
fetched over the air by the devices themselves. There's no source code here.

- `channels/<device>.json` — the latest version for a device: version, URL,
  size, sha256 and an HMAC signature (devices reject anything unsigned)
- `firmware/<device>/<version>/` — the images
  - `micropython.bin`: app image, what OTA installs
  - `firmware.bin`: full image for a USB install at offset 0x1000

Devices:

- `crowpanel28-clock` — Tetronimo Clock on an Elecrow CrowPanel 2.8" (ESP32)
