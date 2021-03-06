# NodeMCU DallasTemperature sensor integrated with MQTT

__This is work in progress. I've just uploaded my CRUD project files for now. Please be patient with me.__

## Data flow

```ascii
 --------     ---------     --------     -----     ----------     -------------
| sensor |   | NodeMCU |   | MQTT   |   | AWS |   | AWS      |   | AWS         |
|        |-->| ESP8266 |-->| Broker |-->| IoT |-->| IoT Rule |-->| Elasticache |
 --------     ---------     --------     -----     ----------     -------------
```

### TL;DR

* Hook up your sensor to `D4`.
* Run a couple of commands:
```bash
$ cp ./platformio-dist.ini platformio.ini
$ pio lib install PubSubClient
$ pio lib install OneWire
$ pio lib install DallasTemperature
```

Edit `platformio.ini` with your credentials and other settings.

Upload and run your code:
```bash
$ pio run -e nodemcuv2 -t upload && pio serialports monitor -b 115200
```

Weee :-)

... more to come.


## Other resources

* [Getting started with NodeMCU, Arduino or Wemos D1 mini](https://github.com/5orenso/arduino-getting-started)
* [NodeMCU code for the toilet sensors integrated with AWS IoT](https://github.com/5orenso/nodemcu-mqtt-toilet-project)
* [NodeMCU code for the toilet lights integrated with AWS IoT](https://github.com/5orenso/nodemcu-mqtt-toilet-project-display)
* [NodeMCU code for home sensors integrated with AWS IoT](https://github.com/5orenso/nodemcu-mqtt-home-sensors)
* [NodeMCU code for BME280 sensor integrated with AWS IoT](https://github.com/5orenso/nodemcu-mqtt-bme280)
* [NodeMCU code for DallasTemperature sensor integrated with AWS IoT](https://github.com/5orenso/nodemcu-mqtt-dallastemperature)
* [Arduino code for Neopixel animations](https://github.com/5orenso/nodemcu-neopixel-animations)
* [AMI for MQTT Broker](https://github.com/5orenso/aws-ami-creation)


## Contribute

Please contribute with pull-requests.
