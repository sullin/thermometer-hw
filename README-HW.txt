The thermometer board has esp8266 wifi module. It supports 3 kind of sensors:
 - NTC 10kohm 3950 curve sensors. Up to 2 sensors supported, connect first sensor to pins 9,10 and second sensor to pins 11,12. NTC thermistors are cheap and reasonably accurate; depending on sensor construction can tolerate up to around 150C.
 - Thermocouple, type K. Connect to pins 7,8. Thermocouples are very high-temperature sensors and tolerate very high temperatures. The cable of the thermocouple shall not be extended, these are special wires and shall be connected directly to the thermometer board (and the connections shall be kept at the same temperature as the board for accuracy reasons)
 - Dallas DS18B20 1-wire bus sensors. Multiple sensors may be connected, each is identified by its unique id. Connect GND to pin 5, VCC to pin 3 and data to pin 6. Sensors can tolerate up to around 100C and the original ones are very precise at lower temperatures, up to 0.5C. Most of the cheap probes with DS18B20 chips are fakes and the accuracy is usually much worse. As the sensors use a digital bus, you can wire up multiple sensors in parallel.

Unconnected sensors are not shown, only the connected ones show up.

Powering the board:
- You can use either the 12V power input (pins 1,2; 7V to 17V allowed) or power via USB connector.
- The 1-wire sensor power output at pin 3 is NOT suitable for powering the board (use only for 1-wire sensor power, depending on the board model either 5V or 3.3V)

Wifi:
- if the wifi is configured, the board will try to connect to wifi (blinking red) until it succeeds (green).
- if the wifi is not configured, the board will start and access point for configuration (red). Connect to its wifi and use a web browser to set up the connection.
- hold down the button to reset configuration

