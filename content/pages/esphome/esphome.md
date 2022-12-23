+++
title = "esphome"
date = 2022-12-05

[taxonomies]
tags = ["computer","hardware","firmware"]
+++

framework for IoT using Espressif esp32 and/or other similar hardware
alternative framework:
[[tasmota]]
[tasmota](/tasmota)
example of camera:
[[zola_blog_content/computer/espcam]]
[espcam](espcam)
[](esp32-cam)

## why

esphome replacing tasmota
- allows better integration with home assistant
- allows actions that do not require the controller?
- builds using python
- next steps:
- newest esphome requires newer python than on renegade/201
	- build firmware elsewhere
	- possible to program from renegade/201?
- Can migrate between Tasmota and esphome, firmware is uploadable through the web interface
	- Insufficient space? Use the gzip version of the firmware.bin

# Building
- Use a python virtual environment to be able to maintain versions of libraries

```sh
python venv
source py /bin/activate
export PIP_CACHE_DIR=<path>
python3 -m pip install --upgrade pip
python3 -m pip install --upgrade wheel
PLATFORMIO_CORE_DIR=$( pwd )/dot_platformio
export PLATFORMIO_CORE_DIR
mkdir -p ${PLATFORMIO_CORE_DIR}
python3 -m pip install --upgrade esphome
this brings in platformio?
pio upgrade?
```

- Or container image

```sh
docker run --rm --net=host -v "${PWD}":/config -it esphome/esphome
```

- Start building a basic configuration yaml for a device by using the wizard
```sh
esphome wizard <devicename>.yaml
```

- Edit that yaml

- Build

```sh
esphome compile <>.yaml
```
	- Older versions used esphome yaml compile

- Firmware produced will be in ./.esphome/build/<node>/.pioenvs/<node>/firmware.bin

[https://esphome.io/guides/configuration-types.html#config-substitutions](https://esphome.io/guides/configuration-types.html#config-substitutions)
esphome config <>.yaml

```sh
sourc ed venv
python3 -m pip install --upgrade pip
python3 -m pip install --upgrade wheel
python3 -m pip install --upgrade cryptography
python3 -m pip install --upgrade esphome

esphome version

esphome wizard <>.yaml
	like device_name
esphome wizard sonoff_s31_01.yaml
	asks name, give it the same name
	esp8266 platform for all sonoff?
	but then esp8285 board?
```

serial console adapter for rock64
default is 1.5M baud, why?
3v3 signaling
but some sort of problem prevents boot
serial@ff13000


### Advanced sensor creation
- generally falls under the idea of template based sensor and follows home assistant
```yaml
- platform: template
  sensors:
    something_state:
      friendly_name: something_status
      value_template: >-
      {% if
      (states()|int >= 5 and (as_timestamp(now())-(as_timestamp(states))))
      %}
        on
      {% else %}
        off
      {% endif %}
```
