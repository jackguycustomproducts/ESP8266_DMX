The is a simple sketch that allows an ESP8266 board running Arduino to receive DMX from a lighting control program that is multicasting E1.31 (aka sACN) or Art-Net UDP packets over a WiFi network, and relay the RAW 3x 8-bit RGB DMX channels to a single connected string of WS2812 LEDs. The DMX addressing starts at channel one of the selected universe. Each LED pixel is sent three consecutive DMX channels. You can select a different universe by changing the last 2 octets of the multicast IP address on line 10. Do not set the third octet to 255. This group of addresses are reserved.

MY_SSID should be set to your network name

MY_PASS should be your network password

NUM_LEDS is the number of pixels attached

LED_PIN is the data pin for the LED string. I've had good luck with D3
