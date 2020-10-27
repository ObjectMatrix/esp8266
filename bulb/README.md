# ESP8266 (ESP-01)The ESP8266 is a low-cost Wi-Fi microchip, with a full TCP/IP stack and microcontroller capability. 

Important note: 
- Use Board Manager Module ESP8266 (version: 2.5.0)  Tools->Board->Board Manager
![board manager](./esp8266-esp-01-board-manager.png)
- Remove GPIO 0 from ground after loading sketch
- Use RST to reset/restart when necessary


## ESP8288 (ESP-01) pin configuration

![pins](https://github.com/ObjectMatrix/esp8266/blob/main/bulb/ESP8266%20Pins.png)


## Recomendation
Use on of this ESP8266 ESP-01 USB Serial Programmer, it's easier, faster than Arduino based board.

![UART Uploader](./serial.png)


## Do not forget
Select required Serial Port when switching between boards

## Preferences (comma separated, for different boards, exaple: ESP8266 (ESP-01), ESP32):  
Example:
- https://dl.espressif.com/dl/package_esp32_index.json,
- http://arduino.esp8266.com/stable/package_esp8266com_index.json
