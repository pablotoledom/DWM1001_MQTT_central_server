# DWM1001_MQTT_central_server
MQTT central server and frontend project to scale to multiple gateways

## This project is based in Qorvo/Decawave MDEK1001 developper kit, which include the WDM1001 board for UWB (Ultra Wide Band)

#Server Requirements

- NodeJs.
- Any MQTT server, the most used is Mosquitto, this configuration use MQTT over Websocket.
- Available Ports for HTTP, MQTT and WS, in this configuration used ports 80, 1883 and 15675 respectively.

#All Infraestructure requirements

- Local Area Network.
- 2 o more Raspberry Pi 3.
- Central server (PC or another Raspberry).
- 8 or more WDM1001 boards (10 is recomended for basic tests).

#How to run

1) Clone this project in your server
2) Run 'npm install' command
3) Run 'npm start' command
