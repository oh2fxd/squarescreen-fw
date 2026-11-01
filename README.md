# SquareScreen Firmware Releases

Official precompiled binaries for the **Guition ESP32-4848S040** (ESP32-S3 4.0" 480×480 IPS Smart Display).

---

## Latest Binary

* **Current Release**: `v2.1.0`
* **Direct Download**: [squarescreen.bin](squarescreen.bin)

---

## Flashing Instructions

### Method 1: Browser Web OTA (Recommended)
If your SquareScreen is already connected to your local network:
1. Open `http://<device-ip>/update` in your browser.
2. Select `squarescreen.bin`.
3. Click **Upload & Flash**. The device will update and reboot automatically.

### Method 2: PlatformIO / esptool (USB-C)
Connect the device to your computer via USB-C:
```bash
esptool.py --chip esp32s3 -p /dev/ttyACM0 write_flash 0x10000 squarescreen.bin
```

---

## Auto-Update Feed
The firmware update feed is hosted at:
```
https://raw.githubusercontent.com/oh2fxd/squarescreen-fw/main/firmware.json
```
