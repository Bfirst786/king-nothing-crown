# firmware

ESP32-S3 firmware and the desktop asset-conversion utility. Keep every pin in `config.h` and confirm pinouts against the exact purchased displays before final wiring.

Guidance from the brief: no blocking delay longer than 20 ms, a static fallback scene if asset or display initialization fails, a global brightness cap, and no Wi-Fi or Bluetooth during electrical validation. Do not embed lyrics in any asset.
