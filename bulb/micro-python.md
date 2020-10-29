# Install Micropython ESP-01 (ESP8266)

## Install esptool 
`pip3 install esptool`

## Switch to `UART download` and now Erase the flash: 
`esptool.py --port /dev/cu.wchusbserial2210 erase_flash`

## download micropython
` http://micropython.org/download/all/`

## Write flash
`esptool.py --port /dev/cu.wchusbserial2210 --baud 115200 write_flash --flash_size=detect -fm dio 0 ./esp8266-20190529-v1.11.bin`

## Switch to `Flash Board` and wait for the Prompt (quite screen: Ctrl-A, CTRL-\)
```
�aua�>��BG�EE�n�YB�eS�!�qs�cR!aG��
>>> help()
Welcome to MicroPython!

For online docs please visit http://docs.micropython.org/en/latest/esp8266/ .
For diagnostic information to include in bug reports execute 'import port_diag'.

Basic WiFi configuration:

import network
sta_if = network.WLAN(network.STA_IF); sta_if.active(True)
sta_if.scan()                             # Scan for available access points
sta_if.connect("<AP_name>", "<password>") # Connect to an AP
sta_if.isconnected()                      # Check for successful connection
# Change name/password of ESP8266's AP:
ap_if = network.WLAN(network.AP_IF)
ap_if.config(essid="<AP_NAME>", authmode=network.AUTH_WPA_WPA2_PSK, password="<password>")

Control commands:
  CTRL-A        -- on a blank line, enter raw REPL mode
  CTRL-B        -- on a blank line, enter normal REPL mode
  CTRL-C        -- interrupt a running program
  CTRL-D        -- on a blank line, do a soft reset of the board
  CTRL-E        -- on a blank line, enter paste mode

For further help on a specific object, type help(obj)
```


## install REPL
REPL stands for Read Evaluate Print Loop, and is the name given to the interactive MicroPython prompt that you can access on the ESP8266.
Using the REPL is by far the easiest way to test out your code and run commands.
There are two ways to access the REPL: either via a wired connection through the UART serial port, or via WiFi.

`brew install repl`
