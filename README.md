# SquareScreen Firmware Releases

Official precompiled binaries for the **Guition ESP32-4848S040** (ESP32-S3 4.0" 480×480 IPS Smart Display).

---

## Latest Binary

* **Current Release**: `v2.1.1`
* **Direct OTA Download**: [squarescreen.bin](squarescreen.bin)
* **Merged Factory Flash (Offset 0x0)**: [squarescreen.merged.bin](squarescreen.merged.bin)

---

## Flashing Instructions

### Method 1: Browser Web OTA (Recommended)
If your SquareScreen is already connected to your local network:
1. Open `http://<device-ip>/update` in your browser.
2. Select `squarescreen.bin`.
3. Click **Upload & Flash**. The device will update and reboot automatically.

### Method 2: Initial Factory Flash via USB-C (esptool)
Connect the device to your computer via USB-C and flash the single merged binary at offset `0x0`:
```bash
esptool --chip esp32s3 write_flash 0x0 squarescreen.merged.bin
```

---

## First-Time Wi-Fi Setup
SquareScreen comes with **no hardcoded credentials**:
1. On initial boot, SquareScreen starts an open Setup Hotspot: `SquareScreen-Setup`
2. Connect to the Wi-Fi network `SquareScreen-Setup` on your phone or PC.
3. Open `http://192.168.4.1/config` in your browser.
4. Enter your local Wi-Fi SSID and password, then click **Save & Reboot**.
5. The device connects to your Wi-Fi and saves the configuration permanently in NVS!

---

## Auto-Update Feed
The firmware update feed is hosted at:
```
https://raw.githubusercontent.com/oh2fxd/squarescreen-fw/main/firmware.json
```

---

## License

This project is licensed under the [MIT License](LICENSE) — Copyright (c) 2026 oh2fxd.
