# Changelog

## [2.1.0] - 2026-11-01
- Built from commit 4f9d222

## [2.1.0] - 2026-11-01

### Initial Release for Guition ESP32-4848S040

- **Hardware Support**:
  - Full support for Guition ESP32-4848S040 (ESP32-S3, 16MB Flash, 8MB Octal PSRAM).
  - 4.0" 480×480 IPS TFT display driver via LovyanGFX (ST7701S RGB parallel interface).
  - Goodix GT911 capacitive touch screen integration.
  - Backlight PWM brightness control on GPIO 38.

- **Features**:
  - **Shelly 3EM Monitoring**: Live polling of active household power (W/kW), 3-phase breakdown (L1, L2, L3), and voltage with load threshold color alerts. Supports both Gen2/Gen3 RPC and Gen1.
  - **12H Pörssisähkö (Nordpool Spot Price)**: Hourly Finnish electricity prices from api.porssisahko.net with dynamic scaling bar chart, color-coded price tiers, and current hour highlight.
  - **Animated Kissala Mode**: 16-frame 96×96 character animation scaled to 1.6× / 2.0× with live spot price banner.
  - **Weather Station (WX)**: Telemetry support for local weather station.
  - **WWW Configuration Portal**: Dedicated `/config` web page to update WiFi, Shelly, Spot, and Display settings stored in persistent NVS.
  - **Browser OTA**: Integrated `/update` endpoint for zero-wire firmware updates.
  - **Touch Navigation**: Tap top to cycle brightness; tap screen to cycle Energy, Animation, and Weather views.
