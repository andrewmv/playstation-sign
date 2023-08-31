# Playstation Sign Driver

4-channel PWD LED driver for ESPHome and HomeAssistant

## Contents

* `playstation_sign.yaml`: ESPHome project file

## Hardware

Input/Output: 5VDC

Target platform: ESP8266

Pin Mapping:
|NodeMCU Pin 	|ESP Pin 	|Direction	|Function 			|
|- 				|- 			|- 			|- 					|
|D1 			|GPIO5 		|Out		|Square PWM			|
|D2 			|GPIO4 		|Out		|Cross PWM			|
|D5 			|GPIO14 	|Out		|Circle PWM			|
|D6 			|GPIO12 	|Out		|Triangle PWM 		|
|D3 			|GPIO0 		|In			|Mode button, BOOTSEL|

## Software Setup

Setup ESPHome per
https://esphome.io/guides/getting_started_command_line

Provide a `secrets.yaml` file in the same directory as `playstation_sign.yaml` with the following contents:

```
ssid: 		# WiFi network name
wappw:		# WiFi password
hotspotpw:	# Create a password for the fallback ad-hoc network, if the device is unable to connect to wifi
apipw:		# Create a password for Homeassistant to use to connect to the device
```

## Compile / Run

```
esphome compile playstation_sign.yaml
esphome run playstation_sign.yaml
```

## Logs / Debug

```
esphome logs playstation_sign.yaml
```
