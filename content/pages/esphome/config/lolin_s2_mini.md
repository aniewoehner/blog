+++
title = "lolin s2 mini"
date = 2022-12-12

[taxonomies]
tags = ["computer"]
+++

lolin s2 mini

```yaml
esphome:
  name: lolin-s2-1_0_0
  platformio_options:   
    board_build.mcu: esp32s2

esp32:
  board: lolin_s2_mini
  variant: ESP32S2
  framework:
    type: esp-idf
    platform_version: https://github.com/jhamhader/platform-espressif32#8bc085573e4f6986ffcda7050b9607739f3c6976
```
