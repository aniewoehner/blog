+++
title = "esp hardware"
date = 2022-12-12

[taxonomies]
tags = ["computer","hardware","firmware"]
+++

esp8266 vs esp32
8266 has some advantages using unsecured access point, not going to do that
for secured (WPAx) access point, esp32 has advantage

ESP32 - 2016 - plain - Wi-Fi 4, bt 4.2 
	
- ESP32-C6 - 2021 - 32-bit RISC-V, 2.4 GHz Wi-Fi 6, Bt (LE) 5, IEEE 802.15.4, nothing found?
    - mini and wroom
- ESP32-C3 - 2020 - 32-bit RISC-V <160MHz, 2.4 GHz Wi-Fi, Bt (LE) 5, 400 kB SRAM 384 kB ROM, spi/qpi, $10 for one
    - mini and wroom
- ESP32-C2 -  - 32-bit RISC-V <120MHz, 2.4 GHz Wi-Fi, Bt (LE) 5, 272 kB SRAM, 16kB cache, 576 kB ROM, nothing found?
    - mini and wroom
- ESP32-S3 - 2020 - 32-bit LX7, 2.4 GHz Wi-Fi, Bt (LE) 5, 3 for $20
    - mini and wroom
- ESP32-S2 - 2019 - 32-bit LX7, 2.4 GHz Wi-Fi, 3 for $15
    - mini and solo, wrover and wroom not rec for new design, 

- supposedly S2 is much more energy efficient, adds a different camera interface
- S2, C3, S3 have native USB, no need for usb-to-serial chip
- RISC-V are lower cost
- S3 is like updated ESP32, higher specs

- WROOM - does not use the 2 GPIOs
- WROVER - has 8MB SPI PSRAM chip + ESP32-D0WDQ6, 2 GPIOs used for the ram
[https://www.espressif.com/en/products/modulesmini](https://www.espressif.com/en/products/modulesmini)
[https://docs.espressif.com/projects/esp-idf/en/latest/hw-reference/index.html](https://docs.espressif.com/projects/esp-idf/en/latest/hw-reference/index.html)

# lolin

- DoHome ESP-C3 5.99

    - [https://www.amazon.com/DoHome-Development-Dual-Mode-Microcontroller-Integrated/dp/B09HC2SRNP/](https://www.amazon.com/DoHome-Development-Dual-Mode-Microcontroller-Integrated/dp/B09HC2SRNP/)

- ESP-C3-12F $8.99

    - [https://www.amazon.com/JacobsParts-ESP-C3-12F-ESP32-C3-Bluetooth-Development/dp/B09B7Y2VKR/](https://www.amazon.com/JacobsParts-ESP-C3-12F-ESP32-C3-Bluetooth-Development/dp/B09B7Y2VKR/)

- ESP32-C3-DevKitM-1 $8.00

    c3-mini-1-n4

    - [https://www.amazon.com/Espressif-ESP32-C3-DevKitM-1-Development-Board/dp/B08W2J9B8J/](https://www.amazon.com/Espressif-ESP32-C3-DevKitM-1-Development-Board/dp/B08W2J9B8J/)

    - [https://www.mouser.com/ProductDetail/Espressif-Systems/ESP32-C3-DevKitM-1?qs=pUKx8fyJudB1sOWbbEnGFw%3D%3D](https://www.mouser.com/ProductDetail/Espressif-Systems/ESP32-C3-DevKitM-1?qs=pUKx8fyJudB1sOWbbEnGFw%3D%3D)

- 3x ESP32-C3-DevKitM-1 for 13.88
    - [https://www.amazon.com/Teyleten-Robot-ESP32-C3-DevKitM-1-Development-Bluetooth/dp/B0B6HT7L9L/](https://www.amazon.com/Teyleten-Robot-ESP32-C3-DevKitM-1-Development-Bluetooth/dp/B0B6HT7L9L/)

- ESP32-C3-DevKitC-02 $8.00

    ESP32-C3-WROOM-02-N4

    - [https://www.amazon.com/Espressif-ESP32-C3-DevKitC-02-Development-Board/dp/B09D3S4RPZ/](https://www.amazon.com/Espressif-ESP32-C3-DevKitC-02-Development-Board/dp/B09D3S4RPZ/)

    - [https://www.mouser.com/ProductDetail/Espressif-Systems/ESP32-C3-DevKitC-02?qs=stqOd1AaK7%2F1Q62ysr4CMA%3D%3D](    https://www.mouser.com/ProductDetail/Espressif-Systems/ESP32-C3-DevKitC-02?qs=stqOd1AaK7%2F1Q62ysr4CMA%3D%3D)

- ESP32-C3-DevKitC-02U $9.80

    ESP32-C3-WROOM-02U-N4

    - [https://www.amazon.com/Espressif-ESP32-C3-DevKitC-02U-Development-Board/dp/B09D3TGJGD/](https://www.amazon.com/Espressif-ESP32-C3-DevKitC-02U-Development-Board/dp/B09D3TGJGD/)

    - [https://www.mouser.com/ProductDetail/Espressif-Systems/ESP32-C3-DevKitC-02U?qs=Wj%2FVkw3K%252BMATroZS6qcRPw%3D%3D](https://www.mouser.com/ProductDetail/Espressif-Systems/ESP32-C3-DevKitC-02U?qs=Wj%2FVkw3K%252BMATroZS6qcRPw%3D%3D)


- ESP32-C3-DevKitM-1U $9.80

    https://www.amazon.com/Espressif-ESP32-C3-DevKitM-1U-Development-Board/dp/B09D3THNXK/ref=sr_1_10?keywords=ESP32-C3&link_code=qs&qid=1670587675&sourceid=Mozilla-search&sr=8-10
    https://www.mouser.com/ProductDetail/Espressif-Systems/ESP32-C3-DevKitM-1U?qs=Wj%2FVkw3K%252BMBXW0wbfKCpog%3D%3D
    ESP32-C3-MINI-1U

s2 mini may not use esphome, may be waiting for esphome to catch up to platformio 4.3

- s2 mini 2 for $13.99

    - [https://www.amazon.com/dp/B0BBGKJNV5](https://www.amazon.com/dp/B0BBGKJNV5)

- s2 mini hiletgo 3 for $15.49 

    - [https://www.amazon.com/dp/B0B291LZ99](https://www.amazon.com/dp/B0B291LZ99)

- ESP32 S2 Mini ESP32-S2FN4R2 ESP32-S2 1 for 3 for 5 for $23.99

    - [https://www.amazon.com/dp/B0B2ZWZWLW](https://www.amazon.com/dp/B0B2ZWZWLW)

s2 mini

have to press 0 button, tap reset button in order to fire up cdc_acm serial port

