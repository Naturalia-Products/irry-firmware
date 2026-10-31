# irry-firmware

Firmware update channel for Irry devices, served by GitHub Pages at `https://naturalia-products.github.io/irry-firmware`.

Each device variant has a folder:

- `<variant>/manifest.json` describes the latest version: version, image path, MD5, ECDSA P-256 signature and release notes link;
- `<variant>/<variant>-<version>.ota.bin` is the OTA image.

| Variant | Board |
|---|---|
| `it7` | x8 relay board (ESP32) |
| `it7ws` | Waveshare ESP32-S3-ETH-8DI-8RO |

Devices install an image only if its signature verifies with the public key compiled into their firmware, so a file changed here is rejected. Pre-release versions (`X.Y.Z-rcN`) are offered for manual install only and are never installed in Auto mode.
