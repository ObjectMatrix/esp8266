# Install Micropython ESP-01 (ESP8266)

## Install esptool 
pip3 install esptool

## Erase the flash: 
esptool.py --port /dev/cu.wchusbserial2210 erase_flash

## download micropython
- http://micropython.org/download/all/

## Write flash
esptool.py --port /dev/cu.wchusbserial2210 --baud 115200 write_flash --flash_size=detect -fm dio 0 esp8266-1m-20200902-v1.13.bin
