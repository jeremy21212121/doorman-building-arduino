# Doorman - Main apartment building door

> web server code is based on the advanced web server example from the [esp8266 arduino library repo.](https://github.com/esp8266/Arduino/tree/master/libraries/ESP8266WebServer/examples/AdvancedWebServer)

This code runs on an arduino-compatible ESP8266-based board to control my apartment door buzzer.

This embedded web server works in conjunction with my [doorman webapp](https://github.com/jeremy21212121/doorman-webapp) to let me into my building.

The ESP8266 board is connected to the door release button via a simple NPN transistor. When the webserver receives a request for /api/toggle, it brings a pin HIGH to power the base pin of the transistor and unlock the door. The lack of moving parts has made this extremely reliable, with months of uptime without needing to touch the device. Flimsy security comes from it only being accessible on my local network.
