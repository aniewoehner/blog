+++
title = "lolin c3"
date = 2022-12-12

[taxonomies]
tags = ["computer"]
+++

lolin c3

```yaml
esphome:
  name: lolin-c3-1_0_0
  platformio_options:
    board_build.flash_mode: dio

esp32:
  board: esp32-c3-devkitm-1
  variant: ESP32C3
  framework:
    type: esp-idf
    sdkconfig_options:
      CONFIG_ESP_TASK_WDT_TIMEOUT_S: "10"
      CONFIG_BT_BLE_50_FEATURES_SUPPORTED: y
      CONFIG_BT_BLE_42_FEATURES_SUPPORTED: y

wifi:
  ssid: !secret wifi_ssid
  password: !secret wifi_password
  output_power: 8.5  # will result in a bootloop otherwise

esp32_ble_tracker:
# bluetooth_proxy:  will result in a non reactive state
```
