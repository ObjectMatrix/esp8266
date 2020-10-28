# Install Micropython ESP-01 (ESP8266)

## Install esptool 
`pip3 install esptool`

## Erase the flash: 
`esptool.py --port /dev/cu.wchusbserial2210 erase_flash`

## download micropython
` http://micropython.org/download/all/`

## Write flash
`esptool.py --port /dev/cu.wchusbserial2210 --baud 115200 write_flash --flash_size=detect -fm dio 0 esp8266-1m-20200902-v1.13.bin`

## install REPL
REPL stands for Read Evaluate Print Loop, and is the name given to the interactive MicroPython prompt that you can access on the ESP8266.
Using the REPL is by far the easiest way to test out your code and run commands.
There are two ways to access the REPL: either via a wired connection through the UART serial port, or via WiFi.

`brew install repl`
