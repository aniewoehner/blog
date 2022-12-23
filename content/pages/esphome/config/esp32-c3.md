+++
title = "esp32-c3"
date = 2022-12-12

[taxonomies]
tags = ["computer"]
+++

esp32-c3

```yaml
esphome:
  name: test
  platform: ESP32
  board: esp32dev
  platformio_options:
    platform: espressif32
    board: esp32-c3-devkitm-1
    board_build.mcu: esp32c3
    board_build.f_cpu: 160000000L
    upload_protocol: esptool
    build_flags:
      - -D PIO_FRAMEWORK_ARDUINO_ENABLE_CDC
      - -D USBCON
```
